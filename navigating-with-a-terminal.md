# Navigating with a Terminal

## The Filesystem 

The way your computer organizes storage is called a filesystem. The filesystem on your computer is like a tree made up of folders (also called "directories") and "files". The highest point in the tree is the root directory located at `/`. Everything you can access on your computer lives within the sub-directories of this root directory.

We often navigate the filesystem graphically by clicking on graphical folders in programs like Finder or Windows Explorer where we can explore different files and folders. We can do the exact same navigation from the command line.

## Command Line Confusion

There are a few text commands that we’ll be using in order to navigate the filesystem on our computer. But before we dive into them let's clarify something. 

There are probably a dozen terms for the tools that developers use to process text-based commands they enter into a program. For example, you might hear the terms "Terminal", "Command Line", "Command Line Interface", or "Shell" all thrown around as a start. This guide won't dive into those differences in too much detail. Instead, I'll try to clarify a few potentially confusing terms relevant to what you will be using. 

**Command Line or Terminal** 

In the context of this guide, I'll try to use these terms to generally mean a place where you type in commands that are not Python code. This might be into VS Code within the "Terminal" section, or into a Mac/Linux program called "Terminal". On Windows, this could be inside of the PowerShell or Command Prompt programs. Each of these support entering text-based commands that interact with your computer.

**Shell**

I'll try to use this term to differentiate between different things that process the text-based commands you type out. For example, in VS Code if you open the "Terminal" section you should see a dropdown that says one of the following:

- `bash` (On Linux and Mac)
- `powershell` (On Windows 10)
- `cmd` (On Earlier Windows OSes)

These are different programs that process the text commands you enter.

**The VS Code Terminal** 

A feature inside of VS Code that loads up a window where you can type in the commands mentioned above to do things like navigate your file system. This feature will load up a different program in the background depending on your operating system. For example, on Mac and Linux the default program is called `bash` whereas on Windows you may either be using `PowerShell` or `Command Prompt` depending on the version of Windows you're using.

## Command Line Commands 

For Mac and Linux (with bash) and Windows (with PowerShell or Command Prompt) the commands below should all work the same with a few noted exceptions. However, there are other differences between operating systems and these shells so if you start to learn more command line commands, be sure to learn them for your particular shell and operating system.

For now, here are the commands you'll need:

- `ls` (or `dir` for Command Prompt) lists the contents of a directory (“what’s in this folder?”).
- `pwd` prints the full directory path to your current directory. It stands for "print working directory." This command wont work in the Command Prompt, but you also wont need it because Command Prompt and PowerShell show you what directory you're in by default.
- `cd` moves you into a new directory (it stands for “change directory”).
- `cd folder_name` - Go into the `folder_name` directory.
- `cd ..` - Go up one level in the folder heirarchy.

The `dir` command will also work with PowerShell.

## Practicing Commands

So now that we understand some of the terminology and the purpose of a few commands, let's get started trying them out.

First, in VS Code open up a Terminal under the Terminal tab. Then follow along with the instructions for your setup below.

### Windows 

In the VS Code terminal window, type out these commands:

dir - This lists all the files in your home directory.
cd C:\ - This will change you into the C:\ directory.
dir - This lists the contents of the C:\ directory.
cd Users - This will change you into the Users subdirectory of the C:\ directory.
dir - You should see the names of all the files and directories in C:\Users.
cd .. - The two dots mean “parent directory”, so this command moved you up to the parent directory. You were in C:\Users, so now you are in C:\, the root directory.
dir - This lists the contents of the current directory (root).

TIPS




### Mac - bash

### Linux - bash



## [Next... Navigating with a Terminal](navigating-with-a-terminal.md)