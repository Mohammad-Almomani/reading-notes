# The Command Line

A user interface that is browsed by typing instructions at prompts rather than using a mouse is known as the command line, sometimes known as the terminal, command screen, or text interface.


### The Shell, Bash

There are many different shells accessible, but bash, which stands for Bourne again shell, is the most popular one. (you can use `echo $SHELL` to check you current shell)

A shell is what is found inside a terminal.
The operating system component that controls how the terminal will function and appear after performing (or carrying out) commands on your behalf.


### Basic Navigation!

In this section, the basics of navigation where introduced, three commands where explained:

* PWD (Print Working Directory): Will print the current directory.

* ls (list): List the contents of a directory, you can combine it with flags to list more details, for example; ls -l, ls -a ... .

* cd (Change Directories): will move you to another directory, can be used in relative path `/nextPath`, 
or can be used in reference path `~(ref to home)/firstPath/nextPath`.


### Files

In short words, everything in linux is a file. Linux system is case sensitive and you can have any file extension you want.


### Manual Pages

The manual pages are a collection of pages that describe each command accessible on your system, including what they perform, the intricacies of how you execute them, and the command line parameters they take. 

man (some command):Look up the manual page for a particular command.

man -k (keyword): Do a keyword search for all manual pages containing the given search term.

`Instead of attempting to memorize everything, keep in mind that the man pages make it simple to search things up. `


### File Manipulation!

* how to make a new directory:

    >mkdir (directory name)

* how to remove a directory:

    >rmdir (empty directory name)

    >rm (directory or file name)


* how to create a new file:

    >touch (file name)


* how to copy a file or directory:

    >cp path1(where) path2(to)


* how to move a file or directory:

    >mv path1(where) path2(to)


`Note`: _to rename a file, just move iin the same path but change the name_

