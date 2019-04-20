# Easy bash
It is a simple guide that you can scrow down easily and learn quickly (assuming that you have some programming experience).

You might wonder what bash is? 
bash is just a shell command line program and a program language to access your Operating System (OS) which could be Linux or your Mac's terminal 

#### 2 points before we start 

##### 1) comment key word is #
```bash 
the hashtag is use as comments # <--- as an example 
```

##### 2) output (terminal)
Just keep in mind that output (standard output) is the terminal to show our testing :)  

```
stdout:
-------
example
```

## echo

let's begin with a simple echo which prints a line of text. 

```bash
$ echo "bash tutorial"
```

```
output:
-------
bash tutorial 
```

## Moving between your File System 

## Where are you located now? 
## pwd (present working directory)
Yes ~ files are called directory in most of the command line 

```bash
$ pwd #where I am located now?
```

```
output:
-------
/home/chini5ko
# my current directory is chini5ko (your could be different directory )
```


## What if I want to see all the directories and files?
## ls (list command)

```bash
$ ls #list me the files and directories 
```

```bash
output:
-------
hello.txt secretFolder
```
- hello is a file
- secretFolder is a directory 

### what if I don't have this file under my current directory?

## touch (touch program)
this command create a file under your current directory 
```bash
$ touch hello.txt 
```

## mkdir 
this command create a file under your current directory 
```bash
$ mkdir secretFolder # create a directory with the name <anyName>
```


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

## pws






