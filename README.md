# Burgis_Linux_From_Scratch
A custom Linux distribution built from scratch using the Linux From Scratch (LFS) methodology.  

---

## Overview  
Burgis_Linux_From_Scratch is a minimalist, educational Linux distribution designed for advanced users who want to learn the internals of Linux by building an operating system from source. This project demonstrates the power of customization and the flexibility of Linux systems.  

---

## Key Features  
- Fully built using Linux From Scratch (LFS) version 12.2.  
- Lightweight and highly customizable.  
- Ideal for learning and experimentation with Linux internals.  
- Includes essential tools for development and system management.  

---

## System Requirements  
- **CPU**: 2+ cores (x86_64 architecture).  
- **RAM**: 2GB minimum.  
- **Storage**: 10GB free disk space.  

---

## Linux From Scratch Build Guide (Step by Step chapter by chapter)
I. Introduction
1. Introduction
   - Purpose: Introduces the concept of Linux From Scratch, emphasizing the control and understanding you gain by building a Linux system manually.
   - Purpose: Introduces the concept of Linux From Scratch, emphasizing the control and understanding you gain by building a Linux system manually.
   - Organization: Provides an overview of the book's structure and the major stages of the build.

2. Preparing a New Partition
- **Objective**: Create a dedicated partition for the Linux From Scratch system.
- **Steps**: 
   1. Create and format the partition.
   2. Mount the partition (e.g., /mnt/lfs).
   3. Set up a directory structure for the build.

3. Packages and Patches
- **Objective**: Lists all the software packages and patches needed for the build.
- **Steps**:
   1. Download the required source code and patches.
   2. Verify their integrity using checksums.

4. Final Preparations
- **Objective**: Prepare the environment for building the temporary system.
- **Steps**:
    1. Create a directory for the tools (**/mnt/lfs/tools*) and set ownership.
    2. Set up the $LFS environment variable.
    3. Ensure the host system has the necessary software and compilers.

5. Building the Temporary System
- **Objective**: Build a minimal toolchain for compiling the LFS system.
- **Steps**:
   1. Compile and install Binutils, GCC, and other essential packages in isolation.
   2. Use a staged process to ensure the temporary tools are independent of the host system.

6. Building the LFS System
- **Objective**: Compile and install the core of the LFS system.
- **Steps**:
   1. Recompile toolchain components (Binutils, GCC, etc.) using the temporary toolchain.
   2. Build essential system libraries like Glibc and system utilities.
   3. Build the Linux kernel and install it into the system.

7. Setting Up System Configuration
- **Objective**: Configure the base system for booting and operation.
- **Steps**:
   1. Create configuration files for the bootloader (e.g., GRUB), network, and system services.
   2. Configure essential files like **/etc/fstab* and **/etc/passwd*.
   3. Set system clock, hostname, and locale.

8. Booting the LFS System
- **Objective**: Boot into the new LFS system for the first time.
- **Steps**:
   1. Install and configure a bootloader (GRUB).
   2. Reboot the system and test functionality.

9. 

### 1. Using VirtualBox (Recommended)
To test **Burgis_Linux_From_Scratch** in a virtual environment, follow these steps:

1. **Install VirtualBox** on your system (download from [VirtualBox](https://www.virtualbox.org/)).
2. Open VirtualBox and create a new virtual machine with the following settings:
   - Type: Linux
   - Version: Linux 64-bit
   - Allocate memory: 2GB or more (depending on your system's resources)
   - Create a virtual hard disk with at least 10GB of space
3. When setting up the virtual machine, use the ISO file directly as the bootable disk.
   - Go to the settings of your VM, select **Storage**, and attach the **Burgis_Linux_From_Scratch ISO** to the optical drive.
4. Start the virtual machine. The system should boot from the ISO, and you can follow the installation steps.

---

## Downloads
- **Click here to download the ISO**: [burgis_linux_from_scratch.iso](https://github.com/leighAhs/linuxFromScratch_distro_isoImage)  

how to add additional software

names daw with github repo of each