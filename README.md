# Custom OS Development at Loginware Sofftech

## Objective:
#### The primary goal of my internship was to create a custom operating system (OS) using Buildroot, with customizations based on specific project instructions.

## 1. Setting Up the Virtual Environment
#### I initially installed VM VirtualBox, a hypervisor that enables running multiple OS on a single physical machine. This setup allowed for experimentation with different Linux distributions without altering the host machine.
## Install VirtualBox: Follow the installation instructions for your host OS from the VirtualBox website.
#### Create a New VM
    ```bash
    VBoxManage createvm --name <VM_Name> --register
    VBoxManage modifyvm <VM_Name> --memory <Size_MB> --cpus <Number_of_CPUs> --boot1 dvd --nic1 nat

- ### Tools Used:
- #### VirtualBox for virtualization
- #### Various Linux-based distributions as base systems

## 2. Base OS Selection: Zorin OS
#### I started with Zorin OS (an Ubuntu-based distribution) as a foundation for creating a custom OS using Buildroot.
### - Rationale for Using Zorin OS:
#### - Ubuntu-based: easy to work with.
#### - Stable and user-friendly for initial testing.

## 3.Experimentation with Lightweight Debian Distributions
#### Later, I switched to lighter alternatives: antiX Core and antiX Base, Debian-based minimal distributions optimized for low resource usage.
### - Rationale for antiX OS
#### - Lightweight, ideal for testing in limited environments.
#### - Debian-based, ensuring compatibility with most Buildroot configurations.

## 4. Switching to Yocto Project Due to Buildroot Crashes
#### Due to frequent system crashes while using Buildroot (likely caused by resource constraints), I switched to the Yocto Project, a robust system for creating custom Linux distributions, particularly for embedded systems.
### - About Yocto Project: 
#### - The Yocto Project provides templates and tools for creating custom Linux-based systems, supporting multiple architectures and offering extensive customization options.

### - Advantages of Yocto over Buildroot:
#### - Modular development structure.
#### - Strong support for embedded platforms.
#### - Version control integration with Git.

## 5.Cloning Yocto Project and Poky Repository
- To start with Yocto, I cloned the official repository from GitHub and worked with the Poky reference distribution.
- Commands for Cloning Yocto Project:
  ```bash
  git clone git://git.yoctoproject.org/poky
  cd poky

- Commands to Create a New OS Using Yocto:
  ```bash
  source oe-init-build-env    # Set up the build environment
  bitbake core-image-minimal  # Build a minimal OS image

## 6. Challenges with Yocto Project
- Yocto posed significant challenges due to its complexity and higher system requirements. I faced difficulty managing dependencies and configurations, prompting me to return to Buildroot.

## 7. Using Raspberry Pi OS Lite
- During the process, I also experimented with Raspberry Pi OS Lite, which uses the ARMv8-A architecture. However, VM VirtualBox supports only x86 and AMD64/Intel64 architectures, making it incompatible with Raspberry Pi OS Lite.

### Observation
-Creating a custom OS with Buildroot was much simpler than reconfiguring Raspberry Pi OS Lite due to its architecture and configuration requirements.

## 8. Returning to Buildroot with antiX Base
- After facing issues with Yocto, I returned to Buildroot, using antiX Base for its lightweight design and efficient resource usage.
- Commands for Creating a New OS Using Buildroot:
  ```bash
  git clone https://git.buildroot.org/buildroot  # Clone Buildroot repository
  cd buildroot
  make menuconfig                               # Configure system options
  make                                          # Build the OS

### 9.  Final Outcome: Incomplete Due to System Limitations
- Despite multiple attempts with both Buildroot and Yocto, I could not successfully create a custom OS due to system resource constraints. The development environment experienced frequent crashes, preventing the completion of the project.

## Conclusion
-Although the final goal was not met, the internship allowed me to gain significant experience with tools like Buildroot, Yocto Project, and various Linux distributions. It also deepened my understanding of system architectures, including ARM-based platforms like Raspberry Pi, and provided valuable hands-on experience with OS customization.






