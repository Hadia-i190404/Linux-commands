# Linux-commands
Simple explanation of some Linux commands for the reader's better understanding.
The Linux operating system is an open-source computer operating system. It manages a system's hardware, including its CPU, storage, and memory. The OS connects all of its applications and the physical resources of the system to work seamlessly. The goal of Linux was to be similar to Unix, but it has since evolved to run on a wide range of hardware. Every OS that comes with Linux is built on a set of software packages and the Linux kernel, which is responsible for managing the hardware resources. Organizations can also use Linux servers.
# useradd command
The adduser and useradd commands are similar. The former is a symbolic link that points to the useradd command, while the latter is a command that creates a new user.   
**root@ubuntu:~# useradd JournalDev -d /home/JD**
# usermod command
The usermod command can be used to modify an existing user. It can modify various aspects of the user, such as their permissions and groups.    
**root@ubuntu:~# usermod JournalDev -a -G sudo, audio, mysql**
# dd command
The command is used to copy and convert multiple files from different file systems. Nowadays, it is mainly used to create a bootable USB for Linux. However, there are still some things you can do with it.     
**root@ubuntu:~# dd if = /dev/sdb of = /dev/sda**
# alias command
There are some commands that are used commonly by Linux users.These could be rm -r, ls -l, or tar -xvzf. These commands can help boost your productivity and make your work more efficient. If you frequently use a command, then it’s time that you create an alias. This is a name that you have given to the command that you've defined.     
**root@ubuntu:~# alias lsl="ls -l"**      
OR        
**root@ubuntu:~# alias rmd="rm -r"**
# The firewall interface commands
The Linux kernel's netfilter firewall is composed of two interfaces: the UFW and the IPTables. The former distributes firewall rules to the latter. UFW is very important when it comes to implementing IPTables, as it makes it incredibly easy to set up and manage them. In the example below, we are trying to allow a port 80 connection to our webserver.        
**root@ubuntu:~# iptables -A INPUT -p tcp -m tcp --dport 80 -j ACCEPT**       
**root@ubuntu:~# ufw allow 80**  
# wget command
The wget command is a very important Linux command that will allow you to download files from the terminal. When you specify the link to the file that you want to download, it must be a direct link to it. If the request cannot be made through the wget command, you will get the HTML version instead.         
**root@ubuntu:~ -->> wget <link to file>**    
OR     
**root@ubuntu:~ -->> wget -c <link to file>**    
# ifconfig command
In Linux, we'll be going over the networking section and learning about the various commands that can be used to manage a network. The command ifconfig will allow you to identify all the network interface's IP addresses, MAC addresses, and other details.    
**root@ubuntu:~ -->> ifconfig**   
# traceroute commands
With traceroute, you can specify the IP address, the domain name, or the hostname of the endpoint. The localhost command is just a single hop on the network interface. You can also try this with other IP addresses or domain names to see which routers are taking packets to the destination.   
**root@ubuntu:~ -->> traceroute <destination address>**    
# chown commands
chown command is one of the most important Linux commands. It enables the user to change the file ownership.      
**root@ubuntu:~ -->> chown root:root loop.sh**   
# chmod command
chmod command is also an important command and allows the user to change the file permissions.    
**root@ubuntu:~ -->> chmod +x loop.sh**    
# mount and df commands
When working with Linux, the mount and df commands are very useful tools to get details about the file system and its locations. The command "mount" will allow us to connect the device to a directory and access the files stored on it.     
**root@ubuntu:~ -->> mount /dev/cdrom /mnt**   
**root@ubuntu:~ -->> df -h**   
