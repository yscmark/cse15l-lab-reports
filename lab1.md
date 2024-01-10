# Lab 1

## cd

### No arguments
    [user@sahara ~/lecture1/messages]$ cd
    [user@sahara ~]$ 

* When the command was run, home/lecture1/messages was the working directory.
* cd with no arguments changes the working directory into the home directory.
* This output is not an error.

### Path to a directory as an argument
    [user@sahara ~]$ cd lecture1
    [user@sahara ~/lecture1]$

* When the command was run, the home directory was the working directory.
* cd with a path to a directory as an argument changes the working directory into the directory in the argument.
* This output is not an error.

### Path to a file as an argument
    [user@sahara ~]$ cd lecture1/messages/en-us.txt 
    bash: cd: lecture1/messages/en-us.txt: Not a directory
    [user@sahara ~]$

* When the command was run, the home directory was the working directory.
* cd with a path to a file as an argument doesn't change the working directory and prints an error message.
* This output is an error because cd cannot take in a file as an argument.
