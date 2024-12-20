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
## I. Introduction
1. **Introduction**
   - Discusses the objectives of building an LFS system, changes since the last release, and book's changelog.
   - Lists resources and places to seek help, like forums and mailing lists.
## II. Preparing for the Build
2. **Preparing the Host System**
   - Outlines the host system requirements and steps to ensure the environment is ready.
   - Covers creating a new partition, formatting it, setting the $LFS variable, and mounting the partition.

3. **Packages and Patches**
   - Lists all required software packages and their corresponding patches for the build process.
   - Introduces downloading and verifying these packages.

4. **Final Preparations**
   - Guides setting up the environment by creating the LFS directory layout, adding an LFS user, and configuring environment variables.
   - Explains SBUs (Standard Build Units) and testing suites.

## III. Building the LFS Cross Toolchain and Temporary Tools
**Important Preliminary Material**
- Introduces toolchain technical notes and general compilation instructions.

5. **Compiling a Cross-Toolchain**
   - Steps for building the initial toolchain:
      - **Binutils Pass 1**: Assembler and linker tools.
      - **GCC Pass 1**: Cross-compiler for C programs.
      - **Linux API Headers**: Interfaces for the Linux kernel.
      - **Glibc**: Core library for GNU/Linux systems.
      - **Libstdc++**: Standard C++ library.

6. **Cross Compiling Temporary Tools**
- Builds utilities for the temporary system, including essential tools like:
   - **M4, Ncurses, Bash, Coreutils, Grep, Sed, Tar,** and others.
- Pass 2 of Binutils and GCC refines the cross-toolchain.

7. **Entering Chroot and Building Additional Temporary Tools**
- Steps for transitioning into the LFS environment using chroot.
- Prepares directories, kernel file systems, and builds essential tools like:
   - **Gettext, Bison, Python, Texinfo,** and others.

## IV. Building the LFS System
8. **Installing Basic System Software**
- Builds the core components of the LFS system:
   - Libraries like **Glibc, Zlib, Xz, Zstd**.
   - Tools like **Binutils, GCC, Bash, Coreutils, Make, Grep, Sed**.
   - System utilities like **Gzip, Shadow, GRUB, Procps-ng, SysVinit**.

9. **System Configuration**
- Configures essential system settings:
   - **Devices and modules**.
   - Network configuration.
   - Locale settings and boot scripts.

10. **Making the LFS System Bootable**
- Finalizes the system with steps to:
   - Configure */etc/fstab* for mounting file systems.
   - Install the Linux kernel.
   - Install and configure GRUB as the bootloader.

11. **The End**
- Wraps up the build process with final steps:
   - Reboot the system into the newly built Linux environment.
   - Provides resources for extending and customizing the LFS system further.

*This summary provides an overview of each chapter's content while maintaining the logical structure of the book.*

## Adding Additional Software from BLFS (Beyond Linux From Scratch)
Once theLinux From Scratch system is built, you can enhance its functionality by installing additional software packages using the Beyond Linux From Scratch (BLFS) book. BLFS extends the LFS system by providing detailed instructions for installing various tools, libraries, and applications.

**Key Points**
   1. **Always Follow the Latest BLFS Book**
   - The latest version of the BLFS book is designed to match the toolchain, libraries, and kernel version used in the most recent LFS book. Ensure that you download the latest BLFS book from the official [LFS/BLFS website](https://www.linuxfromscratch.org/blfs/).
   - Using outdated instructions from older BLFS versions can lead to compatibility issues.
   2. **BLFS Categories of Software**
   - BLFS includes software for various purposes, such as:
      - Networking tools
      - Graphical environments (e.g., **X Window System, GNOME, KDE**)
      - Development tools (e.g., **Git, GCC** extensions)
      - Multimedia applications
      - System administration tools
   3. Dependencies
   - Carefully review the dependencies listed for each package. Some software may require additional libraries or tools to be installed first.
   - **BLFS** provides dependency graphs to simplify this process.

*Visit the Linux From Scratch Website for more information*

## Using an LFS iso make by xorriso 

*This is our own Linux From Scratch system, but the bootable ISO created using xorriso is not identical to the original LFS system. The ISO is bootable, but our original system boots directly on the virtual machine where it was built.*

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
- **Click here to download the ISO**:(Click the *view raw*) [Burgis_Linux_From_Scratch.iso](https://github.com/leighAhs/linuxFromScratch_distro_isoImage/blob/main/Burgis_Linux_From_Scratch.iso)  

## Developers
This LFS system was developed by:  

1. [Leigh Ahsley Gadoc](https://github.com/leighAhs)  
2. [Alden Kev Moser](https://github.com/denkev)  
3. [Justin Clark Trinidad](https://github.com/clrkl)
4. [Maria Dianne Ariñez](https://github.com/Eyahhhh)  
5. [Neil Justin amurao](https://github.com/neilamurao) 
