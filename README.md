# Easy bash
It is a simple guide that you can scrow down easily and learn quickly (assuming that you have some programming experience).

#####   Motivation behind this guide:
-   I am a New Yorker, and sometime I just want to open a github repository and learn on my phone looking at README.md like this one. 
-   I hope you enjoy the ride with me during this easy_bash tutorial 

You might wonder what bash is? 
bash is just a shell command line program or a programming language to access your Operating System (OS) which could be Linux or your Mac's terminal 

#### 2 points before we start 

##### 1) The comment key word is an hashtag like #
```bash 
the hashtag is use as comments # <--- as an example 
```

##### 2) output (terminal)
Just keep in mind that output (standard output) is the terminal to show our testing :)  

Since we don't have a bash shell nor a terminal in this README.md, we will use the following format as our output

```
stdout:
-------
example
```

## $ echo

let's begin with a simple echo which prints a line of text. 

```bash
$ echo "bash tutorial"
```

```
output:
-------
bash tutorial 
```

# Moving between your File System 

## $ pwd
(pwd stands for present working directory)
- Where are you located now? 


```bash
$ pwd #where I am located now?
```

```
output:
-------
/home/chini5ko
```
My current directory is chini5ko (your could be different directory )
And Yes ~ files are called directory in most of the terminals 


# What if I want to see all the directories and files?
## $ ls
 (ls stabd for list)
 - ls command list all the files and directories

```bash
$ ls 
```

```bash
output:
-------
hello.txt secretFolder
```
- hello is a file
- secretFolder is a directory 

### what if I don't have this file under my current directory?

## $ touch (touch program)
this command create a file under your current directory 
```bash
$ touch hello.txt 
```

## $ mkdir 
this command create a file under your current directory 
```bash
$ mkdir secretFolder # create a directory with the name <anyName>
```
### Now list all the files under your current directory 


## Flags 

### how do I know if is a file or directory?
-   bash command have flags that you can use to display more details ! 

let's use the -l flag ( which stands for long listing format)
```bash
$ ls -l
```

```bash
output:
-------
-rw-rw-rw- 1 chini5ko chini5ko    0 Apr 20 13:57 hello.txt
drwxrwxrwx 1 chini5ko chini5ko 4096 Apr 20 13:57 secretFolder
```
It print a bunch of details that we will discuss later, but check whether is a file we just have to check the first character of each line
- the first line we have "-" which show that your file is a file
- the first character "d" stands for directory in your second line 



## Variables
variables are tricky in bash because the syntax is not as usual as the other programs. 
-  ```<warning>``` You must not put space between the variable's name, the equal sign,and the string assigned to the name 
```bash
$ name="chini5ko" # (there is no space between the string and the equal sign !)
$ echo $name
```
```
output:
-------
chini5ko  
```

### To do 
variables for integer
explain cd 
... Coming back soon :)






