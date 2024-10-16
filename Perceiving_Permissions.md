# Perceiving Permissions

### Changing File Ownership
In this challenge, we learnt how to change the ownership of the file using `chown` command and read the properties of files using `ls -1` command
```
hacker@permissions~changing-file-ownership:~$ ls -1 /flag
/flag
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -1 /flag
/flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{QNia8SL7HQLiJg8fvk8D-aZGaYf.dFTM2QDL0ITO0czW}
```

### Groups and Files
In this challenge, we learnt how to change the ownership group of a file using `chgrp` command
```
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{QtiACu2oBCDVqjLTfq_Fd0HASwn.dFzNyUDL0ITO0czW}
```

### Fun with Group Names
In this challenge, we learnt how to identify our own group name using the `id` ccommand and then change the group using the `chgrp` command
```
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp4474) groups=1000(grp4474)
hacker@permissions~fun-with-groups-names:~$ chgrp grp4474 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{YLAkSDTRwQKY5njRfHwWql-OYsN.dJzNyUDL0ITO0czW}
```

### Changing Permissions
In this challenge, we learnt how to change the permissions for user using the `chmod` command

```
hacker@permissions~changing-permissions:~$ chmod ugo+rwx /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{YHU84bzuOdW8oscB3LG5UlzTNxw.dNzNyUDL0ITO0czW}
```

### Executable Files
In this challenge, we learnt how to allow user to execute a file using `chmod` command with `x`
```
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{EVl0K0sLk_Nt8wA5VhQK4-dgh6d.dJTM2QDL0ITO0czW}
```

### Permission Tweaking Practice
```

```
