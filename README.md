# Active-Directory-Project
## Introduction

This project demonstrates the process of setting up an Active Directory environment using VirtualBox. It includes the installation of Windows Server and Windows 10 on VirtualBox, and the configuration of Active Directory services.

Active Directory (AD) is a directory service developed by Microsoft for Windows domain networks. It is a critical component for managing users, computers, and other devices within a network, enabling centralized administration and security. By following this guide, you will gain hands-on experience in setting up and configuring Active Directory in a virtualized environment.

This repository contains detailed steps and screenshots to guide you through each phase of the project. Whether you are a student, IT professional, or enthusiast, this project will help you understand the fundamentals of Active Directory and how to deploy it effectively.

## Prerequisites
**Hardware Requirements:**
- A computer with at least 8GB of RAM (16GB recommended)
- At least 50GB of free disk space

**Software Requirements:**
- VirtualBox: The latest version of Oracle VM VirtualBox
- Windows Server ISO: A copy of Windows Server (2016, 2019, or later) ISO file. You can download a trial version from the Microsoft Evaluation Center.
- Windows 10 ISO: A copy of Windows 10 ISO file. You can download it from the Microsoft website.

**Administrative Access:**
- Ensure you have administrative privileges on your computer to install and configure software.

## Installation Steps
**Installing Windows Server on VirtualBox**

In this part, we will go through the process of setting up a new virtual machine on VirtualBox and installing Windows Server. By the end of this section, you will have a fully functional Windows Server instance running in a virtual environment, ready for Active Directory configuration.

**Step 1: Creating a New Virtual Machine**

In this step, we create a new virtual machine in VirtualBox for our Windows Server installation.

1. Open VirtualBox and click on the "New" button to create a new virtual machine.
2.  Name the VM as DomainController AD.
3. Machine Folder: Assign the VM to the folder D:\VirtualMachine. Ensure you have sufficient space on your hard drive (at least 50GB) to avoid storage issues.
4. Type: Select Microsoft Windows.
5. Version: Choose Other Windows (64-bit).

Click "Next" to proceed to the next step.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/badb17c0-7916-4d05-83f5-3e222060543f)

**Step 2: Configuring Memory and Processors**

In this step, we allocate memory and processors to the virtual machine to ensure good functionality.

1. Memory Size: Allocate 2048 MB (2 GB) of RAM to the VM. This amount of memory will ensure that the Windows Server runs smoothly.
2. Processors: Assign 2 CPUs to the VM. This will provide adequate processing power for the server tasks.

Click "Next" to continue with the configuration.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/a08f6f52-4529-47f7-bdad-77eb7072a0f3)

**Step 3: Configuring Storage**

In this step, we allocate storage space for the virtual machine.

1. Hard Disk: Select Create a virtual hard disk now and click "Create".
2. File Location and Size: Set the size to 50 GB to ensure adequate storage space for the Windows Server installation.

Click "Create" to finalize the storage configuration.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/bb75863c-eaa5-4361-8070-a7c7efb01531)

**Step 4: Summary and Finalization**

In this step, we review the configuration to ensure everything is set up correctly.

1. Summary Screen: Review the details of your new virtual machine, including:
- Name: DomainController AD
- Machine Folder: D:\VirtualMachine
- Type: Microsoft Windows
- Version: Other Windows (64-bit)
- Memory Size: 2048 MB
- Processors: 2 CPUs
- Hard Disk: 50 GB dynamically allocated
2. Verify Configuration: Ensure all settings are correct. If everything looks good, click "Finish" to create the virtual machine.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/88c838b7-1034-43c2-a3fc-50df10f61ed7)

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/40864e83-cbde-4546-8f34-1fec6146cc9a)

**Step 5: Configuring Network Adapters**

Before booting the virtual machine, we need to configure the network adapters to ensure proper connectivity.

1. Open Settings: Select the DomainController AD VM and click on the "Settings" button.
2. Network Settings:
- Adapter 1:
 - Ensure Adapter 1 is enabled.
 - Set Attached to: to NAT. This setting allows the VM to access the internet.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/fcb1ff49-89cb-4b2a-aaeb-edbd46f8293b)

- Adapter 2:
 - Go to the Adapter 2 tab.
 - Check the box to Enable Network Adapter.
 - Set Attached to: to Internal Network. This setting allows communication between virtual machines on the same internal network.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/7cca2ca4-5d47-4067-98f3-c5885d8fed5b)


3. Save Settings: Click "OK" to save the network configuration.

**Step 6: Booting from Windows Server ISO**

After configuring the network adapters, we boot the virtual machine and prepare to install Windows Server by attaching the ISO file.

1. Boot Menu: When the VM boots up, it prompts for a bootable medium.
2. Select ISO: Click on the small folder icon next to the "Optical Drive" dropdown menu.
3. Attach ISO: Navigate to the location where the Windows Server ISO file is downloaded, select it, and click "Open" to attach it.
4. Retry Boot: After attaching the ISO, click "Retry" to boot from the attached ISO file.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/4a4d4f4b-ee81-4a5b-bf56-1bdd9cfc86a3)

By following these steps, the virtual machine will boot from the Windows Server ISO, initiating the installation process.

**Step 7: Windows Server Setup**

Once the virtual machine boots from the Windows Server ISO, the setup process begins.

1.Language Selection: The setup wizard prompts for language preferences. Leave the language settings as default or choose according to your preference.
1.Click "Next" to proceed to the next step of the setup process.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c5a4fd23-2144-4a8b-9cb4-579c61144e89)

By clicking "Next," you advance to the next stage of the installation, where you'll configure additional settings for the Windows Server environment.

**Selecting Windows Server Edition**

1. Edition Selection: From the list of available editions, choose "Windows Server 2022 Standard (Desktop Experience) 64-bit".
2. Click "Next" to proceed with the selected edition.
3. Choosing this edition ensures that you install the full version of Windows Server 2022 with a graphical user interface (Desktop Experience), suitable for most server environments.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b75a2609-42cf-439c-84fc-b6b25575a887)

**License Agreement: Review the license terms provided by Microsoft.**

1. Check the box next to "I accept the license terms" to accept the terms.
2. Click "Next" to acknowledge acceptance and proceed with the installation.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/362b00af-31ac-4062-a626-792cea8a3ad1)

**Choosing Custom Installation**

1.Installation Type: Select "Custom: Install Windows only (advanced)" to perform a custom installation.

Custom Installation allows for more granular control over the installation process, including partitioning and disk configuration. This option is ideal for customizing the installation to specific requirements or preferences.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/be109ca2-52d9-477b-8de6-5bb5f57ea08e)

**Selecting Hard Drive**

1. Hard Drive Selection: Choose the appropriate hard drive or partition where you want to install Windows Server.
   
Once the hard drive is selected, click "Next" to proceed with the installation process.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/271dbc47-1bda-4cac-818e-8b5666bbfbcd)

**Installation in Progress**

1. Installation Progress: The setup process displays a progress bar indicating the status of the installation.
2. Wait for the installation to complete. The time taken for installation may vary depending on the system's performance and the selected installation options.
Do not interrupt the installation process to ensure a successful installation of Windows Server on the virtual machine.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/16da6c42-26a0-4d30-9170-a9a5a1a99d11)









