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
	

───────────────────────────────────────────────────────────────────────
# Preqequisites
───────────────────────────────────────────────────────────────────────

Make sure you have *Manufacture* SysWin and CygWin

	https://sourceforge.net/p/manufacture/syswin/

	https://sourceforge.net/p/manufacture/cygwin/

VirtualBox has tightened security and is quite difficult to install in custom directories.

	https://www.virtualbox.org/manual/ch02.html#install-win-installdir-req

	
───────────────────────────────────────────────────────────────────────
# Installation
───────────────────────────────────────────────────────────────────────

Best to install it as *root* (*Administrator*) in the default "C:/Program Files/Oracle/VirtualBox"

	wget https://download.virtualbox.org/virtualbox/7.1.4/VirtualBox-7.1.4-165100-Win.exe


* install in C:/work/Oracle/VirtualBox
	
	
───────────────────────────────────────────────────────────────────────
# Configuration
───────────────────────────────────────────────────────────────────────
	
* Set SYSTEM environment variables

	VBOX_HOME=C:\Program Files\Oracle\VirtualBox\
	
	PATH=%PATH%;C:\Program Files\Oracle\VirtualBox\
	
* Link back to it with Junctions

	junction "C:/work/VirtualBox" "C:/Progam Files/VirtualBox"
	 
───────────────────────────────────────────────────────────────────────
# Extension
───────────────────────────────────────────────────────────────────────

* Install Guest Extension Plugins 

	wget https://download.virtualbox.org/virtualbox/7.1.4/Oracle_VirtualBox_Extension_Pack-7.1.4.vbox-extpack
	
* install in C:/Program Files/Oracle/VirtualBox or drag and drop in VBox manager
	
	
═══════════════════════════════════════════════════════════════════════
# (c) Francis Korning 2024.
═══════════════════════════════════════════════════════════════════════
