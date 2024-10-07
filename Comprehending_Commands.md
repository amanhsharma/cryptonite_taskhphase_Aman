Comprehending Commands
1. Cat: Not the Pet, But the Command!
Challenge
Collect the flag by reading the flag file using the cat command.

Thought Process
I knew that the cat command reads the contents of a file when provided with the file name as an argument.

Solution
I used the following command:
cat flag

Upon execution, I got the flag.

2. Catting Absolute Paths
Challenge
Collect the flag by reading the flag file at its absolute path /flag using the cat command.

Thought Process
I knew that the cat command reads the contents of the file at the given path, and using the absolute path would allow me to access the flag file directly.

Solution
I used the following command:
cat /flag

Upon execution, I got the flag.


3. More Catting Practice
Challenge
Collect the flag by reading the flag file at its absolute path without using the cd command.

Thought Process
The terminal indicated the flag file was located at /usr/include/bsd/flag. Since the challenge required accessing the file without changing directories, I could use cat directly with the file path.

Solution
I used the following command:
cat /usr/include/bsd/flag


Upon execution, I got the flag.

4. Grepping for a Needle in a Haystack
Challenge
Collect the flag by reading the file /challenge/data.txt using the grep command.

Thought Process
I knew that the grep command searches for specific text within a file and prints matching lines. The hint mentioned that the flag starts with "pwn.college," so I used that as the search term.

Solution
I used the following command:
grep pwn.college /challenge/data.txt


Upon execution, I got the flag.


5. Listing Files
Challenge
Collect the flag by listing the files in /challenge.

Thought Process
I knew that the ls command lists all the files in a specified directory. I expected the flag file to be within /challenge, so I used ls to explore the directory.

Solution
I used the following command:
ls /challenge

The output included:
15153-renamed-run-4699 DESCRIPTION.md

I figured the flag would be in 15153-renamed-run-4699, as /challenge/run had been renamed. So, I used the following command:
/challenge/15153-renamed-run-4699


Upon execution, I got the flag.


6. Touching Files
Challenge
Collect the flag by creating two files: /tmp/pwn and /tmp/college, and then running /challenge/run.

Thought Process
I knew that the touch command creates new files.

Solution
I used the following commands:
touch /tmp/pwn
touch /tmp/college
/challenge/run


Upon execution, I got the flag.

7. Removing Files
Challenge
Collect the flag by deleting the delete_me file from the home directory and running /challenge/check.

Thought Process
I knew that the rm command removes files.

Solution
I used the following commands:
rm delete_me
/challenge/check

Upon execution, I got the flag.

8. Hidden Files
Challenge
Collect the flag, which is hidden as a dot-prepended file in /.

Thought Process
I knew that files starting with . are hidden in Linux and can be viewed with the ls -a command.

Solution
I used the following commands:

cd /
ls -a

In the output, I found a file named .flag-184822641918524. I then used:
cat .flag-184822641918524

Upon execution, I got the flag.

9. An Epic File System Quest
Challenge
Collect the flag by following a series of clues scattered across the file system.

Thought Process
The instructions hinted that the first clue was in /, and I would need to follow clues hidden in files named HINT or CLUE. Using ls and cat, I could reveal each clue and follow the path to the flag.

Solution
I used the following commands:
cd /
ls

I found a file named WHISPER. I used:
cat WHISPER

This gave me the next clue. By repeating similar steps using ls, cat, and ls -a, I followed the clues and eventually found the flag.

10. Making Directories
Challenge
Collect the flag by running /challenge/run after creating a /tmp/pwn directory and making a college file within it.

Thought Process
I knew that directories can be created using the mkdir command, and files can be created using the touch command.

Solution
I used the following commands:
mkdir /tmp/pwn
touch /tmp/pwn/college
/challenge/run

Upon execution, I got the flag.

11. Finding Files
Challenge
Collect the flag hidden in a random directory on the file system.

Thought Process
I knew that the entire file system can be searched using the find command with the -name option to locate files by name.

Solution
I used the following command:
find / -name flag


This produced a list of files, some of which were inaccessible to a regular user. It was mentioned that the flag wouldn’t be in restricted files, so I read the contents of the accessible files using cat. After some trial and error, I found the flag.

12. Linking Files
Challenge
Collect the flag stored in /flag, but /challenge/catflag reads /home/hacker/not-the-flag, requiring the use of a symbolic link.

Thought Process
I knew that symbolic links are created using the ln -s command, where the original file path comes before the link path.

Solution
I used the following commands:
ln -s /flag /home/hacker/not-the-flag
/challenge/catflag


Upon execution, I got the flag.



