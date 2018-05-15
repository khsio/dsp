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
> > mkdir directoryname
> > rm -r directoryname
> > touch filename
> > rm filename
> > mv fileyouwanttorename newfilename
> > ls -a
> > cp filename directoryname
> > cat filename
> > uniq filename | sort
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

> > list files in a directory**
> > list files in a directory including hidden ones
> > list files in a directory in long form (permissions, links, owner, group, size, time, name)
> > list files in a directory in long form and specific their units (rounded in two decimal places)
> > list files in a directory in long from, including hidden ones, and specific the units they used
> > list files in a directory in a order of the time last modified
> > list files in a directory in long form and group different type of files in different colors and put a("/") after a directory
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -R #display subdirectory as well
> > ls -m #display the name as comma-seperated list
> > ls -c #display files by file timestamp
> > ls -C #display files in columnar format
> > ls -d #display only directory

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > It takes a standard input that seperated by blanks and execuate a command for each items 
> > An example would be to find some files and piped them to xargs to execute the rm syntax to remove all the files. find filenames | xargs rm

 

