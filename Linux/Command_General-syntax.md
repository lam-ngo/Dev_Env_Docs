Some general practices with command.  

# Option
`<COMMAND> [OPTION]`.  
Options parameter can be short(old): `-a`, or long(new): `--help`.  
For example: `ps --help`.  

# Run as root  
Type `sudo` at the beginning of command.  
Some processes require root privilege to operate.  

# Help or manual  
Help or info for a specific command:  
 `<COMMAND> --help` for help.  
 `man <COMMAND>` for manual.  
 `info <COMMAND>` for info.  
 add `| less` at the end to open help and manual in a different screen.  
 `less` displays text a screen at a time.  
 For example: `ps --help | less`.  

# Quit or escape  
"Control + C" or "q" to quit a program or escape a screen.  

# Naming  
Linux is case sensitive.  
Name length is 1-255 characters.  
File extension has no meaning. Linux checks a file to decide the type.  

# Wild cards
* : any number or character.  
? : any one character.  
[a-g] : any character between a-g.  
[apk] : a, p, k.  

# Redirection  
Arrow (>) redirects output of a program or a command to a file, creates a file
or overwrites an existing file.  
`ls > list.txt`  
Double arrow (>>) adds to an existing file or creates a new file.  
`ls >> list.txt`  
