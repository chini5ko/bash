# Easy bash
It is a simple guide that you can scrow down easily and learn quickly (assuming that you have some programming experience).

#####   Motivation behind this guide:
-   I am a New Yorker, and sometime I just want to open a github repository and learn on my phone while I am riding the trian. 
-   I hope you enjoy the ride with me during this easy_bash tutorial 

What is bash? 
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

# File System basic commands 

Commands: 
- pwd
- ls  
- touch 
- mkdir
- cd
-  (Redirection and append to a file)
- - ``` > and >> ```
- cp 
- mv 
- rm 

These are the 7 commands that you will need to move between your files system as moving between the trian system 

## $ pwd
(pwd stands for present working directory)

```bash
$ pwd #where I am located now?
```

```
output:
-------
/some_path/easy_bash
```
After you cloned this directory in your computer, you would have a folder with the following files:


- README.md
- hello.txt
- secretFolder

### > "What if I want to see all the directories and files?"
## $ ls
 (ls stabd for list)
 - ls command list all the files and directories

```bash
$ ls 
```

```bash
output:
-------
README.md hello.txt secretFolder
```
- hello is a file
- secretFolder is a directory 

### > "what if I don't have this file under my current directory?"

## $ touch (touch program)
this command create a file under your current directory 
```bash
$ touch hello.txt 
```

## $ mkdir 
this command create a directory (or a folder) under your current directory 
```bash
$ mkdir secretFolder # create a directory with the name <anyName>
```
### Now list all the files under your current directory 

## Flags 

### > how do I know if is a file or a directory?
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
It print a bunch of details that we will discuss later, but to check whether is a file or a directory, we just have to look at the first character of each line
- the first line we have "-" which tells you that is a file
- the first character "d" stands for directory in your second line 

### > Wait, did you know that you still have two special directories in your current directory?
- To list all the files, we will use the "-a" flags and use the "-l" (long listing format) as follow:

```bash
$ ls -l -a 
# it works also when you write the flags together as -la 
```

```bash
output:
-------
drwxr-xr-x 1 chini 197609    0 May 30 18:44 .
drwxr-xr-x 1 chini 197609    0 May 15 18:49 ..
drwxr-xr-x 1 chini 197609    0 May 30 18:46 .git
-rw-r--r-- 1 chini 197609    0 May 30 18:45 hello.txt
-rw-r--r-- 1 chini 197609 7647 May 30 18:46 README.md
drwxr-xr-x 1 chini 197609    0 May 30 18:44 secretFolder
```

### > "oh gosh there are 2 directories with dots"
-   one with 1 dot . 
-   the other one with two dots ..
-   (dots files are not listed if you do not use the "-a" flag after your ls command)

## the 1 dot directory . 
It represent your currrent directory 

## the 2 dots directory
It represent your parent directory 

### > how are these dots useful? 
you can move back to your previous directory with the two dots ! 

## $ cd
the cd command stands for change directory 
-   if you want to change your directory to your previos directory, then you use the dots. 
-   You can actually change your directory to the current directory with one dots (but that is not as useful here)
-   you can also move to a directory by typing the direcotry name

```bash
$ cd secretFolder # change your directory to secretFolder
$ pwd #prints your current directory 
$ cd .. # go back to your current directory
$ pwd #prints a directory one level above the previos one 
```

```bash
output:
-------
/some_path/easy_bash/secretFolder
/some_path/easy_bash/
```

### > "How do I write content to a file?"
You have a few options 
-   redirecting from the output of your terminal 
-   Use a editor like Vim -> [http://www.openvim.com] or Nano 

## $ > Redirecting 
Intead of printing to the terminal, we can print it to a file 

```bash
$ cd secretFolder # change your directory to secretFolder
$ touch train7.txt # create a file called trian7.txt
$ echo "Main Street Flushing" > train7.txt # redirecting echo's output to train7.txt
```

```bash
output:
-------

```
No output because it was redirected to the train7.txt file 

## $ >> Appending to a file  
double arrow will append the content to the end of the file without overwring it 

```bash
$ echo "is a place with good traditional Asian food" >> train7.txt # appending to train7.txt
```

```bash
output:
-------

```

# More useful programs:

## $ cat 
cat prints the content of the file to the terminal 

#### Flags:
- n # include number output, starting with one 

```bash
$ cat train7.txt
```

```bash
output:
-------
Main Street Flushing
is a place with good traditional Asian food
```

## $ wc
count the number of words in the file 
#### Flags:
-   -l # count per line 
-   -c # count per bytes or ACISS characters
-   -w # count by the number of words 

```
$ wc -l train7.txt
```
```bash
output:
-------
2 train7.txt
```

### > "Let do piping here to just print the number of line without the file name after displaying the number of lines"

# Piping 
It takes the output of one program as input of the program we are piping to. 

```
$ cat train7.txt | wc -l 
```
```bash
output:
-------
2 
```

## $ sort
sort the contet of a file 
#### Flags:
-   -n # numeric sort
-   -r # sort in reverse 

## $ ls
ls the files
#### Flags:
-   -l # long listing format 
-   -a # show dots files 
-   -d # list directories without showing thier contents 

## $ grep 
searches "x" from the input files and print it to the terminal 

#### Flags:
- -i # igonore cases 
- -E #  -E, --extended-regexp
              Interpret PATTERN as an  extended  regular  expression .

## $ find  
look for file 

#### Flags:
- -name #name of the file
- -exec # do it for each file

## $ cut  
it let you choose an expecific patter to print to the terminal by triming whatever else you dont want to print to the terminal 

#### Flags:
- -f # the field, usually a number 
- -d # d is the delimeter that would be used to let the program know hoow would trimmed 


## $ head 
print from the head 

#### Flags:
- -n number of line that would be printed ot the terminal couniting from the head

## $ tail 
print from the tail

## Variables

### Strings 
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

### arithmetics   
 
```bash
$ age="$((22+1))" # (there is no space between the string and the equal sign !)
$ echo $age
```
```
output:
-------
23
```  
### Here we concluded the small guide for bash !
Let me know at chinisko@outlook.com if you would like to be part of this easy bash guide. 

