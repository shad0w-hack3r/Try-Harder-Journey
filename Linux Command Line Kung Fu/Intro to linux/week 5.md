# System Configuration from the Graphical Interface

## Learning Objectives:
By the end of this chapter, you should be able to:

* Apply system, display, and date and time settings using the System Settings panel.
* Track the network settings and manage connections using Network Manager in Linux.
* Install and update software in Linux from a graphical interface.
  
**gnome-tweaks** can be used, in gnome based linux systems, to perform a lot of customizations related to display e.g. 
  * Changing fonts
  * Change theme
  * Configuring extensions
  * Keyboard layout modification
  * Set programs to run on start-up  
  
Most recent gnome based systems use **gnome-extensions-app** for this purpose.
In most linux distributions display settings can be accessed by right-clicking anywhere on desktop and then clicking on display settings.
By default, Linux always uses UTC time for its own internal time keeping. However the display time or stored time values usually depends on the system time zone settings. These settings can be easily retreived from the settings panel.
c

If the **Automatic Date & Time** setting is on, then the linux system will consult the local time by reliable internet servers.
To check the current dimensions, we can use the following command:
> `xdpyinfo | grep dim

We can easily access the network manager by clicking on top right corner and then either pressing on **settings** option or on wired connected --> wired settings option.
### Installing and updating softwares:

* Debian Packaging:
  * **dpkg** is the underlying pkg manager.
  * Higher level pkg manger is **apt** (advanced package tool).
* Red Hat Packaging:
  * **RPM** is the underlying pkg manager.
  * **Yum** is the higher level pkg manager
* OpenSUSE Packaging:
  * **YaST** (yet another setup tool) is higher level pkg manager. It is a graphical package manager.
  * **RPM** is the underlying package manager.
  * 


