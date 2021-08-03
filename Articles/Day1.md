Introduction
I am Benedict, I join Surfboard as Intern on 2nd August. I am here to learn networking from the basics of networking. On our first day we are learned about basic fundamentals of the program which are
	* Reading
	* Writing
	* Mathematical Thinking
	* Problem Solving
	* Resourcing 
	* Breaking down and Synthesing
	* Typing
	* Creativity
which are following in the internship program to develop our self.

To create file and folder
	After, we completing our basic fundamentals and we learning about CentOS which is  Linux Operating System.
We are learning to create a Folder, File and we are learning to to list the files or folder in directory by using liunx command. The commands are we are learn are ls, ln, mkdir, cd, touch, vi, cp, sudo

	* ls command is used to view in  the files and folder in a directory. 
	* ln command is
	* mkdir command is used for to create a folder
	* touch command is used to create a file
	* cd command is used to change the dicectory path
	* vi command is used to open and edit the text file
	* cp command is used to copy a folder or file from a dirtectory
	* sudo command is used for assign the command as admin or root user
	* ../ command is used for going back from directory

By using this command we are created folders and copy foilder from one to another by the copy command. Then we are going to create a text file by touch command which is used for to create a .txt file or someother files. We using vi command for to view and edit the .txt file which was created by us, in the that .txt file "esc" is used for command," i" is used for insert or edit the .txt file and "v" is used to visual on the display.
In command mode we are using some keywords are to save, redo, undo, moving the line, selecting the word or line and quit.
	* ":w" is used for save the .txt file
	* "u" is used for undo the word or line
	* "cntrl + r" is used for redo the word or line
	* ":(number)" is used for for selecting line eg.:":3"
	* "h, j, k, l" the keys are used to move and select up(k),down(j), right(l), left(h)
	* for copy and paste in the text editor we are using "y" for copy and "p" for paste
	* for delete the entire line by using "dd"
	* "^" is used for move cursor to start of line
	* "&" is used for move cursor to end of line
	* "G" is used for to move the cursor in top of the line
	* "gg" is used to move the cursor in bottom of the line
	* ":wq" is used for save and quit

To Enable GUI
	* After, completing that we are working on change the terminal mode to GUI mode by these commands
	* To find the GUI package by this command "yum group list" if "Server with GUI", "GNOME Desktop" and "Graphical Administation Tools" which are installed or not
	* Then we go to install by these command to promote the terimal to GUI " yum groupinstall "GNOME Desktop" "Graphical Administrator Tools"
	* If didn't work try to add sudo before that command and again to promote the GUI server by "yum groupinstall "Server with GUI"
	* To enable the GUI system Startup by this command " ln -sf /lib/systemd/system/runlevel5.target /etc/systemd/system/default.target"
	* When it all done to see the output of GUI by the command "reboot" and you will get the centOS 7 GUI

