# Lab 2 - Command Line


## Objectives:

- Go to the [IoT repository](https://github.com/kevinwlu/iot)
- Study Lessons [1](https://github.com/kevinwlu/iot/tree/master/lesson1) and [2](https://github.com/kevinwlu/iot/tree/master/lesson2)
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
- `ps` : shows process status

$ ps
```
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     2288    2287    2288      18556  pty1      197609 15:29:19 /usr/bin/bash
S    2286       1    2286      21304  pty0      197609 15:28:46 /usr/bin/nano
     2665    2288    2665      24116  pty1      197609 17:33:06 /usr/bin/ps
     2287       1    2287      13252  ?         197609 15:29:19 /usr/bin/mintty
```
- `pwd` : prints working directory
```
$ pwd
/c/Users/micha
```
- `git clone` : clones a git repo do files, needs link to repo to work.
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
- `cd iot` : directs to the 'iot' directory
```
micha@LAPTOP-1LNLL4EL MINGW64 ~
$ cd iot

micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
```
- `ls` : lists the items within a directory (items within iot repo)
```
micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
$ ls
README.md   health/    lesson2/  lesson6/  make/              systems/
apps/       hype/      lesson3/  lesson7/  projects/          tools/
cases/      lesson1/   lesson4/  lesson8/  special_problems/
economics/  lesson10/  lesson5/  lesson9/  standards/
```
- `cd` : cd will go back one directory (~/iot -> ~/)
```
micha@LAPTOP-1LNLL4EL MINGW64 ~/iot (master)
$ cd
micha@LAPTOP-1LNLL4EL MINGW64 ~ (master)
```
- `df` : displays file system information
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

- `clear` : clears the screen from previous inputs.

- `man uname` : manual uname, prints system information

- `uname -a` : prints system information ('-a' = all)
```
$ uname -a
MINGW64_NT-10.0-19044 LAPTOP-1LNLL4EL 3.1.7-340.x86_64 2021-10-12 16:29 UTC x86_64 Msys
```
- `ifconfig` : displays all network configurations (ex. ip addresses), (ipconfig on windows)

- `ping localhost` :  sends a packet to network 'localhost'
```
$ ping localhost

Pinging LAPTOP-1LNLL4EL [::1] with 32 bytes of data:
Reply from ::1: time<1ms
Reply from ::1: time<1ms
Reply from ::1: time<1ms
Reply from ::1: time<1ms

Ping statistics for ::1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
```
- `netstat` : displays network statistics (connections, routing tables, etc.)
```
$ netstat

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    127.0.0.1:9010         laytheme:22988         ESTABLISHED
  TCP    127.0.0.1:9010         laytheme:23027         ESTABLISHED
  TCP    127.0.0.1:9100         laytheme:22959         ESTABLISHED
  TCP    127.0.0.1:22915        laytheme:65001         ESTABLISHED
  TCP    127.0.0.1:22958        laytheme:49821         ESTABLISHED
  TCP    127.0.0.1:22959        laytheme:9100          ESTABLISHED
  TCP    127.0.0.1:22988        laytheme:9010          ESTABLISHED
  TCP    127.0.0.1:23027        laytheme:9010          ESTABLISHED
  TCP    127.0.0.1:24065        laytheme:28194         SYN_SENT
  TCP    127.0.0.1:49821        laytheme:22958         ESTABLISHED
  TCP    127.0.0.1:65001        laytheme:22915         ESTABLISHED
  TCP    192.168.1.161:22916    ec2-18-209-201-158:https  ESTABLISHED
  TCP    192.168.1.161:22950    162.159.136.234:https  ESTABLISHED
  TCP    192.168.1.161:22995    52.159.127.243:https   ESTABLISHED
  TCP    192.168.1.161:23583    a23-216-132-33:https   CLOSE_WAIT
  TCP    192.168.1.161:23746    lb-140-82-114-25-iad:https  ESTABLISHED
  TCP    192.168.1.161:23772    a104-71-130-48:https   CLOSE_WAIT
  TCP    192.168.1.161:23856    cdn-185-199-109-154:https  ESTABLISHED
```
