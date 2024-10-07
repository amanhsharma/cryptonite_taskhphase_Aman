Pondering Paths
1. The Root
Challenge
Collect the flag by invoking the pwn program using its absolute path.

Thought Process
The challenge required executing the pwn program using an absolute path. In Linux, an absolute path begins from the root directory (/) and specifies the complete location of a file or program.

Solution
I typed the following command:
/pwn
Upon execution, I received the flag.

2. Program and Absolute Paths
Challenge
Collect the flag by invoking the file named run located in the /challenge directory.

Thought Process
I realized that the run program was located in the /challenge directory, and I needed to execute it using its absolute path.

Solution
I used the following command:
/challenge/run
Upon execution, I received the flag.


3. Position Yourself
Challenge
Collect the flag by executing /challenge/run from a specific path.

Thought Process
To complete the challenge, I needed to change the working directory using cd and then execute /challenge/run. Initially, when I executed:
/challenge/run
Upon execution, i received the flag


4. Position Elsewhere
Challenge
Collect the flag by executing /challenge/run from a different specific path.

Thought Process
After running /challenge/run, I got the message:
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.

This indicated I needed to navigate to /var.

Solution
I used the following command to navigate:
cd /var

Then, I executed:
/challenge/run
Upon execution, I received the flag.

5. Position Yet Elsewhere
Challenge
Collect the flag by executing /challenge/run from another specific path.

Thought Process
Upon executing /challenge/run, I got the message:

Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.

This told me to change the directory to /etc.


Solution
I navigated to /etc using:
cd /etc

Then, I ran:

/challenge/run

Upon execution, I received the flag.

6. Implicit Relative Paths, From /
Challenge
Collect the flag by running /challenge/run using a relative path while in the / directory.

Thought Process
Relative paths are based on the current working directory (cwd) and don’t begin with /. Since my cwd was /, I had to find the path to the run file in the challenge directory. I removed the leading / from the absolute path, making the relative path challenge/run.

Solution
I navigated to / and executed:

cd /
challenge/run

Upon execution, I received the flag.

7. Explicit Relative Paths, From /
Challenge
Collect the flag by running challenge/run using . in the relative path while in the / directory.

Thought Process
. represents the current directory. Since my cwd was /, I had to prepend ./ to the relative path challenge/run to explicitly indicate the current directory.

Solution
I navigated to / and executed:

cd /
./challenge/run

Upon execution, I received the flag.


8. Implicit Relative Path
Challenge
Collect the flag by executing the run program using a relative path while in the /challenge directory.

Thought Process
I navigated to /challenge using:

cd /challenge

Simply running run wouldn’t work because Linux avoids automatically looking in the current directory for commands. I had to prepend ./ to run.

Solution
I executed:
./run

Upon execution, I received the flag.


9. Home Sweet Home
Challenge
Collect the flag by executing /challenge/run while specifying a file path as an argument under the following constraints:

The argument must be an absolute path.
The path must be inside your home directory.
Before expansion, the argument must be three characters or less.
Thought Process
I knew that ~ is shorthand for /home/hacker, my home directory in the Dojo. The path had to be within my home directory, and the argument could only be three characters or less. I figured using ~ met the constraints, so I would prepend ~/ to the filename.

Solution
I used the following command:

/challenge/run ~/f

Upon execution, I received the flag.



