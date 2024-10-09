FILE GLOBBING
Matching with *
The * wildcard matches any part of a filename, except for / or a leading .. When the system encounters * in any argument, it replaces it with files or directories matching the pattern. To navigate, I used:
cd /ch*

This took me to the challenge directory. From there, I ran the following command to get the flag:
/challenge/run

2. Matching with ?
The ? wildcard matches exactly one character. I used the following to change directories:
cd /?ha??enge

Then, I executed:
/challenge/run
3.   Matching with []
The [] wildcard matches any single character inside the brackets. After navigating to /challenge/files, I used:
/challenge/run file_[bash]

This matched file_b, file_a, file_s, and file_h.
4. Matching Paths with []
Starting from the home directory, I used the absolute path and bracket globbing to match specific files:
/challenge/run /challenge/files/file_[bash]

5. Mixing Globs
In this challenge, I had to find files "challenging," "educational," and "pwning." I used globbing to search for files beginning with c, e, and p:
/challenge/run [cep]*

6. Exclusionary Globbing
Using ! (or ^ in newer versions) at the start of a bracket negates the pattern, matching characters that aren't listed. To exclude files starting with "pwn," I ran:
/challenge/run [!pwn]*
