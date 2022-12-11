# The C Programming Language

<img decoding="async" src="http://static.runoob.com/images/runoob-logo.png" width="50%">  

Reference: [RUNOOB.com](https://www.runoob.com/cprogramming/c-tutorial.html)
***

<img decoding="async" src="https://ts1.cn.mm.bing.net/th/id/R-C.d03f731884174042191580fdb6945781?rik=A5f%2fBVOVR8cFsA&riu=http%3a%2f%2fwww.programmerspoint.in%2fimages%2fc-programming-course.png&ehk=sLwe%2fD%2b%2bMQJC3EwuM9DRYJzFdoh6xgXkI5l%2fklgVsI4%3d&risl=&pid=ImgRaw&r=0http://static.runoob.com/images/runoob-logo.png" width="100%">


## Introduction
C language is a general-purpose, procedure-oriented computer programming language. In 1972, in order to transplant and develop the UNIX operating system, ***Dennis Ritchie*** designed and developed the C language at Bell Telephone Laboratories.

The C language is a widely used computer language that is as popular as the Java programming language, and both are widely used among modern software programmers.

The latest C language standard is C23, and the C language standards before it include C18, C17, C11...C99, etc.

---

## C Environment Settings
1. Download VScode
   + Through packages from official website (***all platform are supported***): <https://code.visualstudio.com/Download> 
   + Unix/Linux  
     + Ubuntu/Debian Distributions 
        ```shell
        sudo apt install snap
        snap install vscode
        ```
     + Fedora/RedHat Distributions
        ```shell
        sudo dnf install snap
        snap install vscode
        ```
     + Arch Distributions
        ```shell
        sudo pacman -S snap
        snap install vscode
        ```
   + Windows & Mac  
    Download straightly from the official website: <https://code.visualstudio.com/Download> 

2. Dowdload C Compiler
   + Unix/Linux  
     Normally, all Unix/Linux distributions have built-in gcc, a preinstalled compiler for C.  
     Check the version of gcc:
     ```shell
     gcc -v
     ```
   + Windows  
     + To install gcc on Windows, [MinGW](http://mingw-w64.org/) must be installed first.  
     + In the installation GUI, click to choose the following options: **gcc-core**, **gcc-g++**, **binutils**, and **MinGW runtime**.
     + The final step is to add **bin** directory in MinGW to PATH, so that users and use gcc in the commandline.
  
   + Mac  
     + The best way to install gcc on Mac is to install the [Xcode](http://developer.apple.com/technologies/tools/) Development Environment. 
     + After installation, C programs can be compiled by GNU compiler on Mac.


---



## My First Program
```C
#include <stdio.h>
// This is my first C program
int main(){
    printf("Hello World!\n");
    return 0;
}
```

+ **#include <stdio.h>**: Header file.
+ **int main()**: C program must have a "main()" to run.
+ **printf("Hello World!\n");** : prints "Hello World!" and "\n" means starting a new line.  
+ #Notices:  "**;**" must present at the end of each line of code.

This is a simple C program, in which you can understand the basic structure and syntax of all C program: **head files** and ***one*** **main() function**.

---

## C Language Syntax
After viewing the "Hello World!" program in the previous section, you need to understand more profoundly about the most basic syntax of every C program.

### Comment
Practically speaking, comment is not the most important structure of programs written in any programming language. If we assume that we work alone, we do not need much comment, because we know what we are doing and what's the meaning and use of every line of code. However, when working on a large project with a team, teammates need to communicate with precision. In this situation, comments among hundreds or even thousands of line of code would come in handy and help the teammates communicate effectively.  Therefore, the efficient use of comment would be a necessary lesson for programmers to learn.

```C
// This is a type of comments

/* This is also a type of comments*/

/*
This is a type of comments that
cross multiple lines
*/
```

### Data Type
Data type is the core of all programming language, it regulates the storage of every variable we define. If the value of a variable exceeds the limits of its storage range, the program would have a overflow problem.  
Since most modern computers are loaded with 64 bits OS, the values of storage space and range below do not include values of each data type in 32 bits OS. ***(In case you have questions, yes, 64 bits and 32 bits have different value ranges for each data type)***


### **For integer type,** 

|Data Type|Storage Space|Value Range|
|  ----  |  ----  |  ----  |
| char | 1 byte | -128 ~ 127 or 0 ~ 255 |
| unsigned char | 1 byte | 0 ~ 255 |
| signed char | 1 byte | -128 ~ 127 |
| int | 2 or 4 byte | -32,768 ~ 32,767 or -2,147,483,648 ~ 2,147,483,6470 |
| unsigned int | 2 or 4 byte | 0 ~ 65,535 or 0 ~ 4,294,967,295 |
| short | 2 byte | -32,768 ~ 32,767 |
| unsigned short | 2 byte | 0 ~ 65,535 |
| long | 4 byte | -2,147,483,648 ~ 2,147,483,6470 |
| unsigned long | 4 byte | 0 ~ 4,294,967,295 |  

### **For float type,**

|Data Type|Storage Space|Value Range|Precision|
|  ----  |  ----  |  ----  |  ----  |
| float | 4 byte | 	1.2E-38 ~ 3.4E+38 | 6 decimal places | 
| double | 8 byte | 2.3E-308 ~ 1.7E+308 | 15 decimal places |
| long double | 16 byte | 3.4E-4932 ~ 1.1E+4932 | 19 decimal places |


### **For void type,**  
There are three situation that would allow us to use void type:  
|No.|Storage Space|
|  ----  |  ----  | 
| 1 | The return value of a function is void. ***i.e. void exit(int status)*** | 
| 2 | The function has no parameter. ***i.e. int rand(void)*** | 
| 3 | Pointer points to void. i.e. ***void \*malloc(size_t size)*** |


