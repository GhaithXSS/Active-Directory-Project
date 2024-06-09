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

**Installation Completed**

After the installation of Windows Server is finished, the system will automatically restart.

Post-Installation Setup: Once the system restarts, it begins the process of finalizing the installation and preparing Windows Server for use.Wait for the system to complete the post-installation setup. This may involve configuring system settings, installing drivers, and performing other tasks.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b7fcb4a6-2514-4802-9e06-fefc2b024c4c)

**Configuring Administrator Password**

Upon restarting and preparing Windows Server for use, you are prompted to set a password for the Administrator account.

1. Password Configuration: Enter a password for the Administrator account. In this example, the password "Password1" is used.
2. Confirm the password by typing it again in the confirmation field.
3. Click "Finish" or "OK" to confirm the password and proceed.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/4f7e1967-9a26-46c2-944c-06ce0f2e3278)

**Logging In as Administrator**

After setting the Administrator password, Windows Server prompts for user authentication before accessing the desktop.

1. Press Ctrl + Alt + Delete: To initiate the login process, press Ctrl + Alt + Delete simultaneously.
2. Login Prompt: Upon pressing Ctrl + Alt + Delete, the login screen appears.
 
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/72dedc4d-7648-4443-9442-817dd7450437)

3. Password: Enter the password previously set for the Administrator account ("Password1" in this example).

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/4e2fdb35-2967-47cb-904a-3b95304ddc49)

4. Press Enter or click "Sign In" to authenticate and access the Windows Server desktop.
Logging in with the Administrator account grants full access to the system, allowing for further configuration and management tasks.

**Windows Server Manager Dashboard**

After successfully logging in, the Windows Server Manager Dashboard automatically appears, providing an overview of server status and management tools.
- Windows Server Manager: The dashboard displays various management options and server status information.
Leave the Server Manager dashboard open for now. We will proceed to install VirtualBox Guest Additions to enhance the virtual machine's performance and functionality.
- The Server Manager Dashboard serves as a central hub for managing server roles, features, and configurations in Windows Server environments.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e3b5a08f-ab2f-4b10-8342-566bf2b43b45)

**Installing VirtualBox Guest Additions**

1. Accessing Guest Additions: Click on the "Devices" menu at the top of the VirtualBox window.
2. Inserting Guest Additions CD: From the "Devices" menu, select "Insert Guest Additions CD Image."
3. Open Explorer: Navigate to "This PC" or "Computer" on the Windows Server desktop.
4. Locating VirtualBox Guest Additions: Open the CD drive labeled "VBoxGuestAdditions" to access the Guest Additions installer.
5. Initiating Installation: Double-click on the "VBoxWindowsAdditions" executable to start the installation process.
6. Performing Basic Setup: Follow the on-screen prompts to complete the installation by clicking "Next," "Next," and "Install."
- Installing VirtualBox Guest Additions provides additional features such as better graphics support, shared folders, and seamless mouse integration between the host and guest operating systems.
  
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/fe790528-a1b5-4980-876c-025b6466a364)

**Renaming the PC to DC**

To facilitate better management and identification, we rename the Windows Server virtual machine to "DC," signifying its role as a Domain Controller.

1. Accessing System Properties: Right-click on the Start button to open the context menu, then select "System."
2. Renaming the PC: In the System window, click on the "Rename this PC" button.
3. Enter New Name: In the "Computer Name" tab of the System Properties window, type "DC" as the new name for the virtual machine.
4. Click "OK" to save the changes and close the System Properties window.
- Renaming the PC to "DC" helps identify its role as a Domain Controller within the Active Directory environment, simplifying management and administration tasks.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b6583f2e-83e9-4915-9f1c-825565190cad)

**Identifying Network Adapters**

To distinguish between the NAT and Internal network adapters, we navigate to Network Connections in the Control Panel.

1. Accessing Network Connections: Open Control Panel by searching for it in the Start menu or right-clicking on the Start button and selecting "Control Panel."
2. Navigating to Network Connections: In Control Panel, go to "Network and Internet" and then click on "Network Connections."
3. Viewing Adapter Options: In the Network Connections window, you will see a list of network adapters installed on the system.
4. Identifying Adapters: Locate the adapters labeled "Ethernet" and "Ethernet 2." In this case, "Ethernet" corresponds to the NAT adapter, and "Ethernet 2" corresponds to the Internal network adapter.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/cf6ebae4-88a5-4ed6-93c9-f785fd47b375)
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/70b251c4-7f18-4e6d-a59d-c2fdd349604e)


**Renaming Network Adapters**

To enhance clarity and management, we rename the network adapters accordingly.

**Renaming Ethernet Adapter:**
1. Right-click on the adapter labeled "Ethernet" and select "Rename."
2. Change the name to "Internal" to signify its connection to the internal network.
**Renaming Ethernet 2 Adapter:**
1. Right-click on the adapter labeled "Ethernet 2" and select "Rename."
2. Change the name to "External" to denote its connection to external networks, such as the internet.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b9a9fe17-a54c-4b1a-bb0a-2cfc18506a6e)

**Configuring LAN IP Address**

**Accessing Adapter Properties:**

1. Right-click on the adapter labeled "Internal" and select "Properties."
2. Selecting Internet Protocol Version 4 (TCP/IPv4):
3. Locate "Internet Protocol Version 4 (TCP/IPv4)" in the list of items and select it.
4. Click on the "Properties" button.
**Configuring IP Address:**
1. Select "Use the following IP address" and enter the following details:
2. IP Address: 192.168.1.1
3. Subnet Mask: 255.255.255.0
4. Click "OK" to apply the changes and close the properties window.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/bceeadf6-5a8c-4aa8-8fc4-c559511e69d7)

**Installing Active Directory Domain Services**

**Accessing Add Roles and Features:**
1. Return to the Server Manager Dashboard.
2. Click on "Add roles and features" to launch the wizard.
3. Selecting Role-Based or Feature-Based Installation:
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/74f4860b-6905-4cb4-9615-34e7b17174da)

4. In the Installation Type section, choose "Role-based or feature-based installation" and click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/994c445c-04e4-45df-8686-5e80b99f4d86)

**Selecting Server:**

1. Choose the local server (in this case, there should be only one server listed) and click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/856693a7-0beb-4dbe-b5a9-0ace293aedd2)

**Selecting Role:**

1. In the Server Roles section, check the box next to "Active Directory Domain Services."

**Adding Features:**

1. Click on "Add Features" when prompted to add required features.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/a939deda-f529-420d-bc08-46e0acdf1136)

**Confirming Installation:**

Review the information on the Active Directory Domain Services page, then click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/04479a3f-b2da-47a1-ab0d-a83e8213df85)

**Installation:**

1. Click "Install" to begin the installation process.
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e4aff721-5e99-4446-b751-c1f2d67dd013)

**Waiting for Installation:**

1.Wait for the installation to complete. The progress will be displayed on the screen.

- The installation of Active Directory Domain Services is a crucial step in configuring the server as a Domain Controller. It establishes the foundation for managing users, groups, and other directory objects within the Active Directory environment.
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/5774b6c4-6fba-4385-b1a4-7f6b4d280fc6)

**Promoting the Server to Domain Controller**

**Accessing Promotion Wizard:**
1. In the Server Manager Dashboard, a notification will appear prompting to promote the server to a Domain Controller. Click on "Promote this server to a domain controller."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c845031b-2dc1-4e4f-92ef-f58be221af5a)

**Choosing Deployment Configuration:**

1. Select "Add a new forest" since this is the initial deployment of Active Directory in our environment. Click "Next."
**Specifying Domain Name:**

1. Enter the root domain name for the forest. In this case, we enter "mydomain.com" as the domain name. Click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e2e24d00-e571-4033-a139-6d718b8776b7)

**Setting Directory Services Restore Mode Password:**

Specify a Directory Services Restore Mode (DSRM) password for the Directory Services Restore Mode Administrator account. Enter the previously set Administrator password and click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/223834e6-6384-4f62-932c-86f52e3239a5)

**Choosing NetBIOS Name:**

The wizard suggests a NetBIOS name based on the domain name. Accept the suggested NetBIOS name or specify a different one if needed. Click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/300500d3-43e2-45ac-907b-a9cc465686c9)

**Paths:**

Review the default paths for the Active Directory database, log files, and SYSVOL folder. Click "Next."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/7403ca15-777a-4c74-a195-f01d00875400)

**Review:**

Review the configuration settings for the Domain Controller. Click "Next" to proceed.
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/1d4753bd-768e-4115-843a-ca0bb408c4e8)

**Installation:**

1. Click "Install" to begin the promotion process.
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/80e0aed4-df8c-4ce3-ad4d-bfdd2bbf2712)

- The promotion of the server to a Domain Controller establishes the Active Directory forest and domain structure, enabling centralized authentication, authorization, and directory services within the network environment.



