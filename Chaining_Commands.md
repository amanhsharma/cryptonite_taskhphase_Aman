# Chaining Commands

### Chaining with Semicolons
In this challenge, we learnt how to chain various commands using `;`
```
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{s_PC4Rqz_vGspPxnzqsBZ4WqHl2.dVTN4QDL0ITO0czW}
```

### Your first shell script
In this challenge, we learnt to create a shell script ending with `.sh` suffix.
```
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ chmod u+x x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{0voJm4HRvZmPHwGBByx69-ByV_v.dFzN4QDL0ITO0czW}
```

### Redirecting Script Output
In this challenge, we learnt how to redirect the script output and also the use of piping
```
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{c3omo83Wg_rgw4wHx5XVYpp4gfh.dhTM5QDL0ITO0czW}
```

### Executable Shell Scripts
```
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ ls -l script.sh
-rwxr--r-- 1 hacker hacker 17 Oct 17 20:27 script.sh
hacker@chaining~executable-shell-scripts:~$ chmod o+x script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{4InfJyqVMnGlRucsanGbmC-Z748.dRzNyUDL0ITO0czW}
```
