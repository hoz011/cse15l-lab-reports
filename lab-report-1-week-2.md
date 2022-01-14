# Lab Report 1- Remote Access
*JANUARY 14, 2022*

**The following is a tutorial on how to log into and access files on a remote `ieng6` account.**

*[Operating System Used: Windows]*

## STEP ONE: INSTALLING VSCODE
---

1. Click on the following link to download VSCode to your computer: [Link](https://code.visualstudio.com/)
2. Once downloaded, open VSCode and you should see a screen that looks something like the following (color/format may be different): 

    ![Image](vscode_welcome_page.PNG)

## STEP TWO: REMOTELY CONNECTING
---

1. Make sure you have a program called OpenSSH installed. If you don't or aren't sure, see this link for more detailed instructions: [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. Look up your CSE15L account here: [Link](https://sdacs.ucsd.edu/~icc/index.php)
3. Open VSCode, create a new terminal, and type the following into the terminal:

    `$ ssh cs15lwi22__@ieng6.ucsd.edu`

    with your own account information.

4. Enter your password and press Enter. The terminal should display something like this:

    ![Image](ssh_login_terminal.PNG)

*(If your password doesn't work, you may need to reset it.)*

## STEP THREE: TRYING COMMANDS
---

1. The following are all commands you cant ry running in the terminal once you have logged in:

    `cd ~`, `cd`, `ls -lat`, `ls -a`, plus others. All do different things.

    For instance, running `ls -lat` will display something similar to the following:

    ![Image](ls_lat_command.PNG)

    *`ls -lat`  displays a list of files in the directory, as wwell as the dates and times at which they were modified.*

2. You can also log out of the remote server from you terminal by type Ctrl+D or running the command `exit`.

## STEP FOUR: MOVING FILES WITH SCP
---

1. The command `scp`, when run from the client server, can copy file(s) from a client server to a remote server. To use it, run the following command in the same directory as the file you want to copy:

    `scp [file name].java cs15lwi22__@ieng6.ucsd.edu:~/`

2. Then, log back in using ssh, and use the `ls` command to see if your file has been copied into the remote server. If it was successful, you should see the file name.

    ![Image](scp_ls.PNG)

## STEP FIVE: SETTING AN SSH KEY
---

## STEP SIX: OPTIMIZING REMOTE RUNNING
---