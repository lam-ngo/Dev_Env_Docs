# Introduction  
This document contains guideline for most common commands I use for navigating through the file system.  
This is not an official document with all details.  
I am happy to receive any advice or opinion!  

# File system recap  
Files in Linux file system are arranged in the hierarchy structure.  
The root directory is `/`.  
Below is an example of my root directory hierarchy (1 level only):  
```
/
├── bin
├── boot
├── cdrom
├── dev
├── etc
├── home
├── initrd.img -> boot/initrd.img-4.13.0-32-generic
├── initrd.img.old -> boot/initrd.img-4.10.0-42-generic
├── lib
├── lib64
├── lost+found
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── snap
├── srv
├── sys
├── tmp
├── usr
├── var
├── vmlinuz -> boot/vmlinuz-4.13.0-32-generic
└── vmlinuz.old -> boot/vmlinuz-4.10.0-42-generic
```

# Know where you are  
`pwd` (print working directory) command print the path to your current position in the file system.  

# Navigating  
`cd` (change directory) command.  
`cd` with some first letters of a directory inside current directory, and Tab will auto complete the target directory.  
`cd ..` or `cd ../` go one level backward.  
`cd` and `cd ~` both go to home directory.  
`cd <PATH>` goes to a specific path.  
`cd /` goes to root directory.  

# Useful tips  
Using a package called "tree" for listing directory hierarchy.  
Install command: `sudo apt-get install tree`.
Run command:
`tree <PATH> [OPTION]` (to list the directory hierarchy in the terminal).   
For ex: `tree /home/`.  
WARNING: specifying only the path will print everything in that directory. So `tree /home/` can print thousands of files!  
A proper way should be: `tree /home/ -L 1` with `-L 1` limits the level of output to 1 level only.  
`tree <PATH> > <FILENAME>` (to save the directory hierarchy output to text file).
For ex: `tree /home/ -L 1 >> mydirectory`.  
This package is also useful for describing application code structure.  

# Sources  
http://linuxcommand.org  
https://www.archlinux.org/packages/extra/x86_64/tree/  
