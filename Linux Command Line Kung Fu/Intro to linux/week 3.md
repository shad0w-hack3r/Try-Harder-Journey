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
