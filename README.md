# CodeInjector
This is a command line utility meant to be launched from either powershell, a command prompt, or otherwise.

It will attempt to read an executable binary and inject the code into a remote process.

The target remote victim process should be specified by using either a path to an executable or a process PID.  
If a file path is used the target program will be launched and injected with chosen code.
If a PID is used the target program will simply be injected. (Note: This requires user account privilege 'SeDebugPrivileges')

the injected code is exectued as a thread running within the context of the injected application.
