═══════════════════════════════════════════════════════════════════════
# VirtualBox
═══════════════════════════════════════════════════════════════════════

# VirtualBox provisioner

	
<code> 

	#=============================================================================#
	# Manufakture VirtualBox
	#-----------------------------------------------------------------------------#

                                  _____        __      __                        
      _____ _____    ____  __ ___/ ____\____  |  | ___/  |_ __ _________   ____  
     /     \\__  \  /    \|  |  \   __\\__  \ |  |/ /\   __\  |  \_  __ \_/ __ \ 
    |  Y Y  \/ __ \|   |  \  |  /|  |   / __ \|    <  |  | |  |  /|  | \/\  ___/ 
    |__|_|  (____  /___|  /____/ |__|  (____  /__|_ \ |__| |____/ |__|    \___  >
          \/     \/     \/                  \/     \/                         \/ 


	#-----------------------------------------------------------------------------#
	# (c) Francis Korning 2024.
	#=============================================================================#
 	                                                                              
</code>		
	

═══════════════════════════════════════════════════════════════════════
# AUTOMATED Installation
═══════════════════════════════════════════════════════════════════════



───────────────────────────────────────────────────────────────────────
## Preqequisites
───────────────────────────────────────────────────────────────────────

Make sure you have a *Manufacture* SysWin and CygWin full POSIX system running and installed.

	https://sourceforge.net/p/manufacture/syswin/

	https://sourceforge.net/p/manufacture/cygwin/

Manufacture provides the "su.exe" command to run administrator shells (instead of powershell).

In addition to cygwin, you'll probably have a separate gitbash (installed by DockerToolBox).


	
	
───────────────────────────────────────────────────────────────────────
## Installation
───────────────────────────────────────────────────────────────────────

VirtualBox has tightened security and is quite difficult to install in custom directories.

	https://www.virtualbox.org/manual/ch02.html#install-win-installdir-req


install it as *root* (Administrator) in the default "C:/work/VirtualBox/VirtualBox-7.1"

	junction "C:/Progam Files/VirtualBox" "C:/work/VirtualBox" 

	mkdir -p "C:/work/VirtualBox" 

	cd "C:/work/VirtualBox" 


VirtualBox for Windows now only ships as an .exe and no longer ships as an .msi.

However the .exe is a self-extracting .msi package and it can be manually extracted.

	wget https://download.virtualbox.org/virtualbox/7.1.4/VirtualBox-7.1.4-165100-Win.exe


* Choose (a) or (b)
	
a) automatic install (in a windows powershell)

	VirtualBox-7.1.4-165100-Win.exe --extract --path tmp
	
	msiexec /i "tmp/VirtualBox-7.1.4-r165100.msi" INSTALLDIR="C:\Work\VirtualBox\virtualbox-7.1" TARGETDIR="C:\Work\VirtualBox\virtualbox-7.1" /qb


b) manual install in C:/work/VirtualBox/VirtualBox-7.1
	
	
───────────────────────────────────────────────────────────────────────
## Configuration
───────────────────────────────────────────────────────────────────────
	
* Set SYSTEM environment variables

	VBOX_MSI_INSTALL_PATH=C:\work\VirtualBox\VirtualBox-7.1\
	
	VBOX_HOME=C:\work\VirtualBox\VirtualBox-7.1\
	
	PATH=%PATH%;C:\work\VirtualBox\VirtualBox-7.1\
	
	 
───────────────────────────────────────────────────────────────────────
## Extension
───────────────────────────────────────────────────────────────────────

* Install Guest Extension Plugins 

	wget https://download.virtualbox.org/virtualbox/7.1.4/Oracle_VirtualBox_Extension_Pack-7.1.4.vbox-extpack
	
	install in C:/work/VirtualBox/VirtualBox-7.1 or drag and drop in VBox manager
	



═══════════════════════════════════════════════════════════════════════
# MANUAL Installation
═══════════════════════════════════════════════════════════════════════

	
───────────────────────────────────────────────────────────────────────
## Preqequisites
───────────────────────────────────────────────────────────────────────

Make sure you have *Manufacture* SysWin and CygWin

	https://sourceforge.net/p/manufacture/syswin/

	https://sourceforge.net/p/manufacture/cygwin/

In addition to cygwin, you'll want gitbash.

	
───────────────────────────────────────────────────────────────────────
## Installation
───────────────────────────────────────────────────────────────────────

VirtualBox has tightened security and is quite difficult to install in custom directories.

	https://www.virtualbox.org/manual/ch02.html#install-win-installdir-req


Best to install it as *root* (*Administrator*) in the default "C:/Program Files/Oracle/VirtualBox"

	wget https://download.virtualbox.org/virtualbox/7.1.4/VirtualBox-7.1.4-165100-Win.exe


* install in C:/work/Oracle/VirtualBox
	
	
───────────────────────────────────────────────────────────────────────
## Configuration
───────────────────────────────────────────────────────────────────────
	
* Set SYSTEM environment variables

	VBOX_HOME=C:\Program Files\Oracle\VirtualBox\
	
	PATH=%PATH%;C:\Program Files\Oracle\VirtualBox\
	
* Link back to it with Junctions

	junction "C:/work/VirtualBox" "C:/Progam Files/VirtualBox"
	 
───────────────────────────────────────────────────────────────────────
## Extension
───────────────────────────────────────────────────────────────────────

* Install Guest Extension Plugins 

	wget https://download.virtualbox.org/virtualbox/7.1.4/Oracle_VirtualBox_Extension_Pack-7.1.4.vbox-extpack
	
* install in C:/Program Files/Oracle/VirtualBox or drag and drop in VBox manager
	

═══════════════════════════════════════════════════════════════════════
# Operation
═══════════════════════════════════════════════════════════════════════

	vboxmanage
	

The goal is to get this to run:
	
	docker-machine create -d virtualbox default
	
	

	
═══════════════════════════════════════════════════════════════════════
# (c) Francis Korning 2024.
═══════════════════════════════════════════════════════════════════════
