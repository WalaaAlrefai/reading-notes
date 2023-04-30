## The Command Line - What is it, how does it work and how do I get to one.

**A command line**, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.

Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. 

use a command called echo to display a system variable stating my current shell >>>
Typing ***" echo $SHELL "***
its Output in my terminal " /usr/bin/zsh "

## Basic Navigation - An introduction to the Linux directory system and how to get around it.

***"explore the system"***<br>
"__moving around the system"__<br>
 Many tasks rely on being able to get to, or reference the correct location in the system. As such, this stuff really forms the foundation of being able to work effectively in Linux.

__knowing new command like__ <br>
- "ls /etc"
"its for tells ls not to list our current directory but instead to list that directories contents."_


- "ls -l /etc"
" ls with both a command line option and argument. As such it did a long listing of the directory /etc."

 ### Whenever we refer to either a file or directory on the command line, we are in fact referring to a path. ie. A path is a means to get to a particular file or directory on the system.

__There are 2 types of paths we can use, absolute and relative.__ 

- Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / ).

     -Example:"ls /home/ryan/Documents
file1.txt file2.txt file3.txt"

- Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

    -Example:"ls Documents
file1.txt file2.txt file3.txt"

      *same result defferent pathes

***some more building blocks you may use to help build your paths:
 - ~ (tilde) -
    - path /home/ryan/Documents or ~/Documents
 - . (dot) - 
    - It could also be written as ./Documents
 - .. (dotdot)- 
    - ls ../../ and this would do a listing of the root directory.


### More About Files - Find out some interesting characteristics of files and directories in a Linux environment.

***"everything is actually a file"***

### new command " file 
### obtain information about what type of file a file or directory is."

### "Linux is an extensionless system"
Files can have any extension they like or none at all."

### "Linux is case sensitive"


Manual Pages - Learn how to make the most of the Linux commands you are learning.

***"Instead of trying to remember everything, instead remember you can easily look stuff up in the man pages."
** Think about it Like your FRIEND
"The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept. "***

 - man <command>
   - Look up the manual page for a particular command.

 - man -k <search term>
   - Do a keyword search for all manual pages containing the given search term.

 - /<term>
   - Within a manual page, perform a search for 'term'

 - n
   - After performing a search within a manual page, select the next found item.



## File Manipulation - How to make, remove, rename, copy and move files and directories.

- mkdir
  - Make Directory - ie. Create a directory.
    - mkdir -p: tells mkdir to make parent directories as needed 
    - mkdir -pv :which makes mkdir tell us what it is doing
- rmdir
  - Remove Directory - ie. Delete a directory.

- touch
  - Create a blank file.

- cp
  - Copy - ie. Copy a file or directory.
    - cp -r :is for copy directory with its content if it contains files to copy it as well.
- mv
  - Move - ie. Move a file or directory (can also be used to rename).

    - mv foo2 backups/foo3<br>
     "We moved the directory foo2 into the directory backups and renamed it as foo3"
    - mv barney backups/<br>
     "We moved the file barney into backups. As we did not provide a destination name, it kept the same name."
    - mv foo foo3<br>
     "We renamed the file foo to be foo3 (both paths are relative)."
- f.rm
  - Remove - ie. Delete a file.
    - rm -r :When rm is run with the -r option it allows us to remove directories and all files and directories contained within.