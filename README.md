## Week_1

# Day_0

# Q. What are monolithic and microservices?

  Monolithic architecture is built as one large system and is usually one code-baseIt has shared   database
  Microservices architecture is built as small independent module based on business functionality
  Each project and module has their own database

# Q. What are spirits?
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
		Linux is a open source operating system.	                       While windows are the not the open source operating system.        Unix was developed by AT&T Bell labs and is not	
		Linux is free of cost.	                                              While it is costly.						      open source.
		It’s file name case-sensitive.	                               While it’s file name is case-insensitive.                          Unix is licensed OSUnix is mostly on Servers,	
		In linux, monolithic kernel is used.	                               While in this, micro kernel is used.                               Workstations or PCs.
		Linux is more efficient in comparison of windows.	                While windows are less efficient.                                  Ex:- SunOS, Solaris
		There is forward slash is used for Separating the directories.	While there is back slash is used for Separating the directories.
		Linux provides more security than windows.	                        While it provides less security than linux.

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
 
# Ques. Where are unit files located?

Ans. Unit files are stored in the /usr/lib/systemd directory and its subdirectories, while the /etc/systemd/ directory and its subdirectories contain symbolic links to the unit files necessary to the local configuration of this host.

# Ques. Create a service file for nginx.

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
