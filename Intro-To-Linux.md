# Intro to Linux

### What is Linux?
Linux is a type of operating system that is easy to install, customize, and is free. Linux operating systems are used in computers, servers, mobile devices, and embedded devices as well. 

### Operating Systems
Operating systems are softwares that provide an interface between the user or application to the computer hardware. Windows 10, Apple OSX, Ubuntu Linux, Kali Linux, Android, Apple iOS are different types of Operating Systems.

### Kali Linux 
Kali Linux is a Linux Distrubution designed for advanced Penetration Testing, Security auditing, forensics, and other forms of Cyber Security. Kali comes with over 600 penetration-testing tools preinstalled. 

### The Terminal 
Most of Kali's tools and features are accessed from the command line tool. This tool is called the terminal, sometimes also called the bash. The terminal takes commands from the user via text and all output is in text form as well. 

### Basics of using commands on Linux 

You can open the terminal from the application menu, or from the terminal icon on the tray. Once it's open, a blank window with a prompt will appear. The prompt looks something like the following. 

``` student@kali:~$ ```

``` root@kali:~# ```

Note that a user will have a ```$``` while the root user will have ```#```. 

---

To run a command in terminal, simply type the name of the program and press enter. 

```student@kali:~$ firefox```
Will open Firefox Browser. 

Some applications take **arguments** as well. For example

```Bob@Hax0r:~$ touch myfile.txt```
Will use the program touch to create a file called myfile.txt. 

--- 
To learn what a program does, or what arguments it may take, you can use man pages to read about that application. 

```root@kali:~# man touch```

