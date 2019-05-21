### Installing Python on Mac

**Important**: Mac machines come with Python 2 installed, however, Python 2's end-of-life is 2020 and we'll be working with Python 3 so we still have to install Python 3.

1. Download the [Python 3 installer for Mac](https://www.python.org/ftp/python/3.7.3/python-3.7.3-macosx10.9.pkg).
2. Double-click the downloaded file to start the installation process.
3. Click through the wizard. The default settings are all fine to use. Close the wizard when complete. By default, the package installs into a central location which will require you to enter your system username and password during the process.

**Accessing the Python Interpreter**

Let's test that your installation went well. We can do this by:

1. Searching for and opening up the `Terminal` program.
2. Enter `python3` into the terminal and press enter. It should look something like this:
  ```
  $ python3
  ```
  Then, you should then see something like this:
  ```
  Python 3.7.3 (v3.7.3:ef4ec6ed12, Mar 25 2019, 16:52:21) 
  [Clang 6.0 (clang-600.0.57)] on darwin
  Type "help", "copyright", "credits" or "license" for more information.
  >>> 
  ```
  While inside the python interpreter:
    - The `>>>` indicates that you are at a Python prompt.
    - You can exit the Python prompt by typing `exit()` and pressing enter or by using `control+d`.

Practice doing this a few times until you are comfortable entering and exiting the Python shell.
