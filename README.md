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
# Installation
───────────────────────────────────────────────────────────────────────

VirtualBox for Windows now only ships as an .exe and no longer ships as an .msi.

However the .exe is a self-extracting .msi package and it can be manually extracted.

	mkdir -p C:/work/VirtualBox/VirtualBox-7.1
	
	cd C:/work/VirtualBox/
	
	wget https://download.virtualbox.org/virtualbox/7.1.4/VirtualBox-7.1.4-165100-Win.exe


* Choose (a) or (b)
	
a) automatic install (in a windows powershell)

	VirtualBox-7.1.4-165100-Win.exe --extract --path VirtualBox-7.1.4-165100-Win.msi

	msiexec /i "VirtualBox-7.1.4-165100-Win.msi" INSTALLDIR="C:\Work\VirtualBox\virtualbox-7.1" TARGETDIR="C:\Work\VirtualBox\virtualbox-7.1" /qb


b) manual install in C:/work/VirtualBox/VirtualBox-7.1
	
	
───────────────────────────────────────────────────────────────────────
# Configuration
───────────────────────────────────────────────────────────────────────
	
* Set SYSTEM environment variables

	VBOX_MSI_INSTALL_PATH=C:\work\VirtualBox\VirtualBox-7.1\
	
	VBOX_HOME=C:\work\VirtualBox\VirtualBox-7.1\
	
	PATH=%PATH%;C:\work\VirtualBox\VirtualBox-7.1\
	
	 
───────────────────────────────────────────────────────────────────────
# Extension
───────────────────────────────────────────────────────────────────────

* Install Guest Extension Plugins 

	wget https://download.virtualbox.org/virtualbox/7.1.4/Oracle_VirtualBox_Extension_Pack-7.1.4.vbox-extpack
	
	install in C:/work/VirtualBox/VirtualBox-7.1 or drag and drop in VBox manager
	
	
═══════════════════════════════════════════════════════════════════════
# (c) Francis Korning 2024.
═══════════════════════════════════════════════════════════════════════
