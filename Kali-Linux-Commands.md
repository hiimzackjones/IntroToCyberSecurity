# The Terminal
The easiest way to explain the terminal is to compare it to a chat window, or text messaging. The Terminal is essentially a way to talk to the computer using a set of commands and arguments and syntax as input and then it does work based on what you tell it, generally spitting out some sort of output for you or actions like changing settings or file manipulation. The Terminal can be found in the HUB for applications and can also be brought up using <code>Alt+ctrl+t</code> on most Linux Distros. 

The terminal starts with a prompt. In that prompt, it gives you some information. Depending on what operating system you're on. It may show a few different things in the prompt. Just know that generally it will show you 
- The account you're on
- The machine you're on
- The current directory you are working in
- and a symbol to prompt you for your input. For root accounts the symbol will be # and for all other accounts it will be $.  


## Working in the Terminal
The terminal take commands line by line. Commands will act like small applications or functions to do certain jobs. Like finding a file, or showing an IP route. Some commands will work fine by themselves, but many will take arguments and options. Options are exactly as they sound. Arguments are inputs that you give it, sometimes an argument is a number, or a file name, or an IP address. Each command will have different arugments and options that it will accept. 

Possible command syntax
<code>command</code>
<code>command --option</code>
<code>command --option argument</code>
<code>command --option argument argument2 argument3</code>
<code>command argument</code>
Also options are often simplified by a single letter. For example instead of --option, the command may accept -o. These simlifications will be different. Another note is that options can sometimes be stacked on top of each other. 

Here is a logical example. Let's call it a Pseudo Command. This isn't an actual command but you could guess what this command represents.  

<code>drive --fast  --WindowsDown  58W</code>
or 
<code>drive -f -W 58N</code>

Imagine what this command may mean. The command says to drive. With the options of Fast and WindowsDown. It also has an argument of 58W. We could gather that this command would tell the computer to Drive fast with the windows down on 58N. Simple. 

### Super User do!
Sometimes when you are working in terminal, you may be issuing a command that changes some settings in the account or operating system. The OS will sometimes tell you that you do not have permission to make those changes. Whenever the terminal outputs a permissions issue, you should try the command with 'sudo' at the start. This tells it that you are looking to make the changes as an Admin. It will ask for a password and then continue running the command you've issued. To follow with the previous example: <code>sudo drive --slow --AC Route66</code>

### Moving Around in Terminal
Some of the first commands that you should learn are commands to help you move around within the file system, much in the same way that you would click through folders to find files. The following commands are for moving around and looking through directories.  

#### pwd
<code>pwd</code>
PWD stands for Print Working Directory and will print out onto the terminal the Directory (folder) that you're currently in, as well as the directories that it sits in. So if you have a folder named MyFolder in a folder named Files in a folder called Everything, it may look something like Everything/Files/MyFolder. Of course the EverythingFolder is most likely sitting within the user's file structure. For example it may be on your Desktop within your User files.    
For example: <code>/Users/zack/Desktop/Everything/Files/MyFolder</code>

#### ls
<code>ls</code>  
<code>ls -l</code>  
<code>ls -la</code>  
Another terminal command that will help you move around between files is the ls command. This command is simple. It lists all the files and directories in the current working directory. just type ls with no options and press enter. You can also use the -l option to get additional information like the user and ownership of files as well as the time it was created and the permissions. You can also use the -a option to get all files including hidden files. 
For example, here are a few ways to use ls. 
```
Zacks-MacBook-Pro:MyFolder zack$ ls -a
.		..		Folder		HomeWork.txt	picture.jpeg

```

```
Zacks-MacBook-Pro:MyFolder zack$ ls -l
total 0
-rw-r--r--  1 zack  staff  0 Nov  6 14:44 Folder
-rw-r--r--  1 zack  staff  0 Nov  6 14:44 HomeWork.txt
-rw-r--r--  1 zack  staff  0 Nov  6 14:44 picture.jpeg
```

```
Zacks-MacBook-Pro:MyFolder zack$ ls -la
total 0
drwxr-xr-x  5 zack  staff  170 Nov  6 14:44 .
drwxr-xr-x  3 zack  staff  102 Nov  6 14:31 ..
-rw-r--r--  1 zack  staff    0 Nov  6 14:44 Folder
-rw-r--r--  1 zack  staff    0 Nov  6 14:44 HomeWork.txt
-rw-r--r--  1 zack  staff    0 Nov  6 14:44 picture.jpeg
``` 

#### cd
<code> cd Directory</code>  
<code> cd Directory/Directory2</code>  
<code> cd ../ </code>  
<code> cd  ~/Users/Me/Desktop </code>  
The cd command stands for change directory. This command will allow you to move into different directories. It takes various types of arguments to help you move forward and backward and laterial. You can even move recursively down into directories. The arugment for cd needs to be relative to the current working directory. For example if you are currently in a folder named 'Cars' and within that folder there is another folder called 'Hondas' you would simply <code>cd Hondas</code>. You can also move back through folders by using <code>cd ../<code> where the dots represent the previous directory's name. So if you wanted to move back two directories you could use <code>../../<code>. You don't have to type the name of the directory because it is implied. Also, if the directory you are in belongs to a directory that has other directories, you can move laterally by using <code>../OtherFolder</code>  
Lastly, you will often want to use the <code>~</code>
The use of ~ allows you to type an exact directory address regardless of what your current working directory is. So even if you are in Users/Me/Documents/Homework you could use <code> cd ~/Users/Me/Taxes/2017/W2Files </code> and move directly to it. 
### Making and Removing Files & Directories
The next few commands are the basic commands for creating new empty files and directories. This is similar to File -> New Folder/text document or right clicking to do the same job in Windows or even in Mac. Learning these commands will help you do things like organize your files as well as create packages as a developer.   
#### touch
<code>touch newfile.txt</code>    
<code>touch NewCode.js index.js data.json</code>    
<code>touch emptyFile</code>  
The touch command is for creating empty files in the current working directory. The files can be any format with any extension. For example, creating a blank text file you would just <code>touch MyText.txt</code> or if you were planning to write Python code that will need a couple files to work you might create them all at once using <code>touch MyCode.py MoreCode.py </code> The touch command has a few options that are available to allow for timestamp modificaton.
#### mkdir
<code>mkdir DirectoryName</code>  
<code>mkdir FolderOne FolderTwo</code>  
<code>mkdir -p This/Will/Make/These/Directories This/Will/Make/Only/These/Last/Two</code>  
Similar to touch, mkdir creates empty directories in the current working directory. You can create multiple directories as well just by putting spaces between the directory names. The -p option creates directories within directories as long as the parent directories don't already exist.  
Using the above example of  
 <code>mkdir -p This/Will/Make/These/Directories This/Will/Make/Only/These/Last/Two</code>  
  this is what the directory structure will look like.   
```
.
└── This
    └── Will
        └── Make
            ├── Only
            │   └── These
            │       └── Last
            │           └── Two
            └── These
                └── Directories
```  

#### rm
<code>rm FileINeedToDelete.txt</code>  
<code>rm FirstFileToRemove.c SecondFileToRemove.jpg</code>  
Once you've learned how to make files and folders, it's important to know how to remove them. The rm command removes files. It can be used to remove Directories as well, but there is a special option for that. To use rm, make sure you are in the current working directory of the file, and pass the file name as an argument to the rm command as seen above.

#### rmdir
<code>rmdir EmptyDirectory</code>  
<code>rmdir -rf DirectoryWithFilesAndSubDirectories</code>  
Similar to rm, rmdir removes directories. This command without any options will only remove directories that are empty. If you'd like to remove a directory with it's contents, you must use the option -r or more efficently -rf.

### Installing packages with apt-get  
<code>apt-get install packagename</code>  
<code>apt-get update</code>  
<code>apt-cache search .</code>  
<code>dpgk -l</code>  
A vital tool that is utilized in most versions of Linux is the apt-get. APT stands for The Advanced Package Tool and is used to quickly install command line tools. These tools are prepackaged together to make it easy to install. This can be useful for admins to quickly add applications on multiple computers using scripts. To install packages simply use <code>apt-get install ThePackageName</code> and follow the prompt. You can update the list of packages using <code>apt-get update</code>. If you're interested in searching through the repository of available packages, you can use <code>apt-cache search PackageName</code> or look at all of them using <code>apt cache search .</code> And finally you can list the packages that have already been installed buy using <code>dpgk -l</code>. 

It's important to note that each distrubution of Linux may use a different repostories for packages. For example, the popular penentration testing Linux Distro - 'Kali' uses a unique repo with specialized networking tools. 

### Additional Terminal Commands & Tools
#### man
<code>man rmdir</code>  
<code>man touch</code>  
The man command is used to read information about commands to learn what options and syntax to use with the command. It gives examples and is a great resource for learning more about a command. Pass the name of a command into the man command to read it's contents. 

#### grep
<code>grep "Looking for this literal string" InThisFile</code>   
<code>grep -i "ThIsWiLlBecAsEInsenSITive" Inthis</code>  
Grep is a funny sounding command that does a lot of searching magic. The grep command has loads of options and ways to use it to search within files or even output from the terminal. This can be useful if you are looking through multiple files for a paticualr string of information. For example, let's say you have 3 files with a list of first and last names in it. People1.txt People2.txt and People3.txt. You could use grep to find all the names that have the last name of Richards using this example grep:  
```
grep Richards People*.txt

```
This command will search for any lines with the word 'Richards' in it in any file staring with People ending with .txt. It will then print out just those lines. 

>note: the use of * in an argument signifies a wild card. The wildcard is basically a placeholder for any character. Meaning it can represent multiple files.

You can use the -i option to tell grep to find strings even if the letter case is different. The above example:  
<code>grep -i "ThIsWiLlBecAsEInsenSITive" Inthis</code>    
Would output the strings 'thiswillbecaseinsensitive' as well as 'ThisWillBeCaseInsensitive' even though the cases do not match.

---


#### Find
<code> Find thing</code>
<code>Find -name "ReallyImportantFile.txt"</code>  
The Find command will search recursively based off of a regular as an argument. It will take wild cards as part of the input and can be used to find any files with paticular keywords. 
#### Cat
<code> cat Code.py </code>  
<code> cat logfile.txt </code>  
Cat will echo out the contents of any file including text files, binaries, and scripts. This is similar to using Vim but doesn't let you edit the code. Often used with a grep and a pipe: <code> cat file.txt | 'keyword' </code>    
#### Vim
<code> vim program.c </code>  
Vim is a CLI based editor for writing text files, scripts, and code in various languague. Vim can recognize file types and have syntax highlighting. 
> Other terminal based editors are available and are popular. Some of these editors include: Nano, Emacs, gedit.
#### pipe '|'

The pipe character is used to pass output of a command to another command. As seen above a popular combination would to to cat out the contents of a file, then using grep on that output to filter out paticular lines.  
<code>cat logs.txt | grep 'error'</code>    

#### Using $() to nest commands 
Use $() to nest a command within a command. For example <code> Dothis $(ToTheOutPutOfThis) </code>  

#### File Manipulation with >,>>, <,and <<  
<code> > </code> for pushing output of a command into a new file. Overwriting existing content if it's an exisiting file.    
<code> >> </code> for pushing output of a command into an exisiting file, appending the content it already has.   
