1. Redirecting Output
In this challenge, we need to redirect output to a file. Using the command echo PWN > COLLEGE, we successfully write the word "PWN" into a file named "COLLEGE" via output redirection.

hacker@piping~redirecting-output:~$ echo PWN > COLLEGE


2. Redirecting More Output
I redirected the output of /challenge/run to a file called myflag. Then, by using the cat command, I read the contents of myflag to retrieve the flag.


3. Appending Output
I used append-mode redirection (>>) to prevent overwriting the file when adding more data. This way, both the first and second parts of the flag were retained.
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
hacker@piping~appending-output:~$ cat /home/hacker/the-flag


4. Redirecting Errors
To redirect errors, I redirected the output of /challenge/run to myflag and errors to instructions using 2>.
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag


5. Redirecting Input
In this challenge, I needed to write "COLLEGE" to the PWN file and redirect its input to /challenge/run.
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN


6. Grepping Stored Results
I redirected the output of /challenge/run to /tmp/data.txt, then used grep to search for the flag in the file.
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt


7. Grepping Live Output
Here, I piped the output of /challenge/run directly to grep to find the flag in real-time.
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn.college"

8. Grepping Errors
I combined standard output and standard error using 2>&1, then piped them to grep to find the flag.


9. Duplicating Piped Data with Tee
I used tee to duplicate the output of /challenge/pwn to a file, then passed it as input to /challenge/college.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee data.txt | /challenge/college

10. Writing to Multiple Programs
Using process substitution >(), I directed the output of /challenge/hack to both /challenge/the and /challenge/planet.

11. Split-piping stderr and stdout
I split stdout and stderr to be handled by two different programs using 2> for stderr and regular piping for stdout.
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)


