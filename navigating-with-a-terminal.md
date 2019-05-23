# Navigating with a Terminal

## The Filesystem 

The way your computer organizes storage is called a filesystem. The filesystem on your computer is like a tree made up of folders (also called "directories") and "files". On Mac and Linux machines, the highest point in the tree is the root directory located at `/`. For the purposes of this tutorial, the closest Windows equivalent is the top of the C drive at: `C:\`. Everything you can access on your computer lives within the sub-directories of this root directory.

We often navigate the filesystem graphically by clicking on graphical folders in programs like Finder or Windows Explorer where we can explore different files and folders. We can do the exact same navigation from the command line.

## Command Line Confusion

There are a few text commands that we’ll be using in order to navigate the filesystem on our computer. But before we dive into them let's clarify something. 

There are probably a dozen terms for the tools that developers use to process text-based commands they enter into a program. For example, you might hear the terms "Terminal", "Command Line", "Command Line Interface", or "Shell" all thrown around as a start. This guide won't dive into those differences in too much detail. Instead, I'll try to clarify a few potentially confusing terms relevant to what you will be using. 

**Command Line or Terminal** 

In the context of this guide, I'll try to use these terms to generally mean a place where you type in text commands. This might be into VS Code within the "Terminal" section, or into a Mac/Linux program called "Terminal". On Windows, this could be inside of the PowerShell or Command Prompt programs. Each of these support entering text-based commands that interact with your computer.

**The VS Code Terminal** 

This is a feature inside of VS Code that loads up a window where you can type in commands to do things like navigate your file system. This feature will load up a different program in the background depending on your operating system. For example, on Mac and Linux the default program is called `bash` whereas on Windows you may either be using `PowerShell` or `Command Prompt` depending on the version of Windows you're using.

**Shell**

I'll try to use this term to differentiate between different things that process the text-based commands you type out. For example, in VS Code if you open the "Terminal" section you should see a dropdown that says one of the following:

- `bash` (On Linux and Mac)
- `powershell` (On Windows 10)
- `cmd` (On earlier versions of Windows)

These are different programs that process the text commands you enter. And, in fact, if you enter the Python interpreter from within the Terminal window of VS Code the shell is shows will be `Python`.

**The Python Interpreter**

The Python interpreter is what we will be spending most of our time interacting with. You can always tell you are working in the Python interpreter when you see the three greater than signs: `>>>`

That means you're ready to type out Python code.

## Command Line Commands 

For Mac and Linux (with bash) and Windows (with PowerShell or Command Prompt) the commands below should all work the same with a few noted exceptions. However, there are other differences between operating systems and these shells so if you start to learn more command line commands, be sure to learn them for your particular shell and operating system.

For now, here are the commands you'll need:

- `ls` (or `dir` for Command Prompt) lists the contents of a directory (“what’s in this folder?”).
- `pwd` prints the full directory path to your current directory. It stands for "print working directory." This command wont work in the Command Prompt, but you also wont need it because Command Prompt and PowerShell show you what directory you're in by default.
- `cd` moves you into a new directory (it stands for “change directory”).
- `cd folder_name` Go into the `folder_name` directory.
- `cd ..` Go up one level in the folder heirarchy.

The `dir` command will also work with PowerShell.

## Practicing Commands

So now that we understand some of the terminology and the purpose of a few commands, let's get started trying them out.

First, in VS Code open up a Terminal under the Terminal tab. Then follow along with the instructions for your operating system below. Type out each of the commands into the VS Code Terminal and then press the `enter` or `return` key.

### Mac

`ls` - This lists all the files in your home directory.

`pwd` - This displays the full directory path to your current directory, which is your home directory.

`cd /` - This will change you into the `/` (root) directory.

`ls` - This lists the contents of the `/` (root) directory.

`cd Users` - This will change you into the `Users` subdirectory of the `/` (root) directory.

`ls` - You should see a list of all the computer’s users' home directories (and possibly a Shared folder).

`pwd` - This displays the full directory path to your current directory, which in this case is `/Users`.

`cd ..` - When typing in `..` that means the "parent directory" of the current directory. Because you were in `/Users`, now you can move up to the "parent" which is `/`, the root directory.

`ls` - This lists the contents of the root directory, confirming where you are.

`cd ~` - Just like how `..` means "parent directory", `~` means "home" directory. When you execute this command, you’ll change back to your home directory, where all your user files are.

### Linux

`ls` - This lists all the files in your home directory.

`pwd` - This displays the full directory path to your current directory, which is your home directory.

`cd /` - This will change you into the `/` (root) directory.

`ls` - This lists the contents of the `/` (root) directory.

`cd home` - This will change you into the `home` subdirectory of the `/` (root) directory.

`ls` - You should see a list of files and directories in the home directory including a directory with your username.

`pwd` - This displays the full directory path to your current directory, which in this case is `/home`.

`cd ..` - When typing in `..` that means the "parent directory" of the current directory. Because you were in `/home`, now you can move up to the "parent" which is `/`, the root directory.

`ls` - This lists the contents of the root directory, confirming where you are.

`cd ~` - Just like how `..` means "parent directory", `~` means "home" directory. When you execute this command, you’ll change back to your home directory, where all your user files are.

### Windows (PowerShell or Command Prompt)

`dir` - This lists all the files in your home directory.

`cd C:\` - This will change you into the `C:\` directory.

`dir` - This lists the contents of the `C:\` directory now that we are in it.

`cd Users` - This will change you into the `Users` subdirectory of the `C:\` directory.

`dir` - You should see the names of all the files and directories in `C:\Users`.

`cd ..` - The two dots mean "parent directory", so this command moved you up to the parent directory. You were in `C:\Users`, so now you are in `C:\`, the root directory.

`dir` - This lists the contents of the current directory (root).

### Tips

**Tab Auto Complete**

You can use the Tab key to auto-complete both directory and file names. So if you want to change into a directory within the current location called `Documents` and you type `cd Doc` and hit Tab, the command prompt will auto-complete the directory name, and you can then hit enter to change into that directory. Importantly, this will sometimes only happen if there are no other directories that share the same beginning of the directory name. For example, if we also had a `Docuseries` folder on our desktop this wouldn't work the same.

**Command History**

When working with the command line (and with the Python interpreter!) the shell maintains a command history. You can use the up arrow to cycle through old commands. Open a command prompt and hit the up key a few times to see what you've typed recently.

### A Challenge

Now that you know the basics of navigating the file system on your machine with the command line try this:

1. Using Finder (for Mac), File Explorer (for Windows), or the equivalent graphical file explorer for your Linux distribution create a folder on your desktop called `workshop2019`.
2. See if you can find and navigate into the folder with the new commands you've learned.

That's it! You know all the basics you need to know in order to get started learning Python!

## [Next... Part 1](part1.md)

### [Previous... Installing Python and VS Code](installing-python-and-vscode.md)