# 1 - Dev Tools and command line

## Table of Content

1. [Operating systems](dev\_tools.md#operating-systems)
2. [The Command Line](dev\_tools.md#the-command-line)
3. [Beginner Level Terminal](dev\_tools.md#beginner-level)&#x20;
   1. [Navigating in Terminal](dev\_tools.md#navigating-in-terminal)
   2. [Working with Files and Folders](dev\_tools.md#working-with-files-and-folders)
   3. [Listing Files and Flags](dev\_tools.md#listing-files-and-flags)
4. [Terminal Basics Exercises](dev\_tools.md#terminal-basics-exercises)
5. [Intermediate Level Terminal](dev\_tools.md#intermediate-level)
   1. [Permissions and Links](dev\_tools.md#permissions-and-links)
   2. [Redirection](dev\_tools.md#redirection)
   3. [Piping](dev\_tools.md#piping)
6. [Permissions, Redirection, and Piping Exercises](dev\_tools.md#permissions-redirection-and-piping-exercise)
7. [Development Tools](dev\_tools.md#development-tools)
8. [Visual Studio Code Extensions](dev\_tools.md#optional-visual-studio-code-extensions-for-web-development)
9. [More Resources](dev\_tools.md#more-resources)
10. [Advanced Level - 1](dev\_tools.md#advanced-level-1-optional) **{ OPTIONAL }**
11. [Advanced Level - 2](dev\_tools.md#advanced-level-2-optional) **{ OPTIONAL }**

## Operating Systems

An Operating System (OS) is a powerful, and usually large, program that controls and manages the hardware and software on a computer. All computers and computer-like devices require operating systems, including laptops, tablets, desktops, and smartphones. The OS performs all the basic tasks like file management, memory management, process management, handling input and output, and controlling peripheral devices such as disk drives and printers.

The most common operating systems for desktop and laptop computers are:

* Microsoft Windows (Windows 95, Windows 7, Windows 10,...)
* Linux (Debian, Red Hat, Ubuntu,..)
* MacOS
* Chrome OS
* Android and iOS are operating systems for mobile devices.

#### Unix

Unix is ​​a family of operating systems. The first version was developed starting in 1969. Unix is ​​characterized by being portable and multitasking.

Unix operating systems are widely used in a multitude of devices that range from the most capable supercomputers to the mobile phones and computers that we use daily. The philosophy of Unix systems is characterized by:

* a hierarchical file system,
* a large collection of small programs that can work in series,
* the use of text files to store the data,
* treating devices as files.

Linux and MacOS are examples of Unix systems.

#### Linux

Linux is a family of Unix-like operating systems that use the Linux kernel. The name comes from the original programmer, a student named Linus Torvals, who in 1991, working with the GNU project of the Free Software Foundation, created the first version of this operating system.

Linux development is one of the clearest examples of free, open source software development by a diverse community of programmers all over the world. Anyone can use the operating system, study it and modify it. The open source nature of Linux is protected by the GPL (GNU General Public License).

#### Ubuntu

Ubuntu is a Linux distribution. It is an open-source operating system aimed at desktop users, and its strengths are that it is easy to use and install. Although the desktop is somewhat different from Windows or Mac OS, a user who is accustomed to any of these operating systems will not have many problems becoming familiar with Ubuntu. Ubuntu is a Linux distribution based on Debian and composed mostly of free and open-source software. Ubuntu is officially released in three editions: Desktop, Server, and Core for Internet of things devices and robots.

If you are using [Ubuntu](https://ubuntu.com/), you will see this sreen:

![](<../../../../.gitbook/assets/image (97).png>)

Demo of Ubuntu:

* The friendly Desktop
* The filesystem: navigate through folders and files using File Manager
* Ubuntu software: a tool to install software easily

## The Command Line

The **Command Line**, also knows as **Bash**, **Terminal** or **Shell** (**Línea de Comandos** ó **Símbolo de sistema** in Spanish) is a way of controlling a computer, based on a text interface.

![](<../../../../.gitbook/assets/image (31).png>)

Why should I use the command line/terminal?

* Once you know the basics, it helps you to interact with you computer faster
* Some software for developers must always be used from a terminal
* You have more control over the software
* It allows you to create scripts (lists of commands) and automate manual tasks
* It is what hackers use in movies.

#### How do I use the terminal on my computer?

Here are the instructions for the three operating system:

* **MacOS:** You can find the Terminal.app in your Applications, in the folder Utilities. An alternative way to open the Terminal is to search with Spotlight and type in “terminal”. Select the application called terminal and press the return key. This should open up an app with a black background. When you see your username followed by a dollar sign, you’re ready to start using the command line.
* **Linux:** You can open the Terminal by directly pressing \[ctrl+alt+T] or you can search for it by clicking the dash (#) icon, typing in “terminal” in the search box, and opening the Terminal application. This should open up an app with a black background. When you see your username followed by a dollar sign, you’re ready to start using the command line.
* **Windows:** Windows has its own **Command Prompt**. It is very similar to the Unix command line, but some commands are not exactly the same. For the main differences go to this [link](https://enexdi.sciencesconf.org/data/pages/windows\_vs\_mac\_commands\_1.pdf). Because of these differences, and because we want to learn UNIX commands, we use the **Git Bash**. Go to the Windows "Start" button and search the program **Git Bash**. When you open it you will see a screen like this one:

![](<../../../../.gitbook/assets/image (105).png>)

After you have followed the instructions, open a terminal and write `ls`, then press the `Enter` key. What do you see?

#### Commonly used commands

These are the most used commands that you will quickly become comfortable with during the course. These commands allow you to effectively move around the filesystem and write software on your laptop. There are more commands in the tables with more commands and descriptions below.

* `cd` - change directory. To move up one folder level and into the parent directory use: `cd ..`
* `ls` - list the contents of a directory. Can also be used as `ls [directory_name]` to list the contents of a specific directory without actually moving (with `cd`) to it
* `pwd` - print working directory: print the full location of the folder you are working in
* `mkdir [name]` - make directory: create a new directory, with the given `name` after a space
* `touch [file_name]` - create a new file, with the given name (don't forget to add the extension, like `.css` or `.html`)
* `rm [file_name]` - remove a file
* `rm -r [directory_name]` - remove a directory (**and all files inside that directory**)

**Getting Help**

When you're stuck and need help with a command, help is usually only a few keystrokes away. Help on most commands is built right into the commands themselves, available through online help programs (such as [https://linux.die.net/man](https://linux.die.net/man)), and of course online.

**Using a command's built-in help**\
Many (but not all) commands have simple help screens that can be called with special command flags. These flags usually look like `-h` or `--help`. Example: `grep --help`.

**Online manuals: the man pages**\
The best source of information for most commands are the manual pages, also known as the man pages. To read a command's man page, type `man` plus a space and the command.

| Example   | Info                                   |
| --------- | -------------------------------------- |
| `man ls`  | Get help on the ls command             |
| `man man` | Get the manual for info on the manual! |



## Beginner Level



### { Navigating in Terminal. }

#### Objectives:

By the end of this chapter, you should be able to:

* Define what Terminal is and how it is structured
* Navigate through and list files on your machine
* Define the following terms: shell, terminal, directory, absolute path, relative path

| Linux/Mac          | Windows         | Description                                                                |
| ------------------ | --------------- | -------------------------------------------------------------------------- |
| `pwd`              | `cd`            | print working directory: shows current location                            |
| `cd`               | `cd`, `chdir`   | change directory; returns to the home directory                            |
| `cd directory`     | `cd directory`  | change into the specified directory                                        |
| `cd ~`             |                 | \~ means home directory; shortcut to the home directory                    |
| `cd ..`            | `cd ..`         | move up one directory                                                      |
| `cd -`             |                 | returns to the directory of your previous location                         |
| `ls`               | `dir /w`        | list all files in current directory                                        |
| `ls directory`     | `dir directory` | list all files in the specified directory                                  |
| `ls -l`            | `dir`           | list all files in long format: one file per line, with info about the file |
| `ls -a`            | `dir /a`        | list all files, including hidden files (= filenames that start with .)     |
| `ls -ld directory` |                 | show detailed information about the directory                              |
| `ls /usr/bin/d*`   | `dir d*.*`      | list all files starting with d in the `/usr/bin` directory                 |

****

#### What is Terminal?

Terminal is an application that gives us a command line interface (or CLI) to interact with the computer. Everything you can do in Finder/Windows Explorer you can do in Terminal. Developers use Terminal because it is usually much faster to use Terminal than a graphical user interface (GUI) such as Finder/Windows Explorer. Although the Terminal interface can seem daunting at first, with a bit of practice, you'll be up to speed in no time!

#### What is a shell? Bash/ZSH

You will also hear the term "shell" when learning about Terminal so it is important to distinguish between these terms. From [Stack Overflow](https://superuser.com/questions/144666/what-is-the-difference-between-shell-console-and-terminal):

> The **shell** is the program which actually processes commands and returns output. Most shells also manage foreground and background processes, command history and command line editing. These features (and many more) are standard in bash, the most common shell in modern linux systems. (We are using `zsh`).
>
> A **terminal** refers to a wrapper program which runs a shell. Decades ago, this was a physical device consisting of little more than a monitor and keyboard. As unix/linux systems added better multiprocessing and windowing systems, this terminal concept was abstracted into software.

If you are using Windows, there is a great tool called [Babun](https://babun.github.io/), which is a shell that you can install and use the same commands as if you were on Mac or Linux. This is not essential, but using it will enable you to more easily follow along with the material.

#### How Terminal is Structured

In Terminal, all files and folders begin at the root directory. The root directory is noted by a `/`. Inside the root directory are essential files/folders that your machine needs, but we do not modify the files and folders in the root directory often. Inside of the root directory, we have a folder called `Users` which contains all of the user accounts on your computer. If you move into the directory for your user account, you will be in the `home` directory, which is denoted by `~`. For example, if your user name on the computer is `eschoppik`, then your home directory would be `/Users/eschoppik`. A synonym for the `/Users/eschoppik` path is `~` when you are logged in as `eschoppik`.

#### Moving Around

The first thing you want to start to understand when using Terminal is how to navigate from folder to folder. One of the most common commands you will be using in Terminal is `cd` which is short for "change directory." In order to change a directory, type `cd` followed by the directory or a path to the directory. If we want to move up a directory we use `cd ..` and if we want to move into a directory we specify the name of the directory we are moving into. For example, if you are in your home directory and type `cd Desktop`, you should move into your Desktop directory.

We just mentioned that you can type `cd` followed by a directory or path. But what is a path? Let's learn some more vocabulary:

#### Absolute Paths vs Relative Paths

A path is simply the way to reach a file or folder; it's like an address for the file or folder you're trying to reach. When we specify a path starting from the root directory `/`, we call that an absolute path. For example, if I am currently in the `~` home directory and I would like to change directories into my Desktop folder, I can do that in two of the following ways:

1. `cd Desktop` - relative to where I am currently
2. `cd /Users/eschoppik/Desktop` - absolute, starting from the root (first `/`, then `Users`, then `eschoppik`, then `Desktop`)

**Questions to Answer**

* What is the difference between `/` and `~`? What do we call each of these directories?
* What command do we use to change directories?
* What is the difference between an absolute and relative path?



### { Working with Files and Folders. }

#### Objectives

By the end of this chapter, you should be able to:

* Create files and folders in Terminal using `mkdir` and `touch`
* Move files and folders in Terminal using `mv`
* Copy files and folders in Terminal using `cp`
* Remove files and folders in Terminal using `rm` and `rmdir`
* Explain what a flag is in Terminal
* Explain what the following commands do: `whoami`, `pwd`, `cat`, `echo`, `less`, `open`



| Linux/Mac | Windows                 | Description                                       |
| --------- | ----------------------- | ------------------------------------------------- |
| `cp`      | `copy`                  | copy a file from one location to another          |
| `mv`      | `rename`, `ren`, `move` | moves a file to a new location, or renames a file |
| `rm`      | `del`                   | remove (= delete) a file                          |
| `mkdir`   | `md`                    | create a new directory                            |
| `rmdir`   | `rd`, `rmdir`           | remove a directory                                |



#### Creating Files And Folders

Now that we have a good understanding of how to change directories and navigate in Terminal, let's see how we can create our own folders and files. To create a folder we use the `mkdir` command (short for "make directory"), followed by the name (or space-separated names) of the folder(s) that we would like to create. So let's head over to our `Desktop` and create a new folder called `first_folder`.

```
cd /Users/$USER/Desktop
mkdir first_folder
```

Whoa...you should be asking yourself, what is that `$USER` thing? It is an environment variable in your shell that keeps track of the current user of the shell. You can also see who `$USER` by typing `echo $USER` or by using the command `whoami`. Try out both methods of checking who the current user is.

As another side note, this tutorial will use absolute paths to navigate, just to make it easier for you to follow along. However, don't feel like you MUST use absolute paths over relative ones.

Now that we made the `first_folder`, how do we change directories into it? If you are thinking of the `cd` command, you're right! So let's `cd /Users/$USER/Desktop/first_folder`. Or, if you are already in your Desktop, you can just `cd first_folder`.

We just mentioned "if you are already in your Desktop." How do you know which directory you are in if you forget? Thankfully, there is a handy command called `pwd` which will display the absolute path and let you know what current directory you are working in. So if you are ever unsure, just type in `pwd` (which is short for _present working directory_).

Now that we are inside our new folder, `first_folder`, let's create a new file. A simple way to create a file is with the `touch` command. The `touch` command simply creates an empty file. Let's create a file called `first_file`: `touch /Users/$USER/Desktop/first_folder/first_file`. Alternatively, if you are currently in the `first_folder` directory, you can simple type `touch first_file`. Now use the `ls` command to verify that your file was created. `ls`, which is short for "list," will list all of the files and folders in your current directory.

#### Displaying Contents Of A File

A very common command to display the contents of a file is the `cat` command. If you type `cat NAME_OF_FILE` you can see the contents of the file easily, right there in Terminal. Try it out on the file you just created, `first_file`. You should see no output after pressing enter. There is no output because `first_file` is empty.

Let's add some text to the file so that we can use `cat`. Type:

`echo "Hello World" > first_file`

The `echo` command simply writes text to the terminal. The `>` is called a redirect. The `>` redirects the output from the command on the left side into the file on the right hand side. We will see more redirects in the next chapter.

Now try using `cat` on the file again. Do you see `Hello World`?

There are other ways of seeing the contents of a file in the terminal. Try using the command `less`: `less first_file`. `less` is a program that displays the contents of a file and allows the user to navigate up and down through the file or search for text in the file. To exit `less`, just press `q`.

#### Opening up a file

If you would like to open up a file, you can use the `open` command. So if we want to see the contents of `first_file` we can do `open first_file`. The `open` command is also very useful if you want to open all the files and folders in a directory (using your operating system's user interface). Try typing in `open .` and see what happens! If you are on Windows, the command to do this is `start NAME_OF_FILE`

#### Moving Files And Folders

Now that you understand how to create files and folders, let's move onto another essential operation: moving and copying folders. To move files and folders we use the `mv` command. Let's try this out!

Head back to the Desktop by typing in `cd ~/Desktop` and let's make a new file called `test.txt` (remember that command? If not - stop reading and go through the previous section again). Now on your Desktop you should have a folder called `first_folder` and a file called `test.txt`. Our goal is to move `test.txt` inside of `first_folder` - let's do that using the `mv` command. First make sure you are in the Desktop (type `pwd` to be sure), type `mv test.txt first_folder/test.txt`, and press enter.

Did it work? You shouldn't see any kind of success message or confirmation from Terminal, but you also should not see an error. This is very common when working with Terminal: you will see error messages if a command is incorrect, but very rarely see a success message. In other words, no news is good news. In this case, to make sure we did the correct thing, let's `cd` into `first_folder` and type in `ls`. We should see `test.txt` inside of `first_folder`.

#### Copying Files and Folders

Sometimes you may want to make a copy of a file or a folder. To copy a file, we use the `cp` command (short for copy). The general syntax looks like this:

```
cp PATH_TO_ORIGINAL_FILE PATH_TO_COPIED_FILE
```

For example, if we wanted to create a copy of `test.txt` and call it `test_copy.txt`, we could enter the following command (assuming we're inside of `first_folder`:

```
cp test.txt test_copy.txt
```

If you list all of the files in `first_folder`, you should now see three text files.

What if you want to copy an entire directory of files? Try moving up a directory from `first_folder`, and then type `cp first_folder first_folder_copy`. Uh oh! You should see an error: `cp: questions_copy is a directory (not copied).`

In order to copy a directory, you need to modify the `cp` command as follows:

```
cp -r first_folder first_folder_copy
```

The `-r` is called a _flag_; you can think of a flag for a command as an option that can be passed to that command. To learn more about the flags that you can pass to `cp`, you can type `man cp` (`man` is short for manual, on Windows this command is `--help`) and use the arrow keys to move up and down. When you're finished, press `q` to quit.

#### Deleting Files And Folders

Alright, enough with all of these files and folders, let's get rid of them. Make sure you are inside the `first_folder` and type `rm test.txt`. Once again, you shouldn't see much of a response from the terminal, so run a quick `ls` to make sure that the file is removed. Now that it is gone... where did it go? The Trash? The answer is it is completely removed from your computer. There is no confirmation or undo so be **VERY** careful when using the `rm` command. After you have removed this file, go ahead and remove the copied file as well. Finally, remove `first_file`. Now that the `first_folder` is empty, let's move up a directory and remove the `first_folder` directory itself.

Here you may run into a problem. If you try to use `rm` on a directory, you will see this message: `rm: first_folder: is a directory`. It turns out that `rm` is for a file, while the command `rmdir` is used to remove (empty) directories. So, let's use the `rmdir` command to remove `first_folder`. Make sure that there is nothing else inside that folder, or else you will see a message that looks like this: `rmdir: first_folder: Directory not empty`.

If there is anything inside the folder, you will have to use `rm -rf first_folder`. Like we saw with `cp`, the `r` and `f` in `-rf` are examples of flags. How can you learn more about the flags for `rm`? Go ahead and remove the `first_folder_copy` directory using `rm -rf`.

**Exercises**

1. Create a file called `name.txt`.
2. Try renaming the file to `rename.txt` using the `mv` command. What does this tell you about the command?
3. Using the `cp` command, make a copy of `rename.txt` and call it `copy.txt`.
4. Remove the file `copy.txt`.
5. Create a folder called `questions`.
6. Change directories to the `questions` folder.
7. Create a file called `first.txt`.
8. Create a file called `second.txt`.
9. Go back a directory and make a copy of the questions folder and call it `questions_copy`.
10. When using `cp -r` what is the `-r` called? What does it do?
11. Delete the original `questions` folder and the copy.



### { Listing Files and Flags. }

#### Objectives

By the end of this chapter, you should be able to:

* Understand what the `ls` command does
* Define flags and describe how the syntax works
* List files using flags

#### Listing Files

As you saw in the previous chapter, one of the most important commands you are going to be using is `ls`, which lists the contents of a directory. If you type `ls` in a directory you will see all sorts of content. For example, typing `ls` in your home directory will show you all of the files and folders inside of that directory. Typically your home directory contains folders such as `Desktop`, `Documents`, `Downloads`, `Music`, `Pictures`, etc.

Sometimes the default `ls` command does not give us all the information we want. In such cases, we'll need to add some flags to get more details.

#### Flags

In the previous chapter, we saw how flags could be used to modify the behavior of `cp` and `rm`. Flags can change and even enhance commands and are added using a `-` after the command. Flags are usually represented by single uppercase and lowercase letters. With the `ls` command, we can pass in the `-a` flag to list "all" files (including hidden files and folders). If we want the `ls` command to give us more information about each file, we can pass in the `-l` flag. To combine flags we can just use one `-` and pass in each flag. So the command to use `ls` and show all files and more detailed information about each one would be `ls -la`.

Using flags for `ls` will be essential when working with permissions as well as when you start working with `git`. We will also see many other terminal commands which accept flags later in this course.



## { Terminal Basics Exercises. }

Write the following terminal commands to perform the following tasks:

#### Part I

1. make a directory called `first`
2. change directory to the `first` folder
3. create a file called `person.txt`
4. change the name of `person.txt` to `another.txt`
5. make a copy of the `another.txt` file and call it `copy.txt`
6. remove the `copy.txt` file
7. make a copy of the `first` folder and call it `second`
8. delete the `second` folder

#### Part II

1. What does the `man` command do? Type in `man rm`. How do you scroll and get out?
2. Look at the `man` page for `ls`. What does the `-l` flag do? What does the `-a` flag do?
3. Type the following command to download and save the contents of google.com: `curl https://www.google.com > google.html`
4. Use `less` to look at the contents of `google.html`.
5. Look at the `man` page for less. Read the section on `/pattern`. Search for the text **hplogo** in the `google.html` file.
6. How do you jump between words in the terminal?
7. How do you get to the end of a line in terminal?
8. How do you move your cursor to the beginning in terminal?
9. How do you delete a word (without pressing backspace multiple times) in terminal?
10. What is the difference between a terminal and shell?
11. What is an absolute path?
12. What is an relative path?
13. What is a flag? Give three examples of flags you have used.
14. What do the `r` and `f` flags do with the `rm` command?





## Intermediate Level



### { Permissions and Links. }

#### Objectives

By the end of this chapter, you should be able to:

* Determine the permissions set for a file or a directory
* Manage and change permissions using `chmod`
* Manage and change users and groups using `chown` and `chgrp`
* Explain what `root` is, and the relationship between `root` and `sudo`
* Create links in the file system using the `ln` command
* Explain the difference between a hard and a symbolic link

#### Introduction

When you're working in Terminal, you may sometimes find that you're not allowed to do things you want to do. Maybe you're trying to install something, or move a file from one directory to another, and you get an error telling you something along the lines of "permission denied." These sorts of permissions errors are extremely common, so understanding how to deal with them is important. That's what we'll learn how to in this chapter.

#### Users and Groups

Before you learn about permissions, you first need to understand users and groups. Let's take a look at an example. Head to your home directory and list everything using the `ls -lah` command. (Not sure what the `h` flag does? Check the manual!)

The output you get might look something like this:

![](<../../../../.gitbook/assets/image (151).png>)

The details of these files aren't important. What you should see is a bunch of rows of output, one row for each file or directory. Let's figure out what all of this actually means. For instance, here is the line for the `.bashrc` file from the above screen shot:

`-rwxr-xr-x 1 eschoppik staff 67B Aug 29 2014 .bashrc`

The third column specifies the username of the user that owns the file. In this case, `eschoppik` is the owner of the file. The fourth column specifies the name of the group associated with the file. In this case the group `staff` is associated with the file.

In most Mac systems, users are also members of the `staff` group. To see which groups you are a member of, type the `groups` command in Terminal. The `staff` group will likely be one of the many groups you are in. As we will see next, permissions can be set for the owner of the file, a user that is in a group associated with the file, or a user that is neither the owner nor a member of the associated group.

#### Permissions

Let's take a look at that `.bashrc` line again:

`-rwxr-xr-x 1 eschoppik staff 67B Aug 29 2014 .bashrc`

We've already talked about the third and fourth columns in this output. Now let's talk about the first column. The `-rwxr-xr-x` refers to _permissions_ of the `.bashrc` file. Each character of the permissions string, `-rwxr-xr-x` describes something about the file's permisisons. But what are permissions? A file's permissions is a set of rules that describes which operations a user can or cannot perform on a file or folder. There are 3 types of operations that can be allowed or not allowed:

* `r` - reading the file
* `w` - writing to the file
* `x` - executing the file (we will go into this in more detail soon)

You may be asking at this point, why is the permissions string so long if there are only 3 operations that can be specified? Well, a permissions string describes different types of users that can or cannot perform read, write and execute operations. You may be one of 3 different types of users:

1. The owner of the file.
2. Not the owner, but a member of a group associated with the file.
3. Other. Not an owner and not in a group that is associated with the file

So a permissions string specifies the permissions for all 3 types of users plus an extra character to specify the type (file, folder, etc).

Here is how the above permissions string breaks down:

![](<../../../../.gitbook/assets/image (185).png>)

In other words, this string says that `.bashrc` is a file, that the owner of the file can read, write, and execute, users in the group can only read and execute, and other users can only read and execute as well.

#### Changing Permissions

To change the permissions of a file we use the `chmod` command. For each set of permissions (owner, group, everyone) we can assign a number from 0 to 7. This is called **octal** (base-8) notation. Here's a table that illustrates what each number means.

| Number | Permission              | `rwx` (display in terminal) |
| ------ | ----------------------- | --------------------------- |
| 0      | none                    | `---`                       |
| 1      | execute                 | `--x`                       |
| 2      | write only              | `-w-`                       |
| 3      | write and execute       | `-wx`                       |
| 4      | read only               | `r--`                       |
| 5      | read and execute        | `r-x`                       |
| 6      | read and write          | `rw-`                       |
| 7      | read, write and execute | `rwx`                       |

So if we want to change a file so that only the owner and group can read, write, and execute, we would type `chmod 770 somefile.txt`.

If you'd like to be a bit more specific, you can also set permissions using what's called **symbolic** notation. Here's an example of what that looks like:

```
chmod ug+rwx,o-rwx hi.txt
```

This is saying "add read, write, and execute permissions to the **u**ser and the **g**roup, and remove read, write, and execute permissions from **o**ther." While a bit more verbose, it's also a little more descriptive. To see more examples of symbolic notation, check out [this](https://askubuntu.com/questions/518259/understanding-chmod-symbolic-notation-and-use-of-octal) article.

If we want to change permissions for a folder, we need to add the `-R` flag: `chmod -R 755 some_folder`.

You can read more about `chmod` [here](https://en.wikipedia.org/wiki/Chmod).

#### Executable Files and Folders

Now let's talk a little bit more about what the `x` (executable) means for a file or a folder's permissions. If you have executable permissions on a folder, it means that you can cd into it. See what happens with the following commands:

```
mkdir test_folder
cd test_folder
cd ..
chmod 666 test_folder
cd test_folder
```

You should see an error saying permission denied. Add the execute permission back to the folder, and then remove the folder.

Now onto executable files. When a file is executable, it can be run from your shell as if it were a program. Let's first create our file. Type the following in your terminal:

```
echo ls > test.sh
echo pwd >> test.sh
echo pushd . >> test.sh
echo "cd ~" >> test.sh
echo "pwd" >> test.sh
echo popd >> test.sh
cat test.sh
```

The `test.sh` file should look like the following now:

```
ls
pwd
pushd .
cd ~
pwd
popd
```

(Did you notice that our first `echo` command used a single arrow (`>`), while the other commands used two? We'll explore the difference between these two operators in the next chapter!)

Now let's make the file executable and run it. Use chmod to make it executable: `chmod 755 test.sh`. Next, execute the file by providing a path to the file. In our case, the file is in the current directory, so to execute it, we do the following: `./test.sh`. We just made our first executable shell script!

#### chown and chgrp

Now that we have a clearer understanding of users, groups and permissions, let's take a look at the line from `ls -lah` again:

`-rwxr-xr-x 1 eschoppik staff 67B Aug 29 2014 .bashrc`

* The `1` refers to the number of files (this will always be 1 for files)
* `eschoppik` is the "owner"
* `staff` is the group
* `67B` is the size of the file
* `Aug 29 2014` is the last day the file was modified
* `.bashrc` is the name of the file

So what if we don't want `eschoppik` as the owner of the file any longer? Or what if we want a different group to own that file? We can use one of the following commands:

`chown anotheruser:anothergroup .bashrc`

Or if we just want to change the group:

`chgrp anothergroup .zshrc`.

Now let's take a look at this line from the `ls -lah` command:

`drwxr-xr-x 6 root admin 204B Oct 20 2015 ..`

The other file said `eschoppik` for user and `staff` for group, but this one says `root` and `admin`. We can also see that this is a directory because it starts with a `d` before listing the permissions. So what is the `root` user?

#### root user and sudo

The `root` user is a special user on your computer that has the power to do anything it wants. It can change permissions on any file, delete anything it wants, etc. When you see `root` as the owner, and you want to make a change to that file, you have to use a command called `sudo`. The `sudo` command gives you the powers of the `root` user for just one command and will ask you for your password in order to preform the command. Try out commands with sudo. Create a file called `somefile.txt`. Then make the owner the root user:

`sudo chown root somefile.txt`

Now try to delete the file without using sudo. You are not allowed. Look at the permissions. Why is this not allowed?

#### Links

Since we have files and folders located all over our file system, it becomes difficult to identify where many of these are located. Fortunately, we can create a link (also known as an alias) to a file or folder using the `ln` command. The structure looks like this:

`ln path_to_link name_of_link`

There are two kinds of links we can make, hard and symbolic links - let's see how they work!

#### Hard Links

Let's create a file called `learn.txt` in our `Desktop` folder (type in `cd /Users/$USER/Desktop` if you need to get there). We can open up our `learn.txt` file using `open learn.txt` and let's add the text "Learning about links!".

Now let's create a link to this file! We can call our link `first_link`. To do this we use the `ln` command and type `ln learn.txt first_link`. Now if we `cat first_link` we should see the output "Learning about links!".

If we decide to move our `learn.txt` file anywhere we still have a link to it through `first_link`! Pretty awesome!

If we decided to delete our `learn.txt` file, what happens to our hard link? Let's `rm learn.txt` and then `cat first_link`. We still see that we have a link! This might seem strange; shouldn't a link be broken if a file is removed? Not with hard links! You can think of a hard link like a direct copy of a file. If the file is removed, the link still exists.

#### Symbolic Links

We saw that when we remove the original file, any hard links still remain and contain the entire source file. This is usually not what we want, since we usually want a reference to some file and not a direct copy. To create a reference instead of a copy, let's make a symbolic link.

To create a symbolic link, we use the `-s` flag when creating a link. Let's create a new file called `learn_again.txt` and then create a symbolic link using `ln -s learn_again.txt first_sym_link`. If we `cat first_sym_link` we do not get any errors! But if we delete or move `learn_again.txt`, our `first_sym_link` will be broken!

We can also use symbolic links for folders as well, which makes it very useful if we need to access a folder but do not remember the path. However, if your original file/folder path changes or is removed , the symbolic link **will** break!



### { Redirection. }

#### Objectives

By the end of this chapter, you should be able to:

* Explain what redirection is
* Explain the difference between `>`, `>>`, and `<`
* Use redirection to work more effectively in Terminal

#### Redirection

Sometimes instead of simply displaying the output from a command to the terminal, it's useful to take the result output of a command and send it somewhere else. We call this "redirection" and it is denoted by `>>` or `>`. Let's start with a simple example using the `echo` command.

The `echo` command is useful for displaying text to the terminal, but many times it is more useful to take that text and redirect it to a file. In Terminal, type the command `echo Hello World > hello.txt`. Then, using the `cat` command, let's see what we just did by typing `cat hello.txt`. All we did here is take the text "Hello World" and instead of displaying it to the terminal, we sent it to a file called `hello.txt`!

Run the same command again but with slightly different text: `echo Hello Universe > hello.txt`. Now cat the file again. Notice that your new text completely overwrote the old text: you should see that "Hello World" has been replaced by "Hello Universe." In other words, when you use `>`, whatever text you're echoing into the file will completely overwrite any text that might already be in the file.

Maybe this is what you want, but maybe not. What if you're trying to append some text to the end of the file, rather than overwriting the text? In this case, use `>>` instead. Try it out: `echo Hello World >> hello.txt`. Now cat the file. You should see the following:

```
Hello Universe
Hello World
```

One very common use case for redirection is to put small pieces of text in a file. Instead of opening a text editor, typing in some text, saving it and closing the file we can do this all in one step.

#### Redirection with Input

So far we have seen redirection using `>` and `>>`. These arrows indicate redirection with standard output (take something and output it to something else). However, we can also use redirection with input as well using the `<` arrow. Let's use a command called `sort`, which sorts a file alphabetically. Imagine we have a file called `names.txt` with the following names:

```
Bob
Tom
Jim
Amy
```

If we want to sort this file, we can type `sort names.txt` and it will output

```
Amy
Bob
Jim
Tom
```

Now what if we want to take the contents of `names.txt`, redirect that to the `sort` command, and then send _that_ output to a file called `sorted.txt`? The redirection will look like this: `sort < names.txt > sorted.txt`. This will now create a new file called `sorted.txt` with the names sorted alphabetically!

This might seem a bit strange, but try typing these commands and see what information you can output and redirect. As we see right now, we are only using the `sort` command, but what would happen if we wanted to use other commands along with sort? We would somehow need to connect each of these commands together. We connect these commands together through something called "pipes."



### { Piping. }

#### Objectives

By the end of this chapter, you should be able to:

* Explain what the `head`, `tail`, `sort`, `uniq`, `wc` and `grep` commands do
* Define what piping is
* Understand use cases for piping
* Use piping to better work in Terminal

#### Piping

At the end of the last chapter, we saw how we could use redirection to combine a couple of commands into one. In that case, in a single line we were able to both sort a text file and output the contents to a new file.

But what if we want to chain even more commands together? This is where piping comes into play. Before we learn about piping, though, let's learn/review a couple other terminal commands.

`head` - display the first lines of a file (using the `-n` flag we can specify the number of lines)

`tail` - display the last lines of a file (using the `-n` flag we can specify the number of lines)

`sort` - sort lines of a text file

`uniq` - removes duplicated lines (your data **must** be sorted for this to work)

`wc` - word, line, character and byte count

Now let's create two files - `first.txt` which contains the text

```
First
Second
Third
```

And `second.txt` which contains:

```
Fourth
Fifth
Sixth
```

If we want to concatenate (join) these two files together, we use the `cat` command:

`cat first.txt second.txt` (make sure the files and commands are separated by a space).

But what happens if we want to concatenate these two files and then find the word count? What if we want to concatenate and then sort it? This is where we need piping! You can think of a pipe as a connection between the output of one command into the input of another command. So once we concatenate two files we then want to send (or pipe) the result of that to another command. We can even combine this with redirection!

To pipe a command we use the `|` character. So if we want to pipe `cat` into `sort` it would look like this:

`cat first.txt second.txt | sort` or `cat first.txt second.txt | sort | head -n 2`

Take a look at this command and try to figure out what it's doing. You'll find a step-by-step answer below.

`cat first.txt second.txt | sort | tail -n 3 | head -n 1`

1. Concatenate the two files first.txt and second.txt
2. Sort the results
3. Find the last 3 lines
4. Find the first line of those last 3 lines

This is how we can find the third from last line in a file (without knowing how many lines the file has).

#### `grep`

Let's examine another useful command called `grep` which is extremely powerful for finding text. On its own it is helpful, but it is quite useful when piped with `cat`. Let's try a simple example with `cat first.txt | grep First` - what do you see?

You should see the word `First` output to the terminal. This is because `grep` searched the file for the text `First` and found a match!

Notice that if `grep` doesn't find a match, it won't output anything. If it finds multiple matches, it will print them all. Try out these commands and see what `grep` returns to you!

```
cat first.txt second.txt | grep Nope
cat first.txt second.txt | grep th
```

Let's look at another example. Imagine you have a file called `petnames.txt`, and inside you have the following list of names:

```
Lassie
Moxie
Whiskey
Fido
Lassie
Moxie
```

We see here there are quite a few duplicates, so let's try to use the `uniq` command to remove these duplicate names. The problem is, when we run `uniq petnames.txt` we get the following

```
Lassie
Moxie
Whiskey
Fido
Lassie
Moxie
```

If we look back at our definition of how the `uniq` command works, we see that our data must be sorted! So how can we first use `sort` on `petnames.txt` then attach the `uniq` command? Piping to the rescue!

`sort petnames.txt | uniq` gives us

```
Fido
Lassie
Moxie
Whiskey
```

This looks great! But this text is just being output to the terminal, what if we want to output this text to a new file called `petnames_sorted.txt`? We can combine piping with redirection and use `sort petnames.txt | uniq > petnames_sorted.txt`. Now if we `cat petnames_sorted.txt` we should see our four unique sorted names!



## { Permissions, Redirection, and Piping Exercise. }

#### Part I (Permissions and links)

Write terminal commands to do the following:

1. Create a file called `restricted.txt`.
2. Change the permissions on the `restricted.txt` file to allow the owner to read and write to the `restricted.txt` file. Do this using the **Octal** Notation.
3. Change the permissions on the `restricted.txt` file to only allow the owner, group and everyone to read and write and execute the `restricted.txt` file. Do this using the **Symbolic** notation.
4. Create a folder called `secret_files`. Inside the `secret_files` folder create a file called `first_secret.txt` and another folder called `classified`. Inside of the `classified` folder create a file called `super_secret.txt`.
5. Change the permissions on the secret\_files to only allow the owner and group to read, write and execute in all the files and folders inside of secret\_files. Do this using the Octal Notation.
6. Create a hard link for the `restricted.txt` called `hard_link`.
7. Create a symbolic link for the `classified` folder called `classified_link`.

#### Part II (Piping and Redirection)

For the following exercises, create a text file called `vegetables.txt` with the following text:

```
Lettuce
Amaranth
Beet
Celery
Kale
Dill
Cabbage
Broccoli
Lettuce
Amaranth
Beet
Spinach
Chard
Broccoli
Cabbage
Dill
```

Write the following terminal commands to do the following

1. Sort `vegetables.txt`.
2. Count the number of lines in `vegetables.txt`.
3. Create a file called vegetables\_sorted.txt which contains all the unique vegetables sorted in ascending order in vegetables.txt (do this without the touch command).
4. Create a file called `last_three.txt` which contains the last three vegetables in the `vegetables.txt` file (do this without the `touch` command).
5. Count the number of lines the word "Broccoli" appears on (using `wc` and `grep`).





## Development Tools

#### Visual Studio Code

Visual Studio Code or VS Code is an IDE. IDE stands for Integrated Development Environment. It is the software that you will be using to write most of your code. It is designed to help you develop your apps quickly, focusing on the problems that you need to solve instead of having to search online for minor details.

**Auto-complete**

One of the most important features of an IDE is that it provides _auto-completion_. This means that it will give you suggestions of what you can write next, while you are typing something.

For example, when writing a CSS property, VSC will tell you what values you can assign to this property.

![](<../../../../.gitbook/assets/image (166).png>)

**File tree view**

The reason why we call an IDE _integrated_ is that you almost don't need to leave the window when you are write your code. For example, creating, renaming and moving files can be done directly from the IDE. This functionality can be achieved from something called a **tree view**. You can find this view on the left side of your IDE.

![](<../../../../.gitbook/assets/image (177).png>)

**Finding files**

When working with big projects, you will often need to find a file quickly, without having to go through the tree view manually.

![](<../../../../.gitbook/assets/image (198).png>)

**Enable formatting on save**

To automatically give your code the right format:

* In Visual Studio open the settings file (see [https://code.visualstudio.com/docs/getstarted/settings#\_creating-user-and-workspace-settings](https://code.visualstudio.com/docs/getstarted/settings#\_creating-user-and-workspace-settings))
* Search for `editor format`
* Set `editor.formatOnSave` and `editor.formatOnPaste` to `true`

### { OPTIONAL } Visual Studio Code Extensions For Web Development

Visual studio code offers a wide range of extensions. Here is how to install the extension.

Press **SHIFT+COMMAND (or Windows)+X** or just click on the extension icon of visual studio code. Search for the extension and press install

![](<../../../../.gitbook/assets/image (88).png>)

Here are some visual studio code extensions for web development. The choices of the extension are ones personal opinion.

#### 1: Javascript (ES6) Code Snippets

No need to mention that JavaScript is the core of web development. There are lots of code snippets that we used on a daily basis and this extension helps you by not writing that repetitive code again and again.

It provides JavaScript, TypeScript, Vue, React, and HTML code snippets. This is a must-have extension for web development.

Link: [https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)

You can install it by searching the name on the extension section of the visual studio code.

#### 2: CSS Peek

As its name suggests, this extension lets you jump to the CSS code using classes and IDs.

Link: [https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)

You can install it by searching the name on the extension section of the visual studio code.

#### 3: Auto Close Tag

This extension automatically adds the closing tag of HTML and XML.

Link:[ https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

You can install it by searching the name on the extension section of the visual studio code.

#### 4: ESLint

ESLint is the linting utility for JavaScript. It checks your code for common errors and lets you know in the editor itself. It’s like a virtual peer who is validating your code while you are writing it.

Link:[ https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

You can install it by searching the name on the extension section of the visual studio code.

Before installing ESLint in visual studio, install it as a global package first. `npm install -g eslint`

#### 5: Prettier – Code formatter

This extension performs the formatting of the JavaScript, CSS, and HTML code.

Link: [https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

You can install it by searching the name on the extension section of the visual studio code.

#### 6: Path Intellisense

Importing code from other files is what everyone does on a daily basis. This extension makes the development time faster by autocompleting file names.

You type the name of the file in statements and it will search and give you suggestions.

Link: [https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

You can install it by searching the name on the extension section of the visual studio code.

#### 7: GitLens

We use Git almost every day of our life. GitLens is the visual studio code plugin to supercharge git capabilities.

With GitLens, it’s so easy to view code authorship, check commit number, view changes between the last commit and existing changes, and so on

Link: [https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)\
You can install it by searching the name on the extension section of the visual studio code.

#### 8: Project Manager

Do you work on multiple projects and switch back and forth? I know I do and the project manager has been a savior to manage multiple projects in visual studio code

Link: [https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

You can install it by searching the name on the extension section of the visual studio code.

#### 9: Live Server

Live Server extension provides the live preview of your web application right within the editor.

This is very handy and useful for the front end developers.

Link:[ https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)\
You can install it by searching the name on the extension section of the visual studio code.

#### 10: Debugger for Chrome

This extension brought the powerful chrome debugger right into the visual studio code.

It is very useful for front-end developers to perform the testing and debugging.

Link: [https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)\
You can install it by searching the name on the extension section of the visual studio code.

#### 11: Better Comments

This extension helps you to create more human-friendly and easy-to-read comments

Link: [https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)\
You can install it by searching the name on the extension section of the visual studio code.

#### 12: Code time

This extension tracks your development time and provides you with useful stats such as how many hours you have code today etc.

It’s pretty useful to keep track and see the progress. This is not strictly for web development only, anyone can use this extension.

Link: [https://marketplace.visualstudio.com/items?itemName=softwaredotcom.swdc-vscode](https://marketplace.visualstudio.com/items?itemName=softwaredotcom.swdc-vscode)\
You can install it by searching the name on the extension section of the visual studio code.

#### 13: Settings Sync

I use a different machine for my work and personal use. I use visual studio code in both machines, however, I don’t want to repeat the same steps to configure the editor every time.

Enters Setting Sync extension. It creates and stores your configuration in Github gist and synchronizes wherever you want. Simple and awesome!

Link: [https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)\
You can install it by searching the name on the extension section of the visual studio code.



## **More Resources**

* [Tutorial: Terminal for Beginners!](https://medium.com/@grace.m.nolan/terminal-for-beginners-e492ba10902a)
* [Basic commands tutorial 10 mins](https://youtu.be/vhZLTp6N4XA)
* [Intro to Ubuntu and useful command tutorial 45 mins](https://youtu.be/KSh9-6FIu1w)



It's alright if you get stuck or if something doesn't look right! When that happens, please ask your teachers or classmates for help in Slack, or use the **#support-coding** channel.







{% hint style="info" %}
**Everything below is optional and not a requirement of our course. Students who like to challenge themselves can continue with the Advanced Level.**
{% endhint %}

## Advanced Level - 1  { OPTIONAL }

### { Terminal Environment. }

#### Objectives:

By the end of this chapter, you should be able to:

* Describe what a terminal environment is
* Create and modify terminal environment variables, including the `PATH`
* Save environment variables to a configuration file

#### What is your terminal's environment?

A terminal's environment is a list of settings that can be referenced by programs. To see what your terminal's environment looks like right now, try typing `env` in your terminal. You should see output similar to the following:

```
rvm_bin_path=/Users/tim/.rvm/bin
TERM_PROGRAM=Apple_Terminal
GEM_HOME=/Users/tim/.rvm/gems/ruby-2.3.1
TERM=xterm-256color
SHELL=/bin/bash
CLICOLOR=1
IRBRC=/Users/tim/.rvm/rubies/ruby-2.3.1/.irbrc
TMPDIR=/var/folders/5s/zstwqxy52pl_lq_lr3b5v7nc0000gn/T/
Apple_PubSub_Socket_Render=/private/tmp/com.apple.launchd.Q7TcyOvK4P/Render
TERM_PROGRAM_VERSION=361.1
OLDPWD=/Users/tim
TERM_SESSION_ID=281162A1-5C58-4285-9A35-AC9306923C34
USER=tim
__CF_USER_TEXT_ENCODING=0x1F5:0x0:0x0
LSCOLORS=GxFxCxDxBxegedabagaced
PATH=/usr/local/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/tim/.rvm/bin
PWD=/Users/tim/Projects/Rithm/prework
.
.
.

```

Each word on the left side of the equal sign is called an **environment variable**. The value on the right side is the value of the variable.

#### Using environment variables

In the terminal, you can see what value an environment variable has by using `echo`. When referencing an environment variable, you must use the `$` as a prefix. In other words, to print the value for the environment variable `PWD`, the command would be:

```
echo $PWD
```

Try that in your terminal. You should get the same output as the output for the command `pwd`.

#### Creating environment variables

Now let's make our own environment variable. Go to your home directory and create a folder called `Projects`. Now let's make an environment variable called `PROJDIR` (environment variables are usually all caps) that keeps track of the path to your projects directory. To create an environment variable, you can use the `export` command. On a Mac or Linux machine, the command would be:

```
export PROJDIR=/Users/tim/Projects
```

Notice that the `$` isn't being used in this case. When you define an environment variable, you do not use the `$`. Only use the `$` when you want to reference the value of the variable.

Now that you've created the environment variable, let's use it:

```
cd ~
cd $PROJDIR
```

You should now be in your project directory.

So now we have a great way of saving a useful variable in our terminal's environment, but we have a problem. Every time you close your terminal window, the environmet variables get reset, so the `PROJDIR` environment variable will be lost! How do we fix that?

#### Saving environment variables

Now that we know how to create environment variables, we need to learn how to save them so that every time we open a new terminal window, we have those environment variables set. To save environment variables, you need to modify the shell configuration file in your home directory. This file is different depending on what your default shell is. If you are using oh-my-zsh, then your configuration file will be called `.zshrc`; if you are using bash, then your configuration file will be called `.bash_profile`.

Open the configuration file for your shell, either `.zshrc` or `.bash_profile`. Next, add the following line to your file:

```
export PROJDIR=/Users/$USER/Projects
```

Save the file, quit out of all terminal windows, and then open terminal again. Try executing `echo $PROJDIR`. You should see the path to your projects directory.

We did one other interesting thing here. Rather than using a hard coded path to the projects directory, we used another environment variable to figure out the correct user name. Try typing `echo $USER` in your terminal. You should see your user name. The important takeaway here is that an environment variable can be defined using other environment variables. For example, if we had a `python` folder inside of the `Projects` directory, we may want a variable for that as well. We could definite it like the following way:

```
export PYTHON_PROJ=/Users/$USER/Projects/python
```

Or we could use the `PROJDIR` environment variable that we already have set:

```
export PYTHON_DIR=$PROJDIR/python
```

The only catch is that the line for exporting `PROJDIR` must come before the line using `PROJDIR`. Otherwise, `PROJDIR` will not yet be defined when we use it in the `PYTHON_DIR` definition.

#### The `PATH` environment variable

An important environment variable to know and understand is the `PATH`. Your terminal uses the `PATH` environment variable to find programs to execute. Try the following in a new terminal window:

```
export PATH=
```

Now try using `ls` in the terminal. It doesn't work! Try a few other commands like `man` or `chgrp`. None of them work. That's because commands like `ls` are just programs stored in a file somewhere in your filesystem. The reason we don't normally need to give the full path to the `ls` command when we use it is because `ls` is a file found in one of the folders that are specified on the path.

Open a fresh terminal window. The `ls` command should be working again. Now use the `which` command to see where on the path `ls` is coming from:

```
which ls
```

Typically, the `ls` command is located in the `/bin` directory (though if you're using oh-my-zsh, the command may be aliased to `ls -G`). Let's change our `PATH` environment variable again, but this time, let's assign it to `/bin`:

```
export PATH=/bin
```

Now try to use the ls command. It should still work! That's because `ls` can now be found in one of the folders of the `PATH`, specifically in `/bin`. Other commands still don't work however. The `man` command still isn't working because it is not found on the `PATH`. Let's add a few more directories to the `PATH` in the same terminal window. We want to add `/usr/bin`, `/usr/sbin`, and `/sbin`, but we don't want to rewrite the `PATH` variable completely. Instead, let's add to the `PATH` that already exists. In order to do that, we reference the `PATH` environment variable using the `$` and separate multiple paths using a colon:

```
export PATH=$PATH:/usr/bin:/usr/sbin:/sbin
```

Now if you do `echo $PATH`, you should see the following output:

```
/bin:/usr/bin:/usr/sbin:/sbin
```

And commands like `man` should work. Now that you understand the `PATH`, close the terminal window and open a fresh window, so that your `PATH` will be set up correctly.



### { Processes. }

#### Objectives

By the end of this chapter, you should be able to:

* Define what a process is
* Examine processes that are running on your machine
* Kill a process using the `kill` command

#### What is a process?

A process is a program on your computer that is being run. For example, when you have Google's chrome browser open, that is a process running on your machine. An email application, a terminal window, and even the `ls` command are also processes when they are being executed on your machine.

The nice thing about processes is that the operating system ensures that all of the memory for one process cannot be accessed by another process. In other words, if one process crashes, it should not have any effect on the rest of the system.

But how can you tell which processes are running at any given time? And how can you stop a process from the terminal?

#### `ps`

The `ps` command is a useful tool for seeing which processes are running on your machine. You can execute the command `ps` on its own, but more commonly you'll see the command `ps aux` being used. The `a` indicates that you're interested in all processes, not just process for your current user; `u` ensures that the process owner will be displayed; finally, specifying `x` makes sure that you'll see a list of all active processes, not just those attached to a terminal.

(Note: you may be wondering why the command is `ps aux`, and not `ps -aux`. For some history on the command, check out [this](https://stackoverflow.com/questions/15102576/ps-aux-works-but-ps-aux-doesnt) Stack Overflow question.)

Try typing `ps aux` in your terminal and see what you get. You should see something similar to this:

```
USER   PID  %CPU %MEM      VSZ    RSS   TT  STAT STARTED      TIME COMMAND
tim  74874   8.3  1.7  3408348 139912   ??  S     3:34PM   6:39.74 /Applications/Google Chrome.app/Contents/Versions/53.0.2785.116/Google Chrome Helper.app/Contents
tim  74858   6.2  2.8  3224740 233060   ??  S     3:34PM   8:34.62 /Applications/Google Chrome.app/Contents/MacOS/Google Chrome
tim  61431   2.5  0.6  2698840  53728   ??  R     9:46AM   0:59.49 /Applications/Utilities/Terminal.app/Contents/MacOS/Terminal
```

Some important columns are `USER`, `PID`, and `COMMAND`. The USER column is the username of the user who executed the process. The PID column is a number that uniquely identifies the process. This PID will be useful very soon when we learn how to stop a process.

#### `kill`

At times you may have a process that for whatever reason is not responsive. In other words, the process continues to execute when you do not want it to. We can stop the process from running by using the `kill` command.

Let's try it out. First, open any file in terminal using the `less` command. The process will continue to run as long as you have not pressed `q` to quit. In a separate terminal window, type the following:

```
ps aux
```

Now scroll through the list until you find a process that is running that has been started by your username and whose command's path ends with less. Once you've identified the process, take note of the PID.

Next, to kill the process, type `kill` and then the PID and hit enter. For example, if your process looks like the following:

```
tim             10011   0.0  0.0  2434948    900 s000  S+    5:32PM   0:00.00 less readme.md
```

Then your PID is `10011`. So to kill less, your command would be the following:

```
kill 10011
```

After killing the process, you should see your terminal window that was running less go back to a normal terminal prompt.

#### `kill` vs. `kill -9`

Sometimes when you're reading tutorials and a process needs to be killed, you'll see that the command `kill -9` is executed, not `kill`. So what's the difference between these two?

Whenever you try to kill a process, a signal is sent to that process telling it to terminate. By default that signal is the `TERM` signal. However, if a program has crashed or is frozen for some reason, it's possible that it won't pick up on that signal and the process may not terminate. The -9 flag sends a different signal to the process: according to the manual for `kill`, -9 represents the `KILL` signal, which is a "non-catchable, non-ignorable kill." If killing a process doesn't work, try killing with -9 and see if that gets the job done.

For more on `kill` and the different signals you can send, check out [this](https://superuser.com/questions/107543/bash-man-page-kill-pid-vs-kill-9-pid) superuser question.



### { Finding Files and Folders. }

#### Objectives

By the end of this chapter, you should be able to:

* compare and contrast `find` and `grep`
* use `find` to search for files and folders
* use `grep` to search for patterns in a string or text
* define what a _regular expression_ is

#### `find`

One of the most useful terminal commands is the `find` command. When you know how to use it well, you can easily find files on your computer without using Spotlight, Alfred or any other GUI. Let's get started by learning how the syntax works.

To find a specific file in your current directory, you can simply type `find` and the name of the file. (If you try to find a folder you will find all of the contents inside as well.) For example, if try typing the following command from your home directory:

```
find Downloads
```

You should see a list of all your Downloads in the terminal.

To find something with a bit more complexity, use the following pattern

1. `find`
2. a filepath
3. an expression (this is where you have the most flexibility)

Let's `cd` into a folder called `views` and try this pattern to find anything with the name `first.txt` inside of the `views` folder:

`find . -name "first.txt"`

Now this is nice if we know exactly the name of the file we are looking for, but many times we need to use wildcard characters including `*`, `?` and `[]`. The difference between these characters is as follows:

`*` - any number of characters\
`?` - one character\
`[]` - any of the characters inside the brackets

Here are some more examples:

* find inside of the `views` folder (assume we are inside the views folder) anything that ends with `.html` => `find . -name "*.html"`
* find inside of the `views` folder (assume we are inside the views folder) anything that ends with a three letter file extension like `.txt` or `.css` => `find . -name "*.???"`
* find inside of the `views` folder (assume we are inside the views folder) anything that starts with the letter `f` `t` or `s` => `find . -name "[fts]*"`
* find inside of the `views` folder anything that has the text `main` somewhere in the filename (this could be the beginning as well) `find . -name "*main*"`

#### `grep`

Another extremely useful tool for finding information that we've seen before is `grep`. While `find` is for files and folders, `grep` is excellent for searching for specific values in a string or in a text file. If you type `grep` on its own, it's not that valuable because you need to make sure you pass a filename and text to it. You can also use `grep` with piping and `cat`.

We have already seen examples using `grep` with `cat` to find words like `cat people.txt | grep Elie` to find if the word Elie exists in the `people.txt` file. Let's use the file below which we will call `names.txt` as an example:

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
Matt
Liza
Janey
Jane
Shana
```

Let's add a little more onto our knowledge of `grep` and introduce some flags.

* `-i` for case insensitive search

`grep -i "elie" names.txt` => `Elie`

* `-w` for full word search

`grep -i "beth" names.txt`

```
Beth
Elizabeth
```

`grep -iw "beth" names.txt` => `Beth`

* `-A` display a certain number of lines after

`grep -A 3 "Beth" names.txt`

```
Beth
Tim
Elizabeth
Tom
```

* `-B` display a certain number of lines lines before

`grep -B 3 "Beth" names.txt`

```
Lisa
Mark
Elie
Beth
```

* `-C` display a certain number of lines lines around

`grep -C 3 "Beth" names.txt`

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
```

* `-v` invert pattern (you can think of this as anything NOT what you are searching for)

`grep -v "Jane" names.txt`

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
Matt
Liza
Shana
```

* `-c` count matches

`grep -c "Jane" names.txt` => `2`

* `-n` show line number

`grep -ni "Jane" names.txt`

```
10:Janey
11:Jane
```

There are **many** more flags with `grep`; you can google around for more or look at `man grep`.

#### Wildcards with `grep`

We previously saw wildcards with `find`, so how can we use them with `grep`? The key is to use _regular expressions_. Regular expressions are used to define patterns in a string of characters, which are then used to search a text for potential matches. Regular expressions are common and quite powerful: you can use them to check whether a user has submitted a properly formatted email address or phone number, for instance.

We will not go in depth with regular expressions here. There are a number of great [interactive references](https://regexr.com/) online. For now, but let's just take a look at a couple examples of the syntax:

`.` - matches any character

**Example:** How many names have a full name that is four characters long?

`grep -wc "...." names.txt` => `7`

`*` - match zero or more of the preceding character or expression.

**Example:** How many names start with a capital T?

`grep -wc "T.*" names.txt` => `2`

`[]` - any specific characters

**Example:** How many names start with a capital L, M, or E?

`grep -wc "[LME].*" names.txt` => `6`

`[^]` - do not match

**Example** How many names **do not** start with a capital T?

`grep -wc "[^T].*" names.txt` => `10`



## { Advanced Terminal - 1 Exercises. }

#### Part I

Answer the following questions:

1. Create an environment variable called `FIRST_NAME` and set it equal to your first name (this does not need to be permanent)
2. Print the `FIRST_NAME` variable
3. Print out the `$PATH` variable
4. What is the `$PATH` variable?
5. Why would you want to create an environment variable?
6. How do you permanently save environment variables?
7. What is a process?
8. How do you list all processes running on your machine?
9. What is a PID?
10. How do you terminate a process?
11. What is the difference between `kill` and `kill -9`?
12. What `grep` flag allows for case insensitive search?
13. What `grep` flag allows for a certain number of lines before the match?
14. What `grep` flag allows for a certain number of lines around the match?
15. What `grep` flag allows for a certain number of lines after the match?
16. What `grep` flag allows for full word search?
17. What `grep` flag shows you the line number of a match?

#### Part II

Write the following terminal commands to do the following (assume that `instructors.txt` is an imaginary file):

1. Find all files inside the `Desktop` folder that have a name of "learn."
2. Find all files inside the `Desktop` folder that start with a "P."
3. Find all files inside the `Desktop` folder that end with `.txt`.
4. Find all files inside the `Desktop/views` folder that have the name `data` somewhere in their filename.
5. Inside of the `instructors.txt` file, output the number of times the word "Elie" appears.
6. Inside of the `instructors.txt` file, list all matches for any full word that starts with a capital "P."
7. Inside of the `instructors.txt` file, list all the line numbers for any full word that starts with a "z" (it should match regardless of upper or lower case).



## Advanced Level - 2  { OPTIONAL }



### { SSH. }

#### Objectives

By the end of this chapter, you should be able to:

* set up an EC2 instance on Amazon
* use the `ssh` command to connect securely to a remote server
* use the `scp` command to copy files to a remote server

#### SSH

SSH, or **S**ecure **Sh**ell, provides a secure channel to access other computers. We commonly use SSH to remotely log in and connect securely to other servers. To practice with SSH we will be setting up our own remote servers using Amazon EC2. This setup can be a bit intimidating, but it's a very valuable skill to know with any kind of development. Let's get started!

#### Setting up an EC2 Instance

As evidenced by the list below, there are a fair number of steps involved in setting up your instance. The links provided also provide a fair amount of context, and help explain the purpose of each of the following steps.

1. Make sure that you have an Amazon Web Services (AWS) account. You can log in / sign up [here](https://docs.aws.amazon.com/) and click on the top right.
2. Create an IAM user [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-an-iam-user).
3. Create a key pair [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-key-pair)
4. Create a VPC [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-vpc)
5. Create a Security Group [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-base-security-group)
6. Launch your instance [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2\_GetStarted.html#ec2-launch-instance\_linux)
7. Connect to your instance [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2\_GetStarted.html#ec2-connect-to-instance-linux).

To connect to your instance using SSH you can start [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html).

Before you try to SSH make sure that your instance is running and that the checks have passed. This should involve typing something along the lines of `ssh -i ./me-key-pair-uswest2.pem ec2-user@YOUR_PUBLIC_DNS`

Once you've connected via SSH, you can exit out of the shell by typing `exit`.

#### Securely copying files to the EC2 Instance with scp

To move files to your EC2 instance, we use the `scp` command to securely copy information. We will need our `pem` file that we used before so make sure you know where that is located. The pattern for `scp` looks like this:

`scp -i PATH_TO_YOUR_PEM_FILE FILE_TO_MOVE USERNAME@PUBLIC_DNS`

This command would move the file `move.txt` from my current directory to the `home` directory on my EC2 instance.

`scp -i ./me-key-pair-uswest2.pem move.txt ec2-user@ec2-54-213-7-226.us-west-2.compute.amazonaws.com:/`

#### Terminate your instance

When you are done working on this tutorial - you **MUST** terminate your instance so that it is not still running. This ensures that you will not be charged for anything as well. You can read more about it [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2\_GetStarted.html#ec2-clean-up-your-instance)





### { Cut, Sed, Awk, and Xargs. }

#### Objectives

By the end of this chapter, you should be able to:

* Understand what the `cut` command does and list some use cases for it
* Understand what the `sed` command does and list some use cases for it
* Understand what the `awk` command does and list some use cases for it
* Understand what the `xargs` command does and list some use cases for it

#### cut

The `cut` command is very useful for separating or delimiting strings and characters. If you need to split apart text files or find certain characters, `cut` is the way to go. Let's see how it works with a few examples in a file called `languages.txt`:

`languages.txt`

```
Java,James
Ruby,Matz
Lisp,John
Bash,Brian
Self,David
```

Here's an example using `cut` to grab the first 4 characters of each line (the `-c` flag indicates that the numerical range coming after the flag is referencing characters, not bytes):

`cut -c 1-4 languages.txt`

```
Java
Ruby
Lisp
Bash
Self
```

Now let's grab the last names, but not by the number of characters. Instead, let's do this by delimiting (splitting) on the comma

`cut -d, -f2 languages.txt`

```
James
Matz
John
Brian
David
```

So what is the `-f2`? `-f` refers to each portion that has been split by the delimeter (`-d`) flag. So if we just want the names we can do

`cut -d, -f1 languages.txt`

```
Java
Ruby
Lisp
Bash
Self
```

This is much better because if we had languages of different character lengths, `cut -c 1-4 languages.txt` would not work!

Next, try to use `cut` to print out just the authors. Then sort them and then return the first two authors!

Here's one solution:

`cut -d, -f2 languages.txt | sort | head -n 2`

#### sed

Sed, or Stream EDitor, is one of the _much_ more complex terminal commands, so we will only be going over some simple uses cases. There are many, many things you can do with `sed` so try to follow these examples and push yourself to keep learning!

Sed is commonly used for finding and replacing text, editing text in a file, and printing certain parts of a file (though it can to much more). Let's start by finding and replacing each comma in the `languages.txt` file with a colon.

Here's the command:

`sed 's/,/:/g' languages.txt`

Let's break this down:

`sed` - the command\
`s` - substitute\
`,` - our old value, a comma\
`:` - our new value\
`g` - globally, do this everywhere not just the first match\
`languages.txt` - the file we are working with

Here's what the command should output:

```
Java:James
Ruby:Matz
Lisp:John
Bash:Brian
Self:David
```

Notice that if you `cat languages.txt` after running the above `sed` command, the original file is unchanged. In order to edit the file, we need to use the `i` flag to edit in place. But if you try running the command with the `-i` flag you'll get an error about extra characters. Since we are also specifying additional arguments, we need to use the `-e` flag as well.

`sed -ie 's/,/:/g' languages.txt`

If you run this command, and then `cat languages.txt`, you should see that everything has been replaced!

We are just scratching the surface with `sed`. If you want to learn more about it you can read [this](https://www.tutorialspoint.com/sed/sed\_basic\_syntax.htm) and [this](http://www.panix.com/\~elflord/unix/sed.html)

#### awk

Similar to `sed`, `awk` is an incredibly powerful text processing tool. In fact, AWK itself is actually a language that can pretty much do any kind of text manipulation you can think of. We will briefly cover `awk` and go over a few useful commands you can use with it.

Let's start with the simple command `awk '{print}' languages.txt`. This will simply print out the `languages.txt` file. But what happens if we want to just print out a certain part of the file? We can also use `awk` as a delimiter using the `-F` flag. Let's set `:` to be our delimiter and just print out the first portion delimited using `$1`

`awk -F ':' '{print $1}' languages.txt`

Let's look at another example, using the `history` command. If you type this into the terminal, you should see a list of your recent commands. Let's use `awk` to get a history of just the names of the commands we've used, with no further details. When using `awk`, if the delimiter is an empty space we do not need the `-F` flag. So if we want to find the commands we recently used we can type `history | awk '{print $2}'`.

We can also use `awk` to print out rows and columns. For example, if you type `df -h` into the terminal you'll see a table withs some information on your hard drive (`df` is short for display free desk space). Let's pass the result of this command into `awk`:

```
df -h | awk 'FNR == 2 {print $4}'
```

FNR refers to the record number which is usually a line number. Essentially we're telling `awk` to grab the item in the 2nd row and 4th column of the table, which in this case should be your available disk space.

If you want to read more about `awk`, check out [this](https://www.tutorialspoint.com/awk/) tutorial.

#### xargs

Sometimes you may want to execute the same command for multiple inputs. For instance, maybe you want to search multiple text files for a certain piece of text. This is a case where the `xargs` command can be quite handy. Here are some example use cases for `xargs`; each one runs command for a group of files instead of a single one.

`find . -name *.html | xargs grep "elie"` - look for the text "elie" inside of every single `html` file in the current folder

`ls | xargs wc -l` - counts the total amount of lines for each file in a folder

`find . -name "*" | xargs open` - opens all of the files in the current folder.

`find . -name "*.css" | xargs open` - opens all `css` files in the current folder

`find . -name "*.html | xargs rm` - removes all files that end with `.html`

`ls | xargs -t -I {} mv {} {}.md` - adds a markdown file extension to all files (the `-I` flag replaces occurrences; the `-t` flag causes the command that gets run for each input to be logged to the terminal before it is executed, which can be helpful for debugging).

You can read more about `xargs` [here](http://www.cyberciti.biz/faq/linux-unix-bsd-xargs-construct-argument-lists-utility/)





### { Shell Scripting and Vim. }

#### Objectives

By the end of this chapter, you should be able to:

* write simple shell scripts with arguments
* use `vi` to open and edit files

#### Shell Scripting

So far we have learned how to use terminal commands, but our commands are not dynamic. We know exactly what the filenames are or what we might be searching for. Our commands are also not reusable easily; if the filename changes, we have to write the whole command again. To reduce duplication and perform far more sophisticated commands in the terminal, we can write shell scripts using a language called bash. To get started, let's create a file called `first.sh` and inside place the following

```
echo "Hello World"
```

Now if we try to run `./first.sh` it will tell us `permission denied: ./first.sh`. So we need to make this program executable! Let's change permissions to `755` so that anyone can run this file: `chmod 755 first.sh`. Now we can run `./first.sh`!

Let's make a second script called `second.sh`. Inside of this file, type the following:

```
echo Hello $1
```

What do you think that `$1` represents? Let's first `chmod 755 second.sh` and then run `./second.sh` - we should just see "Hello". Now let's try `./second.sh World` and we should see "Hello World"! What we just did was pass an argument to our script. Using arguments which start with `$1` and continue upward are how we can make more dynamic scripts.

#### Your turn

Write a script called `sum.sh` which accepts two arguments and echoes the sum of the two numbers. You might need to do some research [here](https://stackoverflow.com/questions/6348902/how-can-i-add-numbers-in-a-bash-script).

Here's a solution:

```
echo $(($1+$2))
```

#### More complex scripts

There is much more we can do with shell scripting, including conditional logic, if statements, and much more. But for now, let's try to write some handy scripts to help us with daily tasks. Very commonly we are searching for a process using `ps aux | grep "Something"`. Instead of typing that whole thing, we could make a script that does that for us and passes in an argument. Let's try that out with a script called `process.sh`. It might look something like this.

```
ps aux | grep $1
```

Now this is useful if we want to search for a process! If you would like to use the script frequently, you will want to make sure it is somewhere in your $PATH. You can also remove the `.sh` extension if you are doing this.

#### Vim

Vim is a terminal based text editor. It can be quite intimidating at first, but if you spend the time to learn how to use it, you can become an extremely efficient developer. To open up something in `vi`, simply type `vi NAME_OF_FILE`. Once you are in vim you can exit **without** saving by pressing `escape + : + q`. If that is not working press `escape` + `:` + `q!`. If you want to quit and save a file you can either press `shift + Z + Z` or `escape + : + w + q!`.

When you first get into vim you will be in what is called `visual` mode. This means that your keyboard will be set for navigating and not for inserting characters; if you type letters and do not see anything being output, do not worry! To make insertions, press `i` to enter `insert` mode. Here you can make changes to files and type as you normally would. Just remember, if you want to quit out of a file you have to be in `visual` mode!

You can get more practice by using `vimtutor` - just type `vimtutor` into your terminal and you can get started. Alternatively, if you want a more visual tutorial you can check out [Vim Adventures](https://vim-adventures.com/).



## { Advanced Terminal - 2 Exercises. }

Use the following text file to answer the questions

```
Elie-Schoppik-sushi
Tim-Garcia-gummybears
Janey-Keig-bagels
Colt-Steele-tacos
Matt-Lane-pizza
```

1. Replace all of the `-` with `:` using `sed`
2. Return a file with just the first name and last name separated by a space (you can do this with `cut` and `sed` or just `sed`)

```
1>>>>2
2>>>>3
3>>>>4
4>>>>5
```

1. Using `cut` print out just the numbers 2, 3, 4, 5. Use `xargs` to print them all on 1 line
2. Using `xargs` in the `./Desktop` directory, find all of the files that include the text `Welcome`
3. Write a shell script called `access_file.sh` which accepts one parameter and changes the permissions to `755`
4. Write a shell script called `unaccessible_sh.sh` which accepts one parameter and changes the permissions to `300`
5. Using `sed` write the command to replace all instances of the name "foo" with the string "bar" in a file called `baz.txt`
6. Write the command to only print out all of the `pid`s using `awk`
7. Type in the `df -h` command - it will show you much space you have on your hard drive. Using the `awk` command, print out **only** the first percentage capacity.

