# Using Visual Studio Code for Python
Sasha D. Hafner

# 1. Overview

# 2. Installing software
## VS Code
Visual Studio Code, VS Code, or, as we'll call it, VSC, is a free "integrated development environment" (IDE) produced by Microsoft.
It is a simpler version of Visual Studio with fewer features.
If you don't already have it, you can download it from here: <https://code.visualstudio.com/download>

## Python
Python (3) should be installed from here: <https://www.python.org/downloads/>.

## VS Code Python extension
Lastly, you will need a Python extension.
1. Open up VSC and click the Extensions icon (near top left, looks like four squares) or use `Ctrl + Shift + x`.
2. Search for `Python`.
3. Carefully find the one published by Microsoft that has a description similar to this: "Python language support with extension access points for IntelliSense (Pylance), Debugging (Python Debugger), linting, formatting, refactoring, unit tests, and more."
4. Install it.

Your VSC program may not give you access to all the features you need by default, including extensions, depending on which folder it is running in.
If you see this warning at the top, you must "trust" the folder.

<img width="727" height="76" alt="image" src="https://github.com/user-attachments/assets/75c36dbf-2b7a-4fec-866f-4c5416153f3c" />

Click on "Manage" and then "Trust" to do that.

# 3. PowerShell and other shells
A *shell* is a text-based program that reads commands and does things. 
If you have ever done command-line work, you've worked with a shell.
Most of the readers of this guide are probably using Windows, and for that operating system, the modern shell to use is called PowerShell. 
In our Python work we will typically interact with PowerShell only through VSC.
But here we'll start by running PowerShell in the Windows terminal program (the window that runs shells) just for understanding.

Open up PowerShell (hit the Windows or super key ⊞ and type PowerShell), and you should see something like this:

<img width="1112" height="316" alt="image" src="https://github.com/user-attachments/assets/5451e621-f61d-42f1-9c53-f739cc62d8be" />

The bit at the left, `PS C:\Users\au594831>` is called the "prompt".
The single `>` is one way to tell you are working in PowerShell.

There are many commands that PowerShell understands, for example, `cd .\GitHub_repos` to change to a folder (directory) named "GitHub_repos", `ls` to list the contents of the current directory, and `python scrip1.py` to run a script called "script1.py" in Python (if it has been installed). 
The `mv`, `rm`, and `cp` commands are for moving, removing (deleting), and copying files--use them carefully!

Here is an example PowerShell session.

<img width="1089" height="580" alt="image" src="https://github.com/user-attachments/assets/4c927927-c3c4-4800-ad06-8325e09ba183" />

Try some of these commands yourself, but in a temporary directory with some junk files!

Python scripts can be run directly in PowerShell with the `python` command. 
For example, the command below ran all the code in the `demo.py` script in Python.

<img width="1104" height="148" alt="image" src="https://github.com/user-attachments/assets/4761a0a9-bd72-4305-bd6a-781ae2a34d27" />

A shell can also run some programs interactively, including Python.
To do that, just type `python` at the prompt, like this:

<img width="1105" height="177" alt="image" src="https://github.com/user-attachments/assets/7a0dcede-b838-4683-88aa-d09a8ace90dd" />

Notice how the prompt now looks different?
Like this, but also fuchsia in color: `>>>`.
That is a hint to show that you are now in a Python *interpreter*, which will read any commands you enter and evaluate them.
This type of programming environment is called a REPL, from "read-evaluate-print loop".
You will see the term REPL a lot in this guidance, where it refers to a terminal window running Python interactively.

This window will now act like any interactive Python instance, for example,

<img width="1101" height="243" alt="image" src="https://github.com/user-attachments/assets/1ea6e9dd-dc66-422a-9487-04b0731a8f6c" />

If you are working on a Mac, the shell is called, somewhat confusingly, Terminal.
And on Linux, Bash is the most popular shell. 


