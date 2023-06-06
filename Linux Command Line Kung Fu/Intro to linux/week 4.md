# Graphical Interface:

This section discusses briefly about the graphical user interface of Linux systems.

* Loading the graphical desktop is one of the final steps in the linux boot process.
* This was also known as X Windows System or simply X.
* **Display Manager** is a service which keep track of displays being provided and loads the X server or now new system known as **Wayland**.
* DM is responsible for starting the graphics system, logging in the user and starting the user's desktop environment.
* Default DM for GNOME is **gdm** and for KDE is **kdm**.

  <p align="center"><img src=Display%20Manager.png alt="" width="30%" height="30%"></p>

* Basic settings are easily accessible to users but to perform advanced settings users can utilize a utility called as **gnome-tweaks**, which exposes many more settings option.
  > **nautilus** command is use to open File manager directly from terminal.
* To find the recently modified file in /var/log directory we can use following command:
  > `ls -al /var/log/ | sort -M`
