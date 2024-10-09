1. Learning from Documentation
Challenge:
 Collect the flag by invoking /challenge/challenge with the argument --giveflag.
Thought Process:
The task required passing --giveflag as an argument. I recalled that arguments are extra data passed to a command, with the syntax being command followed by an argument.
Solution:
/challenge/challenge --giveflag
Upon execution, I got the flag.

2. Learning Complex Usage
Challenge:
Collect the flag by invoking /challenge/challenge with the argument --printfile.
Thought Process:
I knew the --printfile argument prints a file to the terminal, and the argument requires the file's path.
Solution:
/challenge/challenge --printfile /flag
Upon execution, I got the flag.


Reading Manuals
Challenge:
Collect the flag by using a secret option from the man page for the challenge.
Thought Process:
I knew man displays a command's manual, and I could navigate it with the arrow keys and quit with 'q'.
Solution:
man challenge
After reading, I found that running the following command would give the flag:
/challenge/challenge --vhjuka 591
Upon execution, I got the flag.


4. Searching Manuals
Challenge:
Collect the flag by searching through the man page.
Thought Process:
I knew I could search through the man page using n for the next result and N for the previous one.
Solution:
man challenge
I searched for the keyword "flag" and found the right argument. Then I executed the following:
/challenge/challenge --tg
Upon execution, I got the flag.

5. Searching for Manuals
Challenge:
Find the hidden man page that reveals how to use /challenge/challenge.
Thought Process:
I recalled that man -k searches the manual database for relevant entries.
Solution:
man -k challenge

After discovering the manual, I ran:
/challenge/challenge --czgpyo 263
Upon execution, I got the flag.

6. Helpful Programs
Challenge:
Collect the flag by using the --help option.
Thought Process:
Some programs provide usage information through the --help option, so I used that.
Solution:
/challenge/challenge --help
I found that I needed to run:
/challenge/challenge -p

Which gave me the value 981. Using that value:
/challenge/challenge -g 981
Upon execution, I got the flag.


7. Help for Builtins
Challenge:
Collect the flag by looking up the help for the shell builtin challenge.
Thought Process:
I recalled that some commands are shell builtins, and using help shows their usage.
Solution:
help challenge
I found that I needed to pass the value "AaeG6NiH" to the --secret argument. I executed the following:
challenge --secret AaeG6NiH
Upon execution, I got the flag.











