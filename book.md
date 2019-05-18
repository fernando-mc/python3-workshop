# A Complete Beginner's Introduction to Python

By Fernando Medina Corey:
https://www.fernandomc.com

# Table of Contents
1. [Introduction to the Introduction](#introduction-to-the-introduction)
    - [About Python](#about-python)
    - [What Can You Do with Python?](#what-can-you-do-with-python)
    - [So what do I need to know or have right now?](#so-what-do-i-need-to-know-or-have-right-now)
2. [Installing Python on Your Machine](#installing-python-on-your-machine)
    - [Installing Python on Windows](#installing-python-on-windows)
    - [Installing Python on Mac](#installing-python-on-mac)
    - [Installing Python on Linux](#installing-python-on-linux)


## Introduction to the Introduction

You're about to have a lot of fun. Python has been my favorite programing language for nearly a decade and I can't wait to share it with you! It's come a long way since then and I can't wait to dive in with you.

By reading this, you'll learn about topics that range from just getting Python installed on your computer to the amazing things you can do with it after you understand the basics.

### About Python

Python is, in my opinion, the most welcoming programming langauge. Both in terms of the community around it and the language's syntax itself. 

Saying hello with python is as simple as:

```py
>>> print("Hello!")
Hello!
```

Now there might be a few basic concepts to master, but as you work with the language you will find they become somewhat intuitive.

Here are a few things about Python to keep in mind:

- **Python is open source**: You can can see all of the underlying code and everyone has the chance to contribute to the code base. Take a look on GitHub: [https://github.com/python](https://github.com/python)
- **Python is popular**: Python consistently ranks as one of the most loved and wanted programming languages.
- **Python is portable**: Python code can be developed and run on Windows, Mac, or Linux systems.
- **Python is powerful and flexible**: Python has a massive community of developers behind it that have contributed powerful tools and applied Python to a variety of different problems.

### What Can You Do with Python?

Lots! Here is a tiny subset of the things that you can do with Python:

  - Write, access and modify files on your computer
  - Collect and clean data from the web
  - Build and deploy websites or APIs
  - Create your own desktop games

### So what do I need to know or have right now?

**Required Knowledge** 

You should know some of the basics of using computers as a non-programmer. This includes things like using web browsers like Google Chrome or Firefox to download programs and visit webpages when given a URL like: [https://www.python.org/](https://www.python.org/).

**Required Materials and Environment**

You will also need to have a "real computer" that you have full permissions over. 

What I mean by this is that you won't be able to use a smartphone, iPad, or graphing calculator to following along (at least none of the graphing calculators I've ever used before). You will need a computer that has a Windows, Mac, or Linux operating system installed. Preferrably, you'll have a more modern version of any of those operating systems. This is because the more ancient your operating system, the more difficult it will be to garuntee it will work with the modern tools used in this course.

Additionally, your computer, regardless of the operating system will require administrator priviliges so that you can download and install programs and software packages.  

### A Quick Note on Syntax

If you see something in this guide that looks like this: `python3 --version`

You should assume that it is some sort of code that should be typed out in the exact same way as you see it. Additionally, if you see some part of this guide with a dollar sign at the start like this: 

`$ python3 --version`

You should assume that that indicates you need to type it into your Terminal, or Command Prompt. Whereas if you see something that has three greater-than signs like this:

`>>> import time`

That means you should type the code that follows it into the Python interpreter (more on the Terminal/Comand Prompt vs. the Python interpreter later).

## Installing Python on Your Machine

### Installing Python on Windows

Here's what you need to do to set up your Windows machine:

1. Use [this link](https://www.python.org/ftp/python/3.7.3/python-3.7.3-amd64.exe) to download Python.
2. Windows may prompt you on whether you want to run or install Python. Click **Run** or **Yes** when these prompts may appear. Otherwise, save the file to your computer and double-click to start the installer.
3. Check the box to "Add Python 3.7 to PATH".
4. Click **Install Now**. This will also install IDLE (official Python IDE), pip (used to install Python packages), and documentation tools that will make your Python learning experience much easier. Follow the instructions to complete the installation, and click CLOSE when complete.
5. Open a command prompt (we will be doing this multiple times, so make a note of how to do this!):
  - **Windows 8 or Windows 10**: Open the Start Menu and search for "command prompt"
  - **Windows 7 or Vista**: Click on the Start menu (the Windows logo in the lower left of the screen), type `cmd` into the Search field directly above the Start menu button, and click "cmd" in the search results above the Search field.
  - **Windows XP**: Click Start menu, click "Run...", type `cmd` into the text box, and hit enter.

You now have what's called a command prompt. This command prompt is another way of navigating your computer and running programs -- just textually instead of graphically. We are going to be running Python and Python scripts from this command prompt.

3. At the command prompt (which will look something like `C:\Users\username>`, type:
  ```
  python
  ```
  You should see something that looks like this:

  ```
  Python 3.6.0 (v3.6.0:41df79263a11, Dec 23 2016, 08:06:12) [MSC v.1900 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  ```
  You just started Python! The `>>>` indicates that you are at a new type of prompt -- a Python prompt. The command prompt lets you navigate your computer and run programs, and the Python prompt lets you write and run Python code interactively. If the number after Python is not 3 or greater, please tell an instructor or assistant.

4. To exit the Python shell, type `exit()` and hit enter.  You'll now be back at the Windows command prompt (the `C:\` that you saw earlier).

### Installing Python on Mac

**Important**: Mac machines come with Python 2 installed, however, Python 2's end-of-life is 2020 and we'll be working with Python 3 so we still have to install Python 3.

1. Download the [Python 3 installer for Mac](https://www.python.org/ftp/python/3.7.3/python-3.7.3-macosx10.9.pkg).
2. Double-click the downloaded file to start the installation process.
3. Click through the wizard. The default settings are all fine to use. Close the wizard when complete. By default, the package installs into a central location which will require you to enter your system username and password during the process.

### Installing Python on Linux

Many Linux machines have both Python 2 and Python 3 pre-installed. To find out, search for the "Terminal" program on your computer and open it up.

Inside the terminal, type out `python --version` and press enter. If you see the result of: `Python 2.7.10` from now on you may need to add the number `3` to the end of `python` when you run commands in the terminal.

Next, try typing in `python3 --version` and pressing enter. Hopefully, you'll see something that indicates a version of Python 3 such as `Python 3.5.2`. 

If this works, and you see a version of Python starting with 3, you're good to go! If it doesn't, you'll need to install Python 3 manually on your Linux machine. This process varies widely depending on your Linux distribution so you should search for guides on installing Python 3 specifically for your distribution. 

## Installing Development Tools

### Installing Sublime Text??? OR VS CODE