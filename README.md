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


