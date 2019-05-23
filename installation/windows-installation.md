### Installing Python on Windows

Here's what you need to do to set up your Windows machine:

1. Use [this link](https://www.python.org/ftp/python/3.7.3/python-3.7.3-amd64.exe) to download Python.
2. Windows may prompt you on whether you want to run or install Python. Click **Run** or **Yes** when these prompts may appear. Otherwise, save the file to your computer and double-click to start the installer.
3. **Important!** Before pressing the "Install Now" button - Check the box to "Add Python 3.7 to PATH".
![Image showing the checkbox needed for adding Python to the Path.](/images/path.png)
4. Click **Install Now**. This will also install IDLE (official Python IDE), pip (used to install Python packages), and documentation tools that will make your Python learning experience much easier. 
5. Follow the instructions to complete the installation if prompted also press **Disable path length limit** and accept the changes. Click **Close** when complete.

**Accessing the Python Interpreter**

Now we can make sure Python installed correctly by opening a command prompt and starting the Python interpreter. We will be doing this a few times so be sure to get comfortable with this process.

Open up the start menu and search for and open the "command prompt". You can also search for "cmd" to find the program.

The command prompt is another way of interacting with your computer. It can do many of the same things like running programs, editing files and more but it does so in a text-based manner. 

We will run the Python interpreter and Python scripts from the command prompt. When you sucessfully open the command prompt, you can 

1. At the command prompt (which will look something like `C:\Users\username>`, type:
  ```
  python
  ```
  You should see something that looks like this:

  ```
  Python 3.7.3 (v3.7.3:ef4ec6ed12, Mar 25 2019, 22:22:05) [MSC v.1916 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  ```
  You just started Python! The `>>>` indicates that you are at a new type of prompt -- a Python prompt. 
  
  The command prompt (the one starting with `C:\`) lets you navigate your computer and run programs, and the Python prompt lets you write and run Python code interactively. Make sure the number that you see following Python is a 3!

4. To exit the Python shell, type `exit()` and hit enter.  You'll now be back at the Windows command prompt (the `C:\Users\username>` that you saw earlier).
