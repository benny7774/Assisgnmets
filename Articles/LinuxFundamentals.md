# Linux Fundamentals

##Components of Linux

	* Bootloader - small codes guide to boot the operating system or by GRUB( GRand Unified Bootloader )

	* OS Kernel - main components for the operating system and it manages I/O devices at hardware level.

	* Daemons - it is background process and it ensures key funcition such as scheluding, printing, Multimedia are working properly

	* OS Shell - it is the computer language interperter which is also caled as command line. It is the interface for OS and Users

	* Graphics server

	* Windows Manager

	* Utilities

## File Hierarchy

	* / - top level directory is the root filesystem

	* /bin - Contains essiential command binaries

	* /boot - contains static bootloader, kernel executable and file requires to boot the OS

	* /dev - Contains device files to facilities access to every hardware device attached the program

	* /etc - Local sysytem configuration files, 

	* /home - Each user for the sysstem has a subdirectory here for storage

	* /lib - shared library that are required to the system boot

	* /media - External removeable device such as USB mounted device

	* /mnt - temporary mount point for filesystem

	* /opt - Optinal file that third party can use the filesystem

	* /root - The home directory for the root users

	* /sbin - The directory contains executable used for system administration

	* /tmp - The operating system and many programs use this directory to store temporary files.

	* /usr - contains executables,libraries,man files, etc

	* /var - it contains variable data files such as log files, email in-boxes, web application related files and more.

## Shell

	Many possiblites to interact with programs and processes to get information faster.

	Tcsh/Csh, Ksh, Zsh,Fish shell and others.

## Prompt Description

	It is easy to understand and, by default, includes information such as the user, hostname and current working directory.

## Getting Help

	It is used get help from terminal because of we dont know from memory or tools we have never seen before. So, we can help ourselves to get familiar with those tools.

## System Information

	In linux system, we need to learn the structure and the information about the system, processes, network configuration, users, directories, user settings and the corresponding parameters.

	* whoami  - display curren user

	* id - returns users identify

	* hostname - prints the name of current host systems

	* uname - prints basic intormation about network interface and system hardware

	* pwd - returns working directory name

	* ifconfig - to view an address to a network interface

	* ip - show routing, network devices, interfaces and tunnels

	* netstat - shows network status

	* ss - Another utility to investigate sockests

	* ps - shows process status

	* who - displays who is logged in

	* env - Prints environment or set and executes command.

	* lsblk - Lists block devices

	* lsusb - Lists USB devices

	* lsof - Lists opened files

	* lspci - lists PCI devices 

## User Management 

	User management is an essential part of linux adminisration. we need to create new user or add other users to specific groups.

	* sudo - execute command as admin

	* su - su utility requests appropriate user crenditials via PAM and switchesto that user ID.

	* useradd - create new user

	* userdel - delete a user account

	* usermod - modifies a user account

	* addgroup - add a group to system

	* delgroup - removes group from system

	* passwd - change user poassword

## Package Management

	It is working as a system administration, maintaining our own linux machines at home or buliding/upgrading/maintaining our penetration testing disturbution of choice. linux package managers and various ways to utilize them to install, update or remove packages.

	* Package downloading

	* Dependency resolution

	* A standard binary package format

	* Common installation and configuration location

	* Additional system-related configuration and functionality

	* Quality control

	Commands are used in the package management are


		*dpkg - it is a tool to install, build, remove and manage debian packages.

		* apt - Apt provides a high-level command-line interface for the package management systems

		* aptitude - it is an alternative to apt is a high-level interface to the package manager

		* snap - install, configure, refresh and remove snap packages.

		* gem - it is the front-end to RubyGems, the standard package manager for Ruby.

		* pip - it is a python package installer recommended for installing python packages.

		* git - it a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.


## Services and Process Management

	Services are relevant services that are required at system startup like perform hardware related tasks and services that are installed by the user.

	Process is 


		* SIGHUP  - it is sent a process when the terminal that controls it is closed

		* SIGINT - sent when a user presses (ctrl+C) in the controlling terminal to interrupt a process

		* SIGQUIT - sent when a user presses (ctrl+D) ro quit

		* SIGKILL - immediately kill a process with no clean-up operations

		* SIGTERM - program termination

		* SIGSTOP - stop the program

		* SIGTSTP - sent whan user presses (ctrl+Z) to request for a service to suspend.

## Working with web service

	Another essential component is the communication with the web servers. They are many different ways to set up web services on linux operating systems. One of the most used and widespread web servers, besides IIS and Nginx is Apache. We create the web pages dynamically using server-side scripting languages.
		Commonly used scrpting languages are PHP,Perl or Rub

## Navigation

	It is used to learn something new is to exoeriment in linux. In linux create,move, edit and delete files and folders. it help to find them on the operating system, differnet types of redirects and what file description.

## Working with Files and Directories

	Create, Move and Copy

		It work with files and directories and learn how to create, rename, move, copy and delete. 

		* touch - to create an empty file

		* mkdir - to create a directory

## Editing Files

	Several ways to edit a file. The most text editors for this is vi and vim. Rarely, nano editor is used.

	* vim  editor - it is an open-source editor for all kinds of ASCIItext. This one is improves version of vi. vim provides an interface to external programs such as grep, awk, sed.

## Find Files and Directories

	Importance of the search

		It is able to find the files and folders. It will be essential to find configuration files, scripts created by users or the administrator and files and folders.

	Which 

		One of the common tools is which. This tool return the path or link that should be executed. It allows us to specfic programs like cURL, netcat, wget, python, gcc are available on the operating system.

	Find

		Another handy tool is find. The function to find files and folders, this tool also contains the function to filter the results. 

	* -type f - we define the type of the searched object. 'f' stands for 'file'.

	* -name *.conf - '-name' we indicate the name of the file we are looking for. The asterisk (*) stands for 'all' files with the '.conf' extension.

	* -user root - option filters all files whose owner is the root user.

	* -size +20k - We can then filter all the located files and specify that we only want to see the files that are larger than 20 KiB

	* -newermt 2020-03-03 - With this option, we set the data.

	* -exec ls -al {}\; - options executes the specified command, using the curly brackets as placeholders for each result.

	* 2>/dev/null - This is a STDERR redirection to the 'null device',which we will come back to in the next section. 

	Locate
		The command locate offer us a quicker way to search through the system. In contrast to the find command, locate works with a local database that contains all information about existing files and folders.

## File Descriptors and Redirections

	File Descriptors

		A file descriptor (FD) in Unix/Linux operating systems is an indicator of connection maintained by the kernel to perform Input/Output(I/O) operations.

		1. Data Stream for Input

			* STDIN - 0

		2. Data Stream for Output

			* STDOUT - 1

		3. Data Stream for Output that relates to an error occurring.

	Filter Contents

		To read files, we do not necessarily have to use an editor for that. There are two tools called more and less, which are very identical.


		* More

		* Less

		* Head

		* Tail

		* Sort

		* Grep

		* Cut

		* Tr

		* Column

		* Awk

		* Sed

		* Wc

		* Practice

Permission Management

		Under linux, permissions are assigned to users and groups. Each user can be a member of different groups, and membership in these groups gives the user specific, additional permissions.

		* (r) - Read

		* (w) - Write

		* (x) - Execute

## Shortcuts

		There are many shortcuts that we can use to make working with Linux asier and faster.

	Auto complete

			[TAB] - Initiates auto-complete. This will suggest o us different options based on the STDIN we provide.

Cursor Movemnet

[ctrl] + A - Move the cursor to the beginning of the current line.

[ctrl] + E - Move the cursor to the end of the current line.

[ctrl] + [left arrow]/[right arrow] - Jump at the beginning of the current/previous word.

[alt] + B/F - jump backward/forward one word.

Erase The Current Line

[ctrl] + U - Erase everything from the current position of the cursor to the beginning of the line.

[ctrl] + K - Erase everything from the current position of the cursor to the end of the line.

[ctrl] + W - Erase the word preceding the cursor position.

Paste Erased Contents

[ctrl] + Y Pastes the erased text or word

End Task

[ctrl]  + c - Ends the current task/process by sending the SIGNT signal.

End-of-File (EOF)

[ctrl] + D - close STDIN pipe that is also known as End-of-File(EOF) or End-of-Transmission.

Clear Terminal

[ctrl] + L - clears the terminal. An alternative to this shortcut is the clear command you can type to clear our terminal.

Background a Process

[ctrl] + z - suspend the current process bt sending the SIGSTP signal.

Search Through Command History

[ctrl] + R - search through command history for commands we typed previously that match our search patterns.

[up]/[down] - go to the previous/next command in the command history.

Switch Between Applications

[alt] + [tab] - switch between opened applications

Zoom

[ctrl] + [+] - Zoom in.

[ctrl] + [-] - Zoom out.


