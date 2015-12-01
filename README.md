# UacBypass
A demo to bypass windows 10 **default** UAC configuration using IFileOperation and dll hijacking.  
**DO NOT USE THIS UNLESS YOU UNDERSTAND EXACTLY WHAT THE CODE DOES**

#Requirements
- An administrator account with UAC enabled.
- UAC level is set to default.
- Tested on Windows 10.10240 (English) x86/x64.

#Usage
- Download and extract/compile a release.
- Run UacBypassTest.exe
- If a cmd with administrator privilege is launched without UAC prompt, the bypass is successful.

#Known issues
- a fake ntwdblib.dll will be copied to C:\Windows\System32\. Any program tries to load this dll will launch cmd.exe and exit itself. **You should remove this file manually after trying the bypass**
- explorer.exe will load UacBypass.dll and cannot unload it. Restart the Windows Explorer process can solve this problem.

Chinese introduction: https://hjc.im/bypass-win10-uac/
