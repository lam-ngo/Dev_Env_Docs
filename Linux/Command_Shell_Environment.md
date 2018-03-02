Read and Set Environmental and Shell Variables

# How they work  
Shell variables only available in the current shell.  
Environmental variables are globally available in the system, for long term usage.  
Normally variable is key:value pair.  
If an environment has more than one value, values are separated by colon(:): `KEY=value1:value2:...`.  

# Listing  
`printenv` lists all variables.  
`printenv <NAME>` prints the value of th chosen variable.  

# Creating  
Variable name is always UPPERCASE.
Shell: `<NAME>=<VALUE>`. Example: `SOME=VAR`.  
Environmental: `export <NAME>=<VALUE>`. Example: `export SOME=VAR`.  
Test by print them: `echo $<NAME>`.  

# Source  
https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps  
