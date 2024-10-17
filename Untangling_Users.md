# Untangling Users

### Becoming root with su
In this challenge, we learnt how to get root access using the `su` command
```
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{44LzwOYjmCiOjI5wRyK29N2gw9-.dVTN0UDL0ITO0czW}
```

### Other users with su
In this challenge, we learnt we can also give username as an argumment to switch to user instead of root using `su username`
```
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{YakCRlxQ36NmyVDTUFIF5IXUSKp.dZTN0UDL0ITO0czW}
```

### Cracking Passwords
In this challenge, we learnt how to crack password for switching to the root user. This is done using John The Ripper tool. We do this, using the command `john` followed by the password list.
```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04681g/s 272.6p/s 272.6c/s 272.6C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{EbHBg-z9DLWxnz4DuDZCUbm1p3Q.ddTN0UDL0ITO0czW}
```

### Using sudo
In this challenge, we learnt the modification of `su` command, that is `sudo`
```
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{A1iCKUXoxrGrSWx753YNQDfp4p9.dhTN0UDL0ITO0czW}
```
