# Linux
@Linux

force filesystem check on next boot
-----------------------------------


 touch /forcefsck

Socket programming with /dev/tcp
--------------------------------


 exec 3<>/dev/tcp/www.google.com/80
 echo -e "GET / HTTP/1.1\n\n" >&3
 cat <&3

See what services are using a particular port
---------------------------------------------
Run as root:



 lsof -w -n -i (tcp|udp):<port>

or



  netstat -luntp

See if hard drive is on its last legs
-------------------------------------


 smartctl -H /dev/sda

Get reboot/shutdown history
---------------------------


 last -x

Date utility
------------


 # Get the date from a timestamp
 date -d @$TIMESTAMP
 # Get the current time as a timestamp
 date +%s

Find all files with a setuid/setgid bit set
-------------------------------------------


 find / -perm +6000 -type f -exec ls -ld {} \; > setuid.txt &

Burn an ISO from the command prompt
-----------------------------------


 cdrecord -v -data image.iso

Delete user, their home directory, and their mailbox
----------------------------------------------------


 userdel -r [user]

Add user, home directory
------------------------


 useradd -m [user]

Create system user
------------------


 useradd -r [user]

See password policies for user
------------------------------


 chage -l [user]

Fixing missing shared library
-----------------------------

* Create a .conf file in `/etc/ld.so.conf.d/` and put the library's directory in it.
* Run `ldconfig` to reload the system paths


Find files changed in the past day
----------------------------------


 find . -ctime -1 -type f

Disable caps lock
-----------------


 setxkbmap -option ctrl:nocaps

Set time on machine that doesn't have NTP
-----------------------------------------


 date --set="$(ssh user@server date)"

Inter-user communication
------------------------


 # Get list of logged in users
 who
 # Send message to all users
 wall [message]
 # Send message to another user's terminal
 write user [ttyname]
 # Enable/disable terminal message
 mesg [n|y]

Assembly
--------
System call table located at ``/usr/include/asm/unistd.h``
Red Hat syscall man pages installed with ``man-pages`` RPM. ``man 2 syscalls`` for a list, ``man 2 <syscall>`` for the syscall.

Put syscall in EAX, put arguments in other ExX registers, call the interrupt, result usually in EAX

Get filesystems kernel can use
------------------------------


 cat /proc/filesystems


* ☐ <https://perf.wiki.kernel.org/index.php/Tutorial>


Get kernel command line arguments
---------------------------------
@proc
	cat /proc/cmdline


ip command
----------

ifconfig is deprecated, ip was added in Linux 2.2



  # Get IP address
  ip addr
  # Get network interface stats
  ip link
  # Get network interface packet stats
  ip -s link

  # Enable interface
  ip link set eth0 up
  # Set IP address
  ip address add 192.168.1.23 dev eth0

  # Show routing table
  ip route show

Sneaking around the open file limit
-----------------------------------
<https://www.youtube.com/watch?v=_XgXCVULj0o>

Open a pair of domain sockets (with socketpair) that connect to the same
process. Throw the FD in one end, close the FD, then read it out of the other
end. Recursively add the ring buffers...

PipeFS, SockFS, DebugFS, SecurityFS
-----------------------------------
<https://www.linux.org/threads/pipefs-sockfs-debugfs-and-securityfs.9638/>

Kernel resources
----------------

* <https://kernel.org>
* <https://lwn.net/>
* <https://kernelnewbies.org/>
* [Kernel syscalls](https://syscalls.kernelgrok.com/)

