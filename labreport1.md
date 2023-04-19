# Lab Report 1

## Part 1: Finding Your CSE15L Account

Use this [link](https://sdacs.ucsd.edu/~icc/index.php) to lookup your course-specific account for CSE 15L. Type in your username and student ID. After entering those fields, you should see a section called "Additional Accounts" with an account "cs15lsp23zz" where "zz" is replaced by the specific letters for your username. 
![Image](account_lookup.png)

Since this is your first time logging in, you'll need to set a new password for your CSE15L account. Follow [this tutorial](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view) to reset your password.


## Part 2: Installing Visual Studio Code

To install Visual Studio Code, go to their website at https://code.visualstudio.com/. Follow the instructions to download Visual Studio Code for your operating system.
Once successfully installed, you should be able to open Visual Studio Code and see a page that looks similar to this:

<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/vscode_installed.png?raw=true" width=50% height=50%>


## Part 3: Remotely Connecting

If you're using Windows, you'll first need to download Git at https://gitforwindows.org/. Once that is installed, you'll need to set your default terminal in Visual Studio Code to use Git Bash.

1. Open Visual Studio Code and press [Ctrl] + [ ` ] to open a terminal.

2. Open the command palette with [Ctrl] + [Shift] + [P]. Type "Select Default Profile" into the search bar and select Git Bash from the options.
<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/git_bash.png?raw=true" width=75% height=75%>

3. Click on the + icon in the terminal window to open a new terminal that uses Git Bash.
<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/bash_terminal.png?raw=true" width=75% height=75%>

Once you have a Git Bash terminal open, you can use `ssh` through this command:
`$ ssh cs15lsp23zz@ieng6.ucsd.edu` where `zz` is replaced by the letters in your course-specific account username.
Since this is your first time remotely connecting to this server, when you run the code you may get a message like this:
```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

Type `yes` and press enter. The terminal should ask you to enter your password. When you type your password, the letters may not appear because the terminal wants to hide the password (similar to how passwords show up as dots on other websites). After you've entered your password, you should see a message like this:
```
Hello cs15lsp23zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   13:20:01   10  0.01,  0.10,  0.15
ieng6-202   13:20:01   4   4.05,  4.08,  4.12
ieng6-203   13:20:01   6   1.08,  1.16,  1.18

 
Sun Apr 09, 2023  1:22pm - Prepping cs15lsp23
```

This means that you have successfully remotely connected to the server!

## Part 4: Running Some Commands

Now that you've remotely connected to the server, you can try running some commands! Here are a list of commands you can try out:
* `cd ~`
* `cd`
* `ls -lat`
* `ls -a`
* `cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/`
* `cat /home/linux/ieng6/cs15lsp23/public/hello.txt`

The code and output should look something like this:

<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/example_code.png?raw=true" width=50% height=50%>

Once you are finished, you can log out of the remote server by using [Ctrl] + [D] or running the command `exit`.
