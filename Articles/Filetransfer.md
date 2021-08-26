nsfer

	It is used to transfer the file from or to the target system. File transfer may successfully web exploit a web application vulnerabilities. There are many ways to transfer the file by the scripts, binaries and tools.

	File Transfer is the core event of an operating system. This module covers techniques that leverage tools and application commonly on windows and Linux System.

## Windows File Transfer Methods

### PowerShell

	HTTP/HTTPS traffic is allowed out of the firewall in some form - and if we have a GUI session, a web browser could also be used. From a windows shell, Powershell offers many file transfer options. In any version of powershell.

	The aliases iwr,curl and wget can be used instead of invoke-webrequest.

	Using powershell can upload and download the files from server or website.

## Linux File Transfer Methods

	Wget and cURL are installed on may linux distributions and support uploading as well as downloading files.

	OpenSSL is frquently installed and is also often included in other software distributions, with sysadmins using it to generate security certificates.

	Bash(/dev/tcp) is built in /dev/tcp device file can be used for simple file downloads.

	PHP is also very prevalent and provides multiple file transfer methods.

	Python is often present on Linux and can be used to download files when Wget and cURL are not available. It isn't currently installed by default in windows. 

	Other languages which are used Ruby, Perl and Golang are some other popular languages that can also transfer files.

## Catching Files over HTTP/SMB

### HTTP/S

	Most common way most people will transfer files between HTTP/HTTPS are the most common protocols allowed through the firewalls. The file will be encrypted in transit. The penetration test and clients network IDS picks up on a sensitive file being transferred over plaintext and having them ask why we sent a password to our cloud server without using encryption.

Nginx Enable PUT

	A good alternative for transferring files to Apache is NGINX because it is configuration is less complicated, and the module system does not lead to security issues like Apache can do.

### SMB

Impacket SMBServer

	Impacket is my preferred method of setting up a file transfer iver SMB because it does not run in the background or involve modifying configuration files. We can use smbserver.py specifically. If other people attempt to connect to the service, it has the bonus that it will display aNETNTLMv2 hash that, if successfully cracked, will reveal the password.

## Web Servers

	Apache and NGINX are possible to stand up a web server using various languages. A compromised linux machine may not have a web server installed or access to the internet.

## SMB/WebDAV 

	SMB is a good option for file transfers, as on Windows as you don't need to install anything. SMB traffic features prominently on networks, and SMB file transfers to windows computers sre expected. Unfortunately, it's also the case that outbound SMB traffic is often allowed through the external firewall. 

Powershell

	Copy-item, Set-Content, Copy/xcopy/robocopy, Map/Mount Drives

Netcat

	Netcat is a very versatile tool that also allows file transfers. The target or attacking machine can be used to initiate the connection, which is useful if a firewall prevents access to the target. The commands below both result in Mimikatz being transferred to the target computer.

SCP

	The OpenSSH client is available by default on linux and has been included in windows 10 and windows server 2019. On windows open SSH server can be enabled using this procedure. On older windows systems, the PuTTY Secure Copy client.

Echo Copy

	Echo copying files is very inefficient and can result in a large amount of data being transferred across the clipboard. So, we can use an executable acker such as UPX to make the source file as small as possible.

OpenSSL base64

	If OenSSL is available on the target system, this can also be used to encode and decode the data in place of certutil.

## Protected File Transfers

	As penetration testers, we often gain access to highly sensitive data such as user lists, credentials, enumeration data that can contain key information about the organization network infrastructure and active directory environments. It is essential to encrypt such information or use encrypted data connections such as SSH, SFTP, and HTTPS.

File Encryption on Windows


	Many different methods can be used to encrypt files and information on Windows systems. One of the simplest methods is the Invoke-AESEncryption.ps1 PowerShell script.

Detection

	Command-line detection based on blacklisting is straightforward to bypass, even using simple case obfuscation. However, although the process of whitelisting all command-lines in a particular environment is initially time-consuming, it is very robust and allows for quick detection and alerting of any unusual command-lines.

## Evading Detection

Changing User-Agent

	In case diligent administrators or defenders have blacklisted any of these User Agents, Invoke-WebRequest contains a UserAgent parameter, which allows for changing the default user agent to one emulating Internet Explorer, Firefox, Chrome, Opera, or Safari. 

LOLBAS / GTFOBins

	Application whitelisting may prevent you from using PowerShell or Netcat, and command-line logging may alert defenders to your presence. In this case, an option may be to use a "LOLBIN" (living off the land binary), alternatively also known as "misplaced trust binaries".


