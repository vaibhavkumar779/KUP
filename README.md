## Week_1

# Day_0

# Q. What are monolithic and microservices?

  Monolithic architecture is built as one large system and is usually one code-baseIt has shared   database
  Microservices architecture is built as small independent module based on business functionality
  Each project and module has their own database

# Q. What are sprints?
  Sprint is a set period of time during which specific work has to be completed and made ready for review.Each sprint begins with a planning meeting

# Q. Difference between Agile and DevOps? 

				Agile								DevOps 
		Agile refers to an iterative approach which		DevOps is considered a practice of bringing 
		focuses on collaboration, customer feedback,		development and operations teams together.
		and small, rapid releases.
		Agile helps to manage complex projects.		DevOps central concept is to manage end-to-end engineering processes.
		Agile process focusses on constant changes.		DevOps focuses on constant testing and delivery.

# Day_1

# Q. What is Linux ?
 
 Linux is an operating System combination of GNU/Linux where GNU is the environment of OS which runs on Linux kernel.
 
# Q. Difference between:
			Linux                                          	                                   Windows      					Unix
		Linux is a open source operating system.	                      While windows are the not the open source operating system.        Unix was developed by AT&T Bell labs and is 
		Linux is free of cost.	                                             While it is costly.						    not open source.
		It’s file name case-sensitive.	                              While it’s file name is case-insensitive.                          Unix is licensed OSUnix is mostly on 	
		In linux, monolithic kernel is used.	                              While in this, micro kernel is used.                               Servers,Workstations or PCs.
		Linux is more efficient in comparison of windows.	               While windows are less efficient.                                  Ex:- SunOS, Solaris
		There is forward slash is used for Separating the directories.	While there is back slash is used for Separating the directories.
		Linux provides more security than windows.	                       While it provides less security than linux.

# Q. What are features of  a kernel?

 A core feature of any operating system, the kernel manages communication between hardware and software. The kernel is responsible for managing memory, and I/O 
 to memory, cache, the hard drive, and other devices. It also handles device signals, task scheduling, and other essential duties.
 It is responsible for managing all the 
1. processes 
2. memory files
3. Device Managment
4. Interrupt Handling
5. I/O Communication

# Q. What do you mean by opensource?

  Open source software is code that is designed to be publicly accessible—anyone can see, modify.
 
# Q. Explain the output of "ls -l" command
 
  It give the list of the following directory.
 
# Q.How to create multipple files with single command?
 
  touch file1 file2 file3
 
# Q. Where are unit files located?
 
  /usr/lib/systemd
 
# Q. What are an absolute path and relative path?
 
  Absolute path is exact path where we want to go and relative path is present path
 
# Q. What are hard links?
 
  Hard link are just like copy of that file with same Inodes .
 
# Q. After ll command what is the arrow indicates to and what it is pointing to?
 
  It show the complete detail of files present in that directory . 
 
# Q. What does srv contain and why is it empty?
 
 In this service data is stored i.e. if u want to run the web server , you will store the file here .
 
# Q. Where are unit files located?

 Unit files are stored in the /usr/lib/systemd directory and its subdirectories, while the /etc/systemd/ directory and its subdirectories contain symbolic
 links to the unit files necessary to the local configuration of this host.

# Q. Create a service file for nginx.

Save this file as /lib/systemd/system/nginx.service

[Unit]

Description=The NGINX HTTP and reverse proxy server
After=syslog.target network-online.target remote-fs.target nss-lookup.target
Wants=network-online.target

[Service]

Type=forking
PIDFile=/run/nginx.pid
ExecStartPre=/usr/sbin/nginx -t
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]

WantedBy=multi-user.target

# Day_2

# Q. What is absolute path and relative path?
 
Absolute path: It is defined as specifying the location of a file or directory from the root directory (/).   It is a complete path of a file from the start. E.g., cat /home/sub-dir/file.txt
Relative path: It is a path related to the present working directory. It starts with the current directory and not the root directory. E.g., cat Desktop/file1 

# Q. What are hard links?

A hard link is essentially a label or name assigned to a file. It is possible to create a number of different names that all refer to the same contents. Commands executed upon any of these different names will then operate upon the same file contents.  Even if you delete the original file, the hard link will still has the data of the original file. Because hard link acts as a mirror copy of the original file.

# Q. What does /srv contains and why is it empty?

The /srv/ directory contains site-specific data served by your system. This directory gives users the location of data files for a particular service, such as FTP or WWW. Data that only pertains to a specific user should go in the /home/ directory. 
/srv is empty sometimes as the system might not be hosting any server at that moment. 

# Q. How does cgroups differ from namespaces?

Namespace is a mechanism to limit the visibility that a group of processes has of the system. It makes is possible to run a whole range of application a single machine and ensure none of the other can interfere with one another. 
Cgroups is for limiting the use of resources by a group of processes running on the system. It is used by a group of processes running on a system. 
Mainly the namespaces do not restrict access to physical restrictions but in cgroups they can be restricted. 

# Q. In vim how can we search inside a file?

In vim by pressing escape and getting into the command mode then pressing / and then typing the pattern/word that we want to search the cursor move to it. 

# Q. How to delete a file in vi editor?

By opening a file and pressing escape and getting into the command mode, :!rm <filename> , using this the currently opened file will be deleted.

# Q. Difference between wq and x?
 
If you :x a file in which no changes have been made, the modification time will be untouched because the file isn’t re-saved. The :wq command will alter the modification time no matter what.

# Q. What are hidden files?
 
Hidden files in Linux are the files that are not listed when the user runs ls command. The name of a hidden file starts with a dot(.). Files are hidden in Linux as to make sure that users don’t accidentally modify the contents of these files or accidentaly delete these files. Or files could be hidden for privacy issues. Most hidden files contain environment settings or data that are accessed by programs being run by the user.
 
# Q. How to identify which type file it is?

We can identify a type of file by the colour of the files which are as follows:
-*Blue*: Directory
- *Green*: Executable or recognized data file
- *Cyan*  (Sky Blue): Symbolic link file
- *Yellow with black background*: Device
- *Magenta*  (Pink): Graphic image file
- *Red*: Archive file
- *Red with black background*: Broken link

# Q. What does srv contain and why is it empty?
 
 In this service data is stored i.e. if u want to run the web server , you will store the file here .
 
# Q. What does the mnt directory contain?
 
 temporary mount points for mounting storage devices, such as CDROMs, floppy disks and USB , key drives.

# Q. How does cgroup be different from namespace?

cgroups limit you use 
namespace limit what you can use 

# Q. How to delete files in vim editor?

Shift+d and then y

# Q. Difference between wq and x? 
wq = save and exit 
x = exit without save

# Q. what are hidden files in linux

files used in order to execute some scripts or to store configuration about some services on your host.

# Q. How to identify which type of file is this?

ls -lah

# Q. Why lib,lib64 is in a different color?

Files that can be used for various functions
chang in color may depends upon link, directory, image etc.
