# Pondering PATH

### The PATH Variable
In this challenge, we learnt the concept of  `PATH` variable which consists of bunch of directory paths in which shell will search for programs corresponding to commmands
```
hacker@path~the-path-variable:~$ PATH=''
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{MJq47yPTwRGpFJL6IxtelYcvM85.dZzNwUDL0ITO0czW}
```

### Setting PATH
In this challenge, we learnt how to add custom path to the `PATH` variable to obtain useful results
```
hacker@path~setting-path:~$ PATH='/challenge/more_commands/'
hacker@path~setting-path:~$ /challenge/run win
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{4WLPQkJDvDft-UULvS70yXQ94Hg.dVzNyUDL0ITO0czW}
```

### Adding Commands
```
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ ls
4BU243l7  PWN           lesgo   not-the-flag  script.sh  win.sh
COLLEGE   f             link    outfile       the-flag   x
Desktop   instructions  myflag  p             win        x.sh
hacker@path~adding-commands:~$ ./win
/usr/bin/cat: /flag: Permission denied
hacker@path~adding-commands:~$ chmod +x win
hacker@path~adding-commands:~$ echo $PATH
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~adding-commands:~$ PATH='/home/hacker'
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{YsXrz-EDEDoai_dFL-U1w6gRv3e.dZzNyUDL0ITO0czW}
```

### Hijacking Commands
```
hacker@path~hijacking-commands:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod +x rm
hacker@path~hijacking-commands:~$ PATH='/home/hacker'
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{stfY-5d-vRy_XwI6jBAmHk5k7Ed.ddzNyUDL0ITO0czW}
```
