# Lab 2 - Command Line


## Objectives:

- Go to the IoT repository
- Study Lessons 1 and 2
- Open a terminal
Enter the following commands:
```
$ hostname
$ env
$ ps
$ pwd
$ git clone https://github.com/kevinwlu/iot.git
$ cd iot
$ ls
$ cd
$ df
$ mkdir demo
$ cd demo
$ nano file
$ cat file
$ cp file file1
$ mv file file2
$ rm file2
$ clear
$ man uname
$ uname -a
$ ifconfig
$ ping localhost
$ netstat
```
## Commands:
- `hostname` : displays device name
```
micha@LAPTOP-1LNLL4EL MINGW64 ~
$ hostname
LAPTOP-1LNLL4EL
```
- `env` : environment variables
```
$ env
USERDOMAIN=LAPTOP-1LNLL4EL
OS=Windows_NT
COMMONPROGRAMFILES=C:\Program Files\Common Files
mingwusrbin=C:\msys64\usr\bin
PROCESSOR_LEVEL=6
PSModulePath=C:\Program Files\WindowsPowerShell\Modules;C:\WINDOWS\system32\WindowsPowerShell\v1.0\Modules;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\PowerShell\Modules\
CommonProgramW6432=C:\Program Files\Common Files
CommonProgramFiles(x86)=C:\Program Files (x86)\Common Files
opencv2=D:\OPENCV\build\x64\vc14\bin
MSYSTEM_CARCH=x86_64
DISPLAY=needs-to-be-defined
HOSTNAME=LAPTOP-1LNLL4EL
PUBLIC=C:\Users\Public
CONFIG_SITE=/etc/config.site
EXEPATH=C:\Program Files\Git
MSYSTEM_CHOST=x86_64-w64-mingw32
USERNAME=micha
LOGONSERVER=\\LAPTOP-1LNLL4EL
PROCESSOR_ARCHITECTURE=AMD64
ERLANG_HOME=C:\Program Files\erl9.2
LOCALAPPDATA=C:\Users\micha\AppData\Local
COMPUTERNAME=LAPTOP-1LNLL4EL
gtkwave=C:\eda\gtkwave
!::=::\
SYSTEMDRIVE=C:
USERPROFILE=C:\Users\micha
PATHEXT=.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC
SYSTEMROOT=C:\WINDOWS
USERDOMAIN_ROAMINGPROFILE=LAPTOP-1LNLL4EL
OneDriveCommercial=C:\Users\micha\OneDrive - stevens.edu
PROCESSOR_IDENTIFIER=Intel64 Family 6 Model 165 Stepping 2, GenuineIntel
MINGW_PACKAGE_PREFIX=mingw-w64-x86_64
OneDriveConsumer=C:\Users\micha\OneDrive
PWD=/c/Users/micha/demo/python_blockchain_app
SSH_ASKPASS=/mingw64/bin/git-askpass.exe
HOME=/c/Users/micha
TMP=/tmp
LC_CTYPE=en_US.UTF-8
TERM_PROGRAM=mintty
TERM_PROGRAM_VERSION=3.5.2
MSYSTEM_PREFIX=/mingw64
OneDrive=C:\Users\micha\OneDrive - stevens.edu
RABBITMQ_NODENAME=rabbit@localhost
PROCESSOR_REVISION=a502
TMPDIR=/tmp
MOSQUITTO_DIR=C:\Program Files\mosquitto
NUMBER_OF_PROCESSORS=12
XILINX=C:\NIFPGA\programs\Xilinx14_7\ISE
ProgramW6432=C:\Program Files
MIC_LD_LIBRARY_PATH=C:\Program Files (x86)\Common Files\Intel\Shared Libraries\compiler\lib\mic
COMSPEC=C:\WINDOWS\system32\cmd.exe
APPDATA=C:\Users\micha\AppData\Roaming
SHELL=/usr/bin/bash
TERM=xterm
VXIPNPPATH=C:\Program Files (x86)\IVI Foundation\VISA\
WINDIR=C:\WINDOWS
mingw64bin=C:\msys64\mingw64\bin
INTEL_DEV_REDIST=C:\Program Files (x86)\Common Files\Intel\Shared Libraries\
MINGW_CHOST=x86_64-w64-mingw32
ProgramData=C:\ProgramData
SHLVL=1
PLINK_PROTOCOL=ssh
PYTHONPATH=c:\users\micha\appdata\local\programs\python\python311\lib\site-packages
ACLOCAL_PATH=/mingw64/share/aclocal:/usr/share/aclocal
PROGRAMFILES=C:\Program Files
MANPATH=/mingw64/local/man:/mingw64/share/man:/usr/local/man:/usr/share/man:/usr/man:/share/man
ORIGINAL_TEMP=/tmp
ORIGINAL_TMP=/tmp
ALLUSERSPROFILE=C:\ProgramData
TEMP=/tmp
DriverData=C:\Windows\System32\Drivers\DriverData
MSYSTEM=MINGW64
MINGW_PREFIX=/mingw64
SESSIONNAME=Console
VXIPNPPATH64=C:\Program Files\IVI Foundation\VISA\
ProgramFiles(x86)=C:\Program Files (x86)
PATH=/c/Users/micha/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/micha/bin:/c/Program Files/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/Razer Chroma SDK/bin:/c/Program Files/Razer Chroma SDK/bin:/c/Program Files (x86)/Razer/ChromaBroadcast/bin:/c/Program Files/Razer/ChromaBroadcast/bin:/c/Program Files (x86)/Common Files/Intel/Shared Libraries/redist/intel64/compiler:/c/Windows/system32:/c/Windows:/c/Windows/System32/Wbem:/c/Windows/System32/WindowsPowerShell/v1.0:/c/Windows/System32/OpenSSH:/c/Program Files/NVIDIA Corporation/NVIDIA NvDLISR:/c/Windows/system32/config/systemprofile/AppData/Local/Microsoft/WindowsApps:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/110/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/DTS/Binn:/c/Program Files (x86)/Windows Kits/8.1/Windows Performance Toolkit:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/IVI Foundation/VISA/Win64/Bin:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files/MATLAB/MATLAB Runtime/v92/runtime/win64:/c/Program Files/MATLAB/R2021b/runtime/win64:/c/Program Files/MATLAB/R2021b/bin:/cmd:/c/Program Files/Microsoft SQL Server/150/Tools/Binn:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/170/Tools/Binn:/c/Program Files/dotnet:/c/eda/ghdl/bin:/c/eda/gtkwave/bin:/c/Program Files/mosquitto:/c/Program Files/nodejs:/c/users/micha/appdata/local/programs/python/python311:/c/Users/micha/AppData/Local/Programs/Python/Python311/Scripts:/c/Users/micha/AppData/Local/Programs/Python/Python311:/c/Users/micha/AppData/Local/Microsoft/WindowsApps:/c/Users/micha/AppData/Local/Programs/Microsoft VS Code/bin:/c/msys64/mingw64/bin:/c/msys64/usr/bin:/c/Users/micha/.dotnet/tools:/c/Users/micha/.alwaysai/Scripts:/d/OPENCV/build/x64/vc14/bin:/c/Program Files/mosquitto:/c/Users/micha/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl
PS1=\[\033]0;$TITLEPREFIX:$PWD\007\]\n\[\033[32m\]\u@\h \[\033[35m\]$MSYSTEM \[\033[33m\]\w\[\033[36m\]`__git_ps1`\[\033[0m\]\n$
HOMEDRIVE=C:
PKG_CONFIG_PATH=/mingw64/lib/pkgconfig:/mingw64/share/pkgconfig
INFOPATH=/usr/local/info:/usr/share/info:/usr/info:/share/info
HOMEPATH=\Users\micha
ghdl=C:\eda\ghdl
OpenCV=%opencv_dir%/bin
ORIGINAL_PATH=/mingw64/bin:/usr/bin:/c/Users/micha/bin:/c/Program Files/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/Common Files/Oracle/Java/javapath:/c/Program Files (x86)/Razer Chroma SDK/bin:/c/Program Files/Razer Chroma SDK/bin:/c/Program Files (x86)/Razer/ChromaBroadcast/bin:/c/Program Files/Razer/ChromaBroadcast/bin:/c/Program Files (x86)/Common Files/Intel/Shared Libraries/redist/intel64/compiler:/c/Windows/system32:/c/Windows:/c/Windows/System32/Wbem:/c/Windows/System32/WindowsPowerShell/v1.0:/c/Windows/System32/OpenSSH:/c/Program Files/NVIDIA Corporation/NVIDIA NvDLISR:/c/Windows/system32/config/systemprofile/AppData/Local/Microsoft/WindowsApps:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/110/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/DTS/Binn:/c/Program Files (x86)/Windows Kits/8.1/Windows Performance Toolkit:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/IVI Foundation/VISA/Win64/Bin:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files/MATLAB/MATLAB Runtime/v92/runtime/win64:/c/Program Files/MATLAB/R2021b/runtime/win64:/c/Program Files/MATLAB/R2021b/bin:/cmd:/c/Program Files/Microsoft SQL Server/150/Tools/Binn:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/170/Tools/Binn:/c/Program Files/dotnet:/c/eda/ghdl/bin:/c/eda/gtkwave/bin:/c/Program Files/mosquitto:/c/Program Files/nodejs:/c/users/micha/appdata/local/programs/python/python311:/c/Users/micha/AppData/Local/Programs/Python/Python311/Scripts:/c/Users/micha/AppData/Local/Programs/Python/Python311:/c/Users/micha/AppData/Local/Microsoft/WindowsApps:/c/Users/micha/AppData/Local/Programs/Microsoft VS Code/bin:/c/msys64/mingw64/bin:/c/msys64/usr/bin:/c/Users/micha/.dotnet/tools:/c/Users/micha/.alwaysai/Scripts:/d/OPENCV/build/x64/vc14/bin:/c/Program Files/mosquitto:/c/Users/micha/AppData/Roaming/npm
OLDPWD=/c/Users/micha/iot/lesson10
_=/usr/bin/env
```
- `ps` : 
```
$ ps
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     2288    2287    2288      18556  pty1      197609 15:29:19 /usr/bin/bash
S    2286       1    2286      21304  pty0      197609 15:28:46 /usr/bin/nano
     2665    2288    2665      24116  pty1      197609 17:33:06 /usr/bin/ps
     2287       1    2287      13252  ?         197609 15:29:19 /usr/bin/mintty
```
- `pwd` : 
```
$ pwd
/c/Users/micha
```
- `git clone` : 
```
$ git clone
fatal: You must specify a repository to clone.

usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --progress            force progress reporting
    --reject-shallow      don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --bare                create a bare repository
    --mirror              create a mirror repository (implies bare)
    -l, --local           to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    -s, --shared          setup as shared repository
    --recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --recursive ...       alias of --recurse-submodules
    -j, --jobs <n>        number of submodules cloned in parallel
    --template <template-directory>
                          directory from which templates will be used
    --reference <repo>    reference repository
    --reference-if-able <repo>
                          reference repository
    --dissociate          use --reference only while cloning
    -o, --origin <name>   use <name> instead of 'origin' to track upstream
    -b, --branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --upload-pack <path>
                          path to git-upload-pack on the remote
    --depth <depth>       create a shallow clone of that depth
    --shallow-since <time>
                          create a shallow clone since a specific time
    --shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --single-branch       clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --shallow-submodules  any cloned submodules will be shallow
    --separate-git-dir <gitdir>
                          separate git dir from working tree
    -c, --config <key=value>
                          set config inside the new repository
    --server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --filter <args>       object filtering
    --remote-submodules   any cloned submodules will use their remote-tracking branch
    --sparse              initialize sparse-checkout file to include only files at root
```
- `cd iot` : 
```
micha@LAPTOP-1LNLL4EL MINGW64 ~
$ cd iot

micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
```
- `ls` : 
```
micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
$ ls
README.md   health/    lesson2/  lesson6/  make/              systems/
apps/       hype/      lesson3/  lesson7/  projects/          tools/
cases/      lesson1/   lesson4/  lesson8/  special_problems/
economics/  lesson10/  lesson5/  lesson9/  standards/
```
- `cd` : 
```
micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
$ cd
```
- `df` : 
```
$ df
Filesystem           1K-blocks      Used Available Use% Mounted on
C:/Program Files/Git 481555452 431729220  49826232  90% /
D:                   976744444 912653296  64091148  94% /d
```
- `mkdir demo` : makes directory (already exists)
```
micha@LAPTOP-1LNLL4EL MINGW64 ~
$ mkdir demo/
mkdir: cannot create directory ‘demo/’: File exists
```
- `cd demo` : enters demo directory
```
micha@LAPTOP-1LNLL4EL MINGW64 ~
$ cd demo

micha@LAPTOP-1LNLL4EL MINGW64 ~/demo
```
- `nano file` : opens file editor (entered "hello" for example)
![image](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)
- `cat file` : reads file
```
micha@LAPTOP-1LNLL4EL MINGW64 ~/demo
$ cat file
hello
```
- `cp file file1` : copies file and names new file, "file1"

- `mv file file2` : renames "file" to "file2"

- `rm file2` : deletes "file2"

- `clear` : 

- `man uname` : 
```
```
- `uname -a` : 
```
```
- `ifconfig` : 
```
```
- `ping localhost` : 
```
```
- `netstat` :
```
```
