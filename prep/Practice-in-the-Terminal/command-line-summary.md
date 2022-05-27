
# **Practice in the Terminal**

**command line, or terminal:** is a text based interface to the system.

**A shell:** is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called  **bash**  which stands for Bourne again shell.

**echo $SHELL** command to know which shell you are using

**up and down arrow keys** to traverse commands history

**left and right arrow keys** to move the cursor where you want to edit commands



## ***Basic Navigation***

**pwd**

Where am I in the system.

**ls [path]**

Perform a listing of the given path or your current directory.

Common options: -l, -h, -a

**cd [path]**

Change into the given path or into your home directory.

**Path**

A description of where a file or directory is on the filesystem.

**Absolute Path**

One beginning from the root of the file system (eg. /etc/sysconfig ).

**Relative Path**

One relative to where you currently are in the system (eg. Documents/music ).

**~ (tilde)**

Used in paths as a reference to your home directory (eg. ~/Documents ).

**. (dot)**

Used in paths as a reference to your current directory (eg. ./bin ).

**.. (dot dot)**

Used in paths as a reference to your current directories parent directory (eg. ../bin ).

**TAB completion**

Start typing and press TAB. The system will auto complete the path. Press TAB twice and it will show you your alternatives.

## ***More About Files***

**file [path]**

Find out what type of item a file or directory is.

**Spaces in names**

Put whole path in quotes ( &quot; ) or a backslash ( \ ) in front of spaces.

**Hidden files and directories**

A name beginning with a . (dot) is considered hidden.

## ***Permissions***

**r (read) w (write) x (execute)**

**Owner or User, Group and Others**

**ls -l [path]**

View the permissions of a file or all items in a directory.

**chmod <permissions> <path>**

Change permissions. Permissions can be either shorthand (eg. 754) or longhand (eg. g+x).

## ***Process Management***

**CTRL + C**

Cancel the currently running process.

**kill <process id>**

Cancel the given process.

Include the option -9 to kill a stubborn process.

**ps**

Obtain a listing of processes and their id's.

Including the option aux will show all processes.

**CTRL + Z**

Pause the currently running process and put it in the background.

**jobs**

See a list of current processes in the background.

**fg <job number>**

Move the given process from the background to the foreground.

## ***Manual Pages***

**man <command>**

View the man page for a command.

**man -k <search term>**

Search for man pages containing the search term.

**Press q to exit man pages**


## ***Filters***

**head**

Show the first n lines.

**tail**

Show the last n lines.

**sort**

Sort lines in a given way.

**wc**

How many words, characters and lines.

**grep**

Search for a given pattern.



## ***Useful Commands***

**du -sh ./***

Find the size of every directory in your current directory.

**df -h**

Display how much disk space is used and also free.

**basename -s .jpg -a *.jpg | xargs -n1 -i cp {}.jpg {}\_original.jpg**

Make a copy of every jpg image file in the current directory and rename adding \_original.

**find /home -mtime -1**

Find all files in the given directory (and subdirectories) which have been modified in the last 24 hours.

**shutdown -h now**

Shutdown the system. (Replace -h with -r for reboot.)

## ***File Manipulation***

**mkdir <directory name>**

Create a directory

**rmdir <directory name>**

Remove a directory (only if empty).

**touch <file name>**

Create a blank file.

**cp <source> <destination>**

Copy the source file to the destination.

**mv <source> <destination>**

Move the source file to the destination.

May also be used to rename files or directories.

**rm <path>**

Remove a file or directory.

Common options: -r -f

## ***Wildcards***

**May be used anywhere in any path.**


Zero or more characters (eg. b*).

**?**

Single character (eg. file.???).

**[]**

Range (eg. b[aio]t).

## ***Piping and Redirection***

**>**

Redirect STDOUT to a file.

**>>**

Append STDOUT to the end of a file.

**2>**

Redirect the STDERR to a file.

**<**

Pass the contents of a file to a program as STDIN.

|

Feed the STDOUT of the program on the left as STDIN to the program on the right.