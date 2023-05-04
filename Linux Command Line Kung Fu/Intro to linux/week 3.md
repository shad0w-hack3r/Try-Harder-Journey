# Linux Basics & System Startup:

## Introduction:

This section discusses the linux boot process, from the boot loader into the graphical user interface.

## What is the boot process?

* It is the procedure for initializing the system.
* It consists of everything that happens from, when the computer is first switched on until the UI is fully operational.
  
<p align="center"> <img src="Boot%20Process.png" alt="" width="15%" height="30%"> </p>
<p align="center">The Boot Process</p>

Below is the explanation of each step which is involved in boot process of an x86 based Linux System:
1. BIOS:
   * When the computer is turned ON, the BIOS(Basic Input/Output System) initializes the hardware & tests the main memory.
   * This testing process is called as POST(Power On Self Test).
   * BIOS software is stored in ROM. After this process the remaining boot process is handeld by OS.
  <p align="center"><img src="Boot%20Process-BIOS.png" alt="" width="20%" height="40%"></p>
  <p align="center">BIOS</p>

2. Master Boot Record (MBR), EFI Partition and Boot Loader:
   * After successful POST completion, system control passes to the **boot loader**.
   * Boot loader is usually installed on one of the system storage devices, either in boot sector(for traditional BIOS/MBR systems) or in the EFI partition for recent EFI/UEFI systems.
   * At this stage, information on date, time and most important peripherals are loaded from the **CMOS** values.
   * There are different types of boot loaders for Linux:
       * GRUB
       * ISOLINUX --> (For booting from Removable Media)
       * DAS U-BOOT --> (For booting from embedded devices)
   * When booting linux, the boot loader is responsible for loading the kernel image and initial RAM disk or filesystem into the memory.
   * Initial RAM disk or filesystem contains some critical files and device drivers needed to start the system.
  
  <p align="center"><img src="BIOS%20vs%20UEFI.png" alt="" width="30%" height="10%"></p>
  <p align="center">BIOS vs UEFI</p>

3. Boot Loader in action:
   The boot loader has 2 distinct stages. I will discuss these stages for both BIOS/MBR and EFI/UEFI systems below:
   * BIOS/MBR Systems:
      * The boot loader examines the **partition table** and looks for a bootable partition.
      * Afterwards it searches for a second stage boot loader e.g. GRUB and loads it into RAM.
      * The second stage boot loader resides under **/boot** directory.
      * When this loads, it allows us to choose which OS and or kernel to boot.
      * After OS or kernel is selected then boot loader loads it into RAM and passes control to it.
    * EFI/UEFI Systems:
      * UEFI firmware reads its Boot Manager Data to determine from which disk and partition EFI partition can be found.
      * The firmware then launches the UEFI application, for example GRUB, as defined in the boot entry in the firmware's boot manager.
      * Then the steps are same from there onwards.
  
  
    Some interesting points to note here are:
    * For systems using BIOS/MBR method, boot loader resides at the first sector of the hard disk, also known as MBR.
    * Size of the MBR is 512 bytes.
    * Kernels are almost always compressed, so when they are called by boot loader, they have to uncompress themselves first.

4. Initial RAM Disk:
    * The initramfs contain all the necessary files which are required by kernel to work properly.
    * Also these files contain all the actions which are required to mount the correct root file system.
    * It also contains all the necessary drivers which are required by the kernel.
    * Therefor once the kernel is loaded it looks for initramfs and load it into the memory.
    * Then initramfs provides the necessary tools and drivers to perform tasks such as detecting and configuring hardware devices, loading necessary kernel modules, and preparing the actual root filesystem for mounting.
    * From here the **mount** program instructs the OS that file system is ready for use and associates it with overall heirarchy of file system **(mount point)**.
    * If this mount is successful, **initramfs** gets cleared from the RAM and the **init** program from root file system is executed.
    <p align="center"><img src="The%20Initial%20RAM%20Disk.png" alt="" width="30%" height="20%"></p>

  5. The Kernal:  
    * As discussed earlier, boot loader loads both, initramfs and kernel into the memory.  
    * Once the kernel is loaded into the memory, it immediately performs:
      * Computer Memory initialization and configuration.
      * Configuration of all the attached hardware e.g I/O subsystems, processors and storage devices e.t.c.
  6. /sbin/init and Services:  
    * After setting up all the hardware and root filesystem mounting, now kernel runs **/sbin/init** process.
    * This is becomes the initial process, which then starts other processes to get them running.
    * Most other processes trace their origin ultimately to **init**.
    * **init** process is responsible for keeping the system running and for shutting it down cleanly.
    * It acts as a manager for all non-kernel processes. It cleans up after them upon completion.
  <p align="center"><img src="init%20&%20services.png" alt="" width="20%" height="30%"></p>
  
  # The Boot Process Explained in above steps is an old boot process also known as Serial Process (SysVinit)  
  In this process the system had to pass through a sequence of **runlevels** containing collection of scripts to start and stop services. However all major distributions have now adopted a new method called as **systemd**.
  Why this sequential process has changed?
  Because each stage required completion of its previous stage to proceed further. Thus this startup did not take advantage of ***parallel processing*** that could be done with multiple processors.  
  Following two alternatives were developed:
     * Upstart --> developed by ubuntu and adopted by RHEL 6 and fedora 9 in 2006
     * systemd --> Adopted by fedora first and then it replaced upstart in RHEL and ubuntu as well
  
  <p align="center"><img src=systemd.png alt="" width="30%" height="30%"></p>

  Systemd vs init startup process:
  * Systems using systemd are faster as compared with those, using init. Why? Because these systems now utilize the true power of parallelization techniques which allow multiple services to be run simultaneously.
  * Complicated startup scripts present in init are now replaced with simpler configuration files.
  * **/sbin/init** now refers to **/lib/systemd/systemd**.
  * One simple systemd command **"systemctl"** is use to start, stop or check the status of the service.  
  > ` systemctl start|stop|restart|status name.service `

  # Linux File System: