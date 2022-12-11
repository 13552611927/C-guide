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

