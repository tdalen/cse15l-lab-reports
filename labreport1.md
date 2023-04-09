# Lab Report 1

## Part 1: Finding Your CSE15L Account

Use this [link](https://sdacs.ucsd.edu/~icc/index.php) to lookup your course-specific account for CSE 15L. Type in your username and student ID. After entering those fields, you should see a section called "Additional Accounts" with an account "cs15lsp23zz" where "zz" is replaced by the specific letters for your username. Since this is your first time logging in, you'll need to set a new password for your CSE15L account. Follow [this tutorial](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view) to reset your password.

## Part 2: Installing Visual Studio Code

To install Visual Studio Code, go to their website at https://code.visualstudio.com/. Follow the instructions to download Visual Studio Code for your operating system.
Once successfully installed, you should be able to open Visual Studio Code and see a page that looks similar to this. 
![Image](vscode_installed.png)

## Part 3: Remotely Connecting

If you're using Windows, you'll first need to download Git at https://gitforwindows.org/. Once that is installed, you'll need to set your default terminal in Visual Studio Code to use git bash.

1. Open Visual Studio Code and press [Ctrl] + [ ` ] to open a terminal. 
2. Open the command palette with [Ctrl] + [Shift] + [P]. Type "Select Default Profile" into the search bar and select Git Bash from the options.
3. Click on the + icon in the terminal window to open a new terminal that uses Git Bash.

Once you have a Git Bash terminal open, you can use ssh through this command:
`$ ssh cs15lsp23zz@ieng6.ucsd.edu` where `zz` is replaced by the letters in your course-specific account username.
