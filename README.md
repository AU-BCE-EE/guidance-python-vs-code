# Using Visual Studio Code for Python
Sasha D. Hafner

# 1. Overview

This guide provides information on using Python the Visual Studio Code, a flexible and free integrated development environment (IDE) that works particularly well for Python.
Altong with relevant background, this guide includes three main ways to use Python in VS Code: 

1. **Interactive** by typing directly into a Python interpreter
2. **Script mode** by calling Python and running script in shell non-interactively
3. **Interactive script development** by sending script code by line or section to the Python interpreter

These are not the only ways Python can be used in VSC.
But they are perfectly sufficient for the majority of our needs in projects and courses.
Some users may prefer a Jupyter Notebook-based approach or a Quarto report.
Both are supported by VSC but are not covered in this guide.
You should recognize that other approaches exist and you may accidentially discover them in VSC by clicking the wrong button!

This guidance document is written in Markdown, and is meant to be viewed online, where GitHub will render the Markdown formatting and include images of the screenshots.
But the repository (repo) includes demos that can be run locally, so it can be helpful to clone the repo and work with the folders and scripts.

Much of what is covered in this guide is specific to VSC.
But any Python code or shell commands are not--they could be applied independent of VSC.

The rest of this guide includes:

* installing software (section 2), which can be skipped if Python and VSC are already installed,
* PowerShell and other shells (section 3), which includes some important conceptual background but could be skimmed,
* 

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

# 4. Getting started with VS Code
## Projects
VSC uses something called *projects* to keep track of all the files involved in a project or assignment.
There is really only one part of this that is important to us--to set the project location before working.

Let's open up VSC and start and new project.
First, make sure you have a directory or folder for your project.
To follow along with this guide, you can create a folder called `simple_project` in any appropriate location on your local computer.
(Or, you can clone this repo and use the `demos/simple_project` folder that is included.)
Then, in VSC, under the `File` menu, click `Open folder`, 

<img width="1487" height="381" alt="image" src="https://github.com/user-attachments/assets/908e8994-9553-46d5-917f-35d7f64f6d72" />

and browse to your folder,

<img width="1564" height="763" alt="image" src="https://github.com/user-attachments/assets/3925bb3f-2507-4b46-9b4e-71dbbb84c3e3" />

and click "Open".

Alternatively, you can hit `Ctrl + k` followed by `Ctrl + o`, and browse to the correct folder.

What does this do?
It ensures that when Python is run it will have this folder as the *working directory*, i.e., the location where Python looks for files and saves output.
Making sure that you start with this `open folder` step avoids a whole lot of problems related to file paths!

## Create a script
A *script* is just a text file with commands in Python or some other computer language.
Python scripts are typically named with the `.py` extension, e.g., `simple1.py`. 
Windows users may think there is a lot of magic in file extensions, but they are simply part of a file name.

In VS Code you can create a new script with the `File` menu by selecting `New File` or `New Text File` (or using the keyboard shortcuts that are shown in the menu, e.g., `Ctrl + n`).
Do this, add some content, e.g.,

```
"""
file: simple1.py
author: Your Name

description:
    A simple Python script
"""

print("If this message is printed, you ran this script!")

x = 10 + 2

print('Here is a sum:', x)
```

and save the file with 

## Open terminal window
Under the `Terminal` menu select `New terminal.
You should then see something like this at the bottom of your VSC window:

<img width="1427" height="214" alt="image" src="https://github.com/user-attachments/assets/4c6ea7cb-f2cc-433c-b8c3-e48942396cd5" />




# Other resources
https://realpython.com/interacting-with-python/
https://www.geeksforgeeks.org/computer-science-fundamentals/what-is-the-difference-between-interactive-and-script-mode-in-python-programming/




