# Introduction  
This document contains commands guideline for working with files.  
Notice that in this context, files mean either directory, program file or any file system objects.  
This is not an official document with all details.  
I am happy to receive any advice or opinion!  

# Create link to access a file in multiple directories  
To have the same file in multiple directories, we can create multiple copies, but need to change all of them if the content changes.  
Instead, we can create multiple links to the original file in the original directory. When the content changes, we only need to change the original file.  
Soft link is recommended:  
`ln -s <originalfilename> <linkname>`

# Create, List, Delete   
## Text file
`touch [OPTION] <FILENAME>` command creates new text file.
- For example: `touch index.html` create an empty html file named "index.html".  
`echo "some text" >> <FILENAME>` command prints "some text" and output it to a new file.  
- For example: `echo "Hello world!" >> index.html` creates a index.html file which contains "Hello world!".
`cat` has many uses. One of them is to copy from keyboard to display.
- For example: `cat > text.txt` copies from keyboard to a file. A fast
way to create a small text file.  
- `cat text.txt` prints a file on screen.  
- `cat text.txt > new.txt` copies a file. Same as `cp text.txt
new.txt`.  
- `cat text.txt >> new.txt` concatenates files.  
`rm [OPTION] <FILENAME>` command removes a file.  
- For example: `rm index.html`.  

## Folder  
`mkdir [OPTION] <FOLDERNAME>` command creates a folder.  
- For example: `mkdir MyFolder` create an empty folder named MyFolder.  
`rmdir [OPTION] <FOLDERNAME>` command removes a folder.  
- For example: `rmdir MyFolder` removes MyFolder folder.  
`rmdir` cannot remove a non-empty folder. To do this, use `rm -rf <FOLDERNAME>`.  
For more option, type `rmdir --help`.  

## List files  
`ls` lists files in current directory.  
`ls -l` lists a long list: permissions, size, etc.  
`ls -a` lists also hidden files.  

# Find, Copy, Move, Change permission  
`find [OPTION]` to find files.  
`grep [OPTION]` to search text from files.  
`cp [OPTION]` to copy.  
`mv [OPTION]` to moves or renames files and directories.  
`chmod [OPTION]` to change permission.  

# Working with program  
## Installing  
Programs can be installed by:  
- apt-get program.  
- From source files, but it is more complicated.  

The procedure for apt-get:  
- `apt-get update` to update installed programs.  
- `apt-get upgrade` to upgrade or `apt-get install <PROGRAMNAME>` to install a specific program.  

## Executing  
To execute programs in the predefined directories, simply type the program name.
For example: `myprogram`.  

To know the directories where Linux searches for programs, type `echo $PATH`.  
If the path to the desire program is not included in the $PATH, you must type the path to the program.  
For example: `/directory/program`.  

To execute programs in the current directory, type `./<PROGRAMNAME>`.  
For example: `./myprogram`.  

# Working with process   
A process is a running program, which includes:  
- owner
- PID  
- priority  
- controlling terminal  
A Daemon is a process without controlling terminal, meaning it runs continuously as a background process, but not under control of an interactive user.  

`ps` command lists all running process.  
`kill` command sends signal to a process.
- Use only when othing else works.  
- `kill <signal> <pid>`
- signal:  
 - -HUP (hang up): restart or re-read the config file.  
 - -TERM (default): end a process.  
 - -KILL kills the process.  
`skill`, `pkill`, and `killall` give more options.  


# Source  
Merilinna Juhani. Lecturer. Haaga-Helia University of Applied Sciences. Business Information Technology. 2018.  
