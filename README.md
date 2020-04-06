# CodeInjector
This is a command line utility meant to be launched from either powershell, a command prompt, or otherwise.

It was created to assist in exploit development and to test the execution of flat binary files such as shellcode.

It will attempt to read a file containing executable binary and inject the code into a remote process.  The code in quesiton should compiled as a flat binary, and not as a full packed executable.  

Tools such as metasploit can be used for binary code creation if desired using the following format:
    msfvenom -p [payload] --platform windows --arch x64 -f raw -o [outfile] [ARGS...]  

The target remote victim process should be specified by using either a path to an executable or a process PID.  
If a file path is used the target program will be launched and injected with chosen code.
If a PID is used the target program will simply be injected. (Note: This requires user account privilege 'SeDebugPrivileges')

the injected code is exectued as a thread running within the context of the injected application.
