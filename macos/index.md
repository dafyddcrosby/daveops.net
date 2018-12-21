---
title: macOS
tags: ["macOS"]
---

Keyboard shortcuts
------------------

| Shortcut              | Desc                                    |
|-----------------------|-----------------------------------------|
| cmd + option + escape | bring up 'force quit applications' menu |
| cmd + shift + 3       | take screenshot of all screens          |
| cmd + shift + 4       | take a partial screenshot               |
| cmd + shift + eject   | lock screen                             |


Open application bundle
-----------------------
	open -a APPLICATION


kernel extensions
-----------------
	# list kernel extensions
	kextstat -l
	# unload kernel extensions
	kextunload -b <id>


Update software
---------------
	softwareupdate -h


Search help
-----------
apple key + ? , search for the help menu

Increase maxfiles for session
-----------------------------

	ulimit -n 4096


Remove launch agents
--------------------

	# get launch list
	launchctl list
	# remove item
	launchctl remove <svc>


Use particular nameservers for a domain
---------------------------------------

Create hosts-style file in `/etc/resolver/<domain>`

See `man 5 resolver`


Burn ISO
--------



 hdiutil burn <image>

List disks
----------



 diskutil list

Get linked libraries/object files
---------------------------------



 # List shared libraries
 otool -L <executable>

.. TODO look more into otool's operations

Create a RAM disk
-----------------



 # Replace XXXXX with MB * 2048 (eg a 4 gig is 8388608 (4096 * 2048))
 diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nomount <ram://XXXXX>`

Boot Options
------------


| keypress             | action                             |
|----------------------|------------------------------------|
| Cmd + r              | Recovery Mode                      |
| Option + Cmd + r     | Upgrade to latest compatible macOS |
| Cmd + v              | Verbose Mode                       |
| Cmd + s              | Single-user Mode                   |
| Shift                | Safe Mode                          |
| D                    | Apple Diagnostics / Hardware Test  |
| C                    | Boot removable device              |
| N                    | Boot from network                  |
| Option               | Startup Manager                    |
| Cmd + Option + P + R | Reset NVRAM                        |


Wireless diagnostics
--------------------


All the neat tools for diagnosing busy channels, noise, etc. are in the 'Window' tab

	/System/Library/CoreServices/Applications/Wireless\ Diagnostics.app/Contents/MacOS/Wireless\ Diagnostics


Virtual Memory Stats
--------------------

	vmstat


Links
-----



* <https://opensource.apple.com/>
* <https://github.com/herrbischoff/awesome-osx-command-line>
* <https://www.raywenderlich.com/151741/macos-development-beginners-part-1>


Power management
----------------

``man pmset``

Use ``caffeinate`` to prevent the system from sleeping

Power management
----------------

``man pmset``

Use ``caffeinate`` to prevent the system from sleeping

Power report
------------

A bunch of dtrace under the hood

	/usr/bin/power_report.sh


System/Application defaults
---------------------------

/Library/Preferences and ~/Library/Preferences

``man defaults``

launch services database
------------------------
	dump database
	/System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -dump
	
	#Remove Open With entries
	lsregister -kill -r -domain local -domain system -domain user


System Preference Panes
-----------------------
PreferencePanes framework

/System/Library/PreferencePanes

System config
-------------
scutil - system config utility
- help command in the shell has lots of goodies
- use ``n.add KEY`` + ``n.watch`` to get notified of config changes

Look for memory leaks
---------------------
leaks(1)

System Integrity Protection
---------------------------
csrutil(1)

### Installing fonts
copy to ~/Library/Fonts
