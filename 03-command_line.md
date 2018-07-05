# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > pwd
mkdir
rm -r
touch
rm 
mv 
ls -a
cp

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > ls: list all file in the current directory
ls -a: list all contents in the working directory, including hidden files and directios
ls -l: list all contents of a directory in long format 
ls -lh: print sizes in human-readable format 
ls -lah: list all content in the working directoris, including hidden files and directories, in long format and print sizes in human_readable format
ls -t: sort by modification time, newest first
ls -Glp: ?
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls, ls -a, ls -t, ls -l, ls -alt

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > The xargs command in UNIX is a command line utility for building an execution pipeline from standard input. Whilst tools like grep can accept standard input as a parameter, many other tools cannot. Using xargs allows tools like echo and rm and mkdir to accept standard input as arguments.
echo 'one two three' | xargs mkdir
ls
one two three
 


 

