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
* cd with a path to a directory as an argument changes the working directory into the directory given in the argument.
* This output is not an error.

### Path to a file as an argument
    [user@sahara ~]$ cd lecture1/messages/en-us.txt 
    bash: cd: lecture1/messages/en-us.txt: Not a directory
    [user@sahara ~]$

* When the command was run, the home directory was the working directory.
* cd with a path to a file as an argument doesn't change the working directory and prints an error message.
* This output is an error because cd cannot take in a file as an argument.

## ls

### No arguments
    [user@sahara ~]$ ls
    lecture1

* When the command was run, the home directory was the working directory.
* ls with no arguments prints the files and directories in the working directory.
* This output is not an error.

### Path to a directory as an argument
    [user@sahara ~]$ ls lecture1/
    Hello.class  Hello.java  messages  README

* When the command was run, the home directory was the working directory.
* ls with a path to a directory as an argument prints the files and directories in the directory given in the argument.
* This output is not an error.

### Path to a file as an argument
    [user@sahara ~]$ ls lecture1/Hello.java 
    lecture1/Hello.java

* When the command was run, the home directory was the working directory.
* ls with a file to a directory as an argument prints the argument.
* This output is not an error.

## cat

### No arguments
    [user@sahara ~]$ cat
    

* When the command was run, the home directory was the working directory.
* cat with no arguments removes the prompt and doesn't output anything. The terminal is put into a state where any input is simply duplicated.
* This output is an error because the terminal is left in a state where no commands can be run.

### Path to a directory as an argument
    [user@sahara ~]$ cat lecture1/
    cat: lecture1/: Is a directory

* When the command was run, the home directory was the working directory.
* cat with a path to a directory as an argument prints an error message.
* This output is an error because cat cannot take in directories as arguments.

### Path to a file as an argument
    [user@sahara ~]$ cat lecture1/Hello.java 
    import java.io.IOException;
    import java.nio.charset.StandardCharsets;
    import java.nio.file.Files;
    import java.nio.file.Path;

    public class Hello {
      public static void main(String[] args) throws IOException {
        String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
        System.out.println(content);
      }

* When the command was run, the home directory was the working directory.
* cat with a file to a directory as an argument prints the lines of the file given as the argument.
* This output is not an error.
