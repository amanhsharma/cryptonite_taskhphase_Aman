# Processes and Jobs

### Listing Processes
In this challenge, we learnt `ps` command. This commands lists the processes running in the terminal. There are two ways to specify the argument: `ps-ef` and `ps-aux`
```
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 20:40 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/do
root           7       1  0 20:40 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 20:40 ?        00:00:00 /challenge/27426-run-5988
root          72      68  0 20:40 ?        00:00:00 sleep 6h
hacker        95       1  1 20:40 ?        00:00:01 /nix/store/g53lqy8w86jkp2g98rz3dd9dpvmvab12-tigervnc-1.13.1/bin/Xvnc :0 
hacker       100       1  0 20:40 ?        00:00:00 /nix/store/1xhds5s320nfp2022yjah1h7dpv8qqns-bash-5.2p32/bin/bash /nix/st
hacker       109     100  0 20:40 ?        00:00:00 /nix/store/3wb0055984n2whn449hywsl4ag9gcjir-python3-3.11.9/bin/python3.1
hacker       119       1  0 20:40 ?        00:00:00 /nix/store/jnz1wdn463qilzhc8nj1kwccshk65pc9-xfce4-session-4.18.3/bin/xfc
hacker       122       1  0 20:40 ?        00:00:00 /nix/store/rvr416z148cjcxh2bmf5anxpsdvmcvrk-dbus-1.14.10/bin/dbus-launch
hacker       123       1  0 20:40 ?        00:00:00 /run/current-system/sw/bin/dbus-daemon --syslog --fork --print-pid 5 --p
hacker       128       1  0 20:40 ?        00:00:00 /nix/store/3zi7zn2bbz3jpx8ds4nharz67j6ajp9k-xfconf-4.18.3/lib/xfce4/xfco
hacker       137       1  0 20:40 ?        00:00:00 /run/workspace/bin/ssh-agent -s
hacker       139     119  0 20:40 ?        00:00:00 xfwm4
hacker       145     119  0 20:40 ?        00:00:00 xfsettingsd
hacker       153     119  0 20:40 ?        00:00:01 xfce4-panel
hacker       158     119  0 20:40 ?        00:00:00 Thunar --daemon
hacker       167     119  0 20:40 ?        00:00:00 xfdesktop
hacker       183     153  0 20:40 ?        00:00:00 /nix/store/xpgf309sv9w5majf26zg50fpd9vqk1x3-xfce4-panel-4.18.6/lib/xfce4
hacker       187     153  0 20:40 ?        00:00:00 /nix/store/xpgf309sv9w5majf26zg50fpd9vqk1x3-xfce4-panel-4.18.6/lib/xfce4
hacker       292     109  1 20:41 ?        00:00:02 /nix/store/3wb0055984n2whn449hywsl4ag9gcjir-python3-3.11.9/bin/python3.1
hacker       365       1  0 20:41 ?        00:00:00 /run/workspace/bin/xfce4-terminal
hacker       371     365  0 20:41 pts/0    00:00:00 bash
hacker       765     371  0 20:43 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/27426-run-5988
Yahaha, you found me! Here is your flag:
pwn.college{MbzcECMNeuo3WNa_DrxDF29wNEa.dhzM4QDL0ITO0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```

### Killing Processes
In this challenge, we learnt hoe to terminate processes using `kill` command. For this challenge, we first find the process id of dont_run process and then we kill the process.
```
hacker@processes~killing-processes:~$ ps -ef | grep dont_run
hacker        73      71  0 20:57 ?        00:00:00 /challenge/dont_run
hacker       367     300  0 20:57 pts/0    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{wYDxZ5PL9FFHji0Rt4JR_awZnx0.dJDN4QDL0ITO0czW}
```

### Interrupting Processes
In this challenge, we learnt how to interrupt a process that is clogging the terminal using hotkey: `Ctrl-C`
```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{gX52bN30lZbSIvx8JBlic8hlVim.dNDN4QDL0ITO0czW}
```

### Suspending Processes
In this challenge, we learnt how to suspend a process using the `Ctrl-Z` hotkey
```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         382     340  0 21:07 pts/0    00:00:00 bash /challenge/run
root         384     382  0 21:07 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         382     340  0 21:07 pts/0    00:00:00 bash /challenge/run
root         459     340  0 21:07 pts/0    00:00:00 bash /challenge/run
root         461     459  0 21:07 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{4AAmLvWxMmCXps9Qe4Vq6-a9pPW.dVDN4QDL0ITO0czW}
```

### Resuming Processes
In this challenge, we learnt how to resume a process which is currently suspended using the `fg` command.
```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back! Here's your flag:
pwn.college{w3c_0CJtLtLW_FcIIxK-QTg4sz0.dZDN4QDL0ITO0czW}
Don't forget to press Enter to quit me!

Goodbye!
```

### Backgrounding Processes
In this challenge, we learnt how to resume a process in the background using the `bg` command.
```
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         356 S+   bash /challenge/run
root         358 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         356 S    bash /challenge/run
root         455 S    sleep 6h
root         528 S+   bash /challenge/run
root         530 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{8t1De8ZPtv1pO3YCAvOx_kUjx4r.ddDN4QDL0ITO0czW}
```

### Foregrounding Processes
In this challenge, we learnt how to foreground a background process using the `fg` command.
```
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{EpNZ_-v5PA_KoiXxjycJUoAaWVN.dhDN4QDL0ITO0czW}
```

### Starting Backgrounded Processes
In this challenge, we learnt that it is not necessary that the processes should be suspended for backgrounding, we can background it using the `&`
```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 410



Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{s16y5ME_7ZtBqGS3cLZpe7meJBX.dlDN4QDL0ITO0czW}
[1]+  Done                    /challenge/run
```

### Process Exit Codes
```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
74
hacker@processes~process-exit-codes:~$ /challenge/submit-code 74
CORRECT! Here is your flag:
pwn.college{w8Fkv0as34fbr296OrLY-TcTpCW.dljN4UDL0ITO0czW}
```
