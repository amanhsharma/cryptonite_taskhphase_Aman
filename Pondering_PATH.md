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

```

### Hijacking Commands
```
```
