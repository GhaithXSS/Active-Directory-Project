# Active-Directory-Project
## Introduction

This project demonstrates the process of setting up an Active Directory environment using VirtualBox. It includes the installation of Windows Server and Windows 10 on VirtualBox, and the configuration of Active Directory services.

Active Directory (AD) is a directory service developed by Microsoft for Windows domain networks. It is a critical component for managing users, computers, and other devices within a network, enabling centralized administration and security. By following this guide, you will gain hands-on experience in setting up and configuring Active Directory in a virtualized environment.

This repository contains detailed steps and screenshots to guide you through each phase of the project. Whether you are a student, IT professional, or enthusiast, this project will help you understand the fundamentals of Active Directory and how to deploy it effectively.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/76e66c94-a451-498f-b715-d4e0586e80bd)

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

**Creating an Administrative User**

We will create an administrative user account for personal use within the Active Directory environment.

**Opening Active Directory Users and Computers:**

1. Open the Start menu, search for "Active Directory Users and Computers," and launch the application.
2. Expand the domain (mydomain.com) in the left pane.
3. Right-click on mydomain.com, then select "New" > "Organizational Unit."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/81139d35-8213-476b-bb6c-c7e291378e81)

4. Name the Organizational Unit "Admins" and click "OK."
![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b0090fbe-bad1-49da-9b4c-594f78d845e3)

**Creating a New User:**

1. Right-click on the "Admins" OU, then select "New" > "User."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/59011441-59af-4623-8d86-4fb31f5e6835)

2. Fill in the user credentials:
- First name: [Your First Name]
- Last name: [Your Last Name]
- User logon name: [Your Username]
3. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/de2fe4fc-23f4-43da-b739-aa52a5d37240)

4. Setting the Password
5. Enter a password and confirm it.
6. Check the box for "Password never expires" (since this is for a home project).

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9f78c0f1-6c1a-44ef-88a0-4e9eb5502545)

7. Click "Next," then "Finish."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/95ccf880-a470-4b72-9918-7429f6bba7ec)


**Assigning Domain Admin Rights:**

1. Right-click on the newly created user and select "Properties."
2. Go to the "Member Of" tab and click "Add."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/de39afe7-a0b1-40a7-8b4d-5458308bca04)

3. In the "Enter the object names to select" field, type "Domain Admins" and click "Check Names" to verify.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/00f3ee03-8af6-4af3-826e-ce28c1e13fcf)

4. Click "OK," then "OK" again to close the properties window.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/df4f6d4f-5535-4473-9556-eb24e9df07fd)

**Verifying the User:**

1. Log out of the current account.
2. At the login screen, select "Other user."
3. Enter the username and password for the new administrative account.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/eb975608-86ab-41e2-aa84-21ded92f1f56)

4. Log in to verify that the new administrative user account has been successfully created and has the appropriate permissions.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/04dbf53c-f4cd-4fc8-9a37-bd23febd8d8a)

By following these steps, you will create a new administrative user account with Domain Admin rights, allowing for enhanced management and administrative capabilities within the Active Directory environment.

**Configuring Routing for Internet Access**

To allow users to access the internet through the server, we will configure routing by installing the Remote Access role.

**Accessing Add Roles and Features:**

1. Open the Server Manager Dashboard.
2. Click on "Add roles and features" to launch the wizard.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9a641352-6719-4ea3-9983-ee070065f756)

**Selecting Installation Type:**

3. In the Installation Type section, choose "Role-based or feature-based installation" and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/618500ad-26ff-4364-83a8-b6ff8951261b)

**Selecting Server:**

4. Select the local server (the server you are configuring) and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/d4d723f7-a988-49e3-b435-799d59f7c93b)

**Selecting Server Role:**

5. From the list of roles, check the box next to "Remote Access."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b966a67f-3abf-4085-8752-a58aa4252494)

6. Click "Next."

**Adding Features:**

7. Click "Next" on the Features page to proceed without adding any additional features.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/f1d2f974-2d73-4f68-8ab9-aeaaeca74303)

8. Click "Next" again on the Remote Access page to continue.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c83239a0-868f-472a-8e4d-9a7c0e4c7553)

**Remote Access Role Services:**

9. Click "Next" on the Role Services page to proceed with the default settings.

**Confirmation and Installation:**

10. Click "Add Features" when prompted to add required features for Remote Access.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/37ba2750-6ea8-4408-bb2c-a23e3c866094)

11. Click "Next" to proceed.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/5efe6f09-d995-4f91-82fb-ef5f435b41ea)

12 .Click "Install" to begin the installation process.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c0abba42-5d11-440b-a8d0-f2bc39601f4e)

13. Wait for the installation to complete.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/ecc4ab07-ef9a-49da-93a3-59a4075b9cce)

- Installing the Remote Access role prepares the server to handle routing and remote access services, which are essential for providing internet connectivity to users within the network. Once the installation is complete, we will proceed with configuring the routing settings to enable internet access.

**Configuring Routing and Remote Access**

To enable routing and provide internet access to users, we will configure the Routing and Remote Access service.

**Accessing Routing and Remote Access:**

1. Open the Server Manager Dashboard.
2. Click on "Tools" in the upper-right corner, then select "Routing and Remote Access."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9ee6ea61-7ae0-4232-9980-6d58100c4ff2)

**Starting the Configuration Wizard:**

3. In the Routing and Remote Access window, right-click on the server name (DC) and select "Configure and Enable Routing and Remote Access."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/2a9aca68-7194-4292-872a-8c0f3e7cc727)

5. The Routing and Remote Access Setup Wizard will pop up. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e6bde9e0-5179-4291-9a8d-ebfd10387a89)

**Choosing Configuration:**

6. Select "Network Address Translation (NAT)" as the configuration option and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/6b117862-a4ac-443b-a721-80436a1c36fb)

**Selecting Network Adapter:**

7. Choose the appropriate network adapter for the internet connection (labeled as "Internet" earlier).

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/49e77e58-5c96-4951-97dc-d82bfc5995d3)

8. Select the "Internet" adapter and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/4b933621-f61b-466f-9bf4-731d281b0582)

**Completing the Setup:**

9. Click "Finish" to complete the configuration.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/aebb008b-41e2-4742-ad0d-2610eb11befa)

- By following these steps, you configure the Routing and Remote Access service to use Network Address Translation (NAT), enabling internet access for users on the internal network. This configuration routes traffic from the internal network through the server, providing a secure and manageable gateway to the internet.

**Installing DHCP Server Role**

To provide dynamic IP addressing to users on the network, we will install and configure the DHCP server role.

**Accessing Add Roles and Features:**

1.Open the Server Manager Dashboard.
2.Click on "Add roles and features" to launch the wizard.

**Selecting Installation Type:**

3. In the Installation Type section, choose "Role-based or feature-based installation" and click "Next."

**Selecting Server:**

4. Select the local server (the server you are configuring) and click "Next."

**Selecting Server Role:**

5. From the list of roles, check the box next to "DHCP Server."
6. Click "Next."

**Adding Features:**

7. Click "Next" on the Features page to proceed without adding any additional features.
8. Click "Next" again on the DHCP Server page to continue.

**Confirmation and Installation:**

9. Click "Install" to begin the installation process.
10. Wait for the installation to complete.
11. Once the installation is complete, click "Close" to exit the wizard.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/de4077d5-1371-4f24-8814-b3f722efaa7b)

- By installing the DHCP server role, we prepare the server to dynamically assign IP addresses to clients on the network. The next step will involve configuring the DHCP settings to define the scope and range of IP addresses that will be assigned to users.

**Configuring DHCP**

After installing the DHCP server role, we configure it to provide dynamic IP addressing to users.

**Accessing DHCP Management:**

1. Open the Server Manager Dashboard.
2. Click on "Tools" in the upper-right corner, then select "DHCP."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9739a289-eda8-4150-9659-369f76c8e0fd)

3. In the DHCP management console, expand the server name (mydomain.com).

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/fadfaa2c-976a-4058-994b-aec13390fe8d)

**Creating a New Scope:**

4. Right-click on "IPv4" and select "New Scope."
5. The New Scope Wizard will open. Click "Next" to begin.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c2523c9f-4cd5-4c3f-9d60-23f33373f93e)

**Naming the Scope:**

6. Provide a name for the scope (e.g., "IP Range 192.168.1.50-192.168.1.200").
7. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/d0b443a9-77db-4554-8a94-ed25349c7a60)

**Configuring IP Address Range:**

8. Enter the starting IP address (192.168.1.50) and the ending IP address (192.168.1.200).
9. Enter the subnet mask (255.255.255.0).
10. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/037bc9f3-0cbb-4d8a-8a3e-99d00a848970)

**Excluding IP Addresses:**

11. If there are any IP addresses you wish to exclude from the scope, you can configure them here. In this case, we don't exclude any addresses.
12. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/7bdd9f5e-6e64-405b-b2e9-f93cc872343b)

**Setting IP Lease Duration:**

13. Set the IP lease duration. In this case, leave it at the default of 8 days.
14. Click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/1daad30c-1c4d-43ff-a1e7-3c80392273a4)

**Configuring DHCP Options:**

15. Click "Next" to proceed with configuring the DHCP options.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c652a902-7e69-491d-bc46-ea7aa5d4a114)

**Adding Default Gateway:**

16. Enter the default gateway, which is the IP address of the Domain Controller (192.168.1.1).
17. Click "Add," then "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e1a18cc4-1fce-4302-8674-ee0ae18ccf05)

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9fe5cb3e-428a-4e85-921d-21de241bb7f5)

**Skipping WINS Server:**

18. Click "Next" to skip configuring a WINS server, as we don't have one.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/1612c068-7d69-442c-b10c-4a3b09de5b68)

**Activating the Scope:**

19. Select "Yes, I want to activate this scope now."
20. Click "Next," then "Finish."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/950c3737-e4b4-4c8f-8899-f0747d9999be)

**Verifying DHCP Status:**

21. Wait a few moments, and the icon next to "IPv4" should turn green, indicating that everything is working fine.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/519e0bcc-66e6-4203-be52-2e96dd9a95e9)

- By following these steps, you configure the DHCP server to dynamically assign IP addresses to clients on the network, ensuring seamless connectivity and management of network resources.


**Adding Users to Active Directory Using a Script**

We will use a PowerShell script to automatically add up to 200 users to Active Directory.

**Downloading the Script:**

1. Download the script file (AD_PS-master.zip).
2. Extract the contents of the zip file to a folder on your server.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b28bdf85-95f4-4983-ae72-13f6b48fc4ac)

**Opening PowerShell ISE:**

3. Open the Start menu, search for "Windows PowerShell ISE," right-click, and select "Run as administrator."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/d7135b8d-0d77-4869-a389-2c9cd0e8158c)

**Loading the Script:**

4. In PowerShell ISE, click on "File" > "Open" and navigate to the folder where you extracted the script.
5. Open the file named Create_Users.ps1.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b7327752-7924-45d8-a997-cd93cb8dfce4)

**Setting Execution Policy:**

6. In the PowerShell command line at the bottom, set the script execution policy to unrestricted by running the following command:

```Set-ExecutionPolicy Unrestricted```

7. Confirm the change when prompted.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e49791e3-9f78-466e-9b43-b4fe3fb18ae3)

**Running the Script:**

8. In PowerShell ISE, click on the "Run" button (green arrow) at the top to execute the script.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/8636c749-21d0-46c7-beb4-a71bb2b639d8)

- The script will run and create the users in Active Directory. Watch the output in the PowerShell ISE window to monitor the progress.

**Verifying User Creation:**

9. Once the script finishes executing, close PowerShell ISE.
10. Open "Active Directory Users and Computers" from the Start menu.
11. Navigate to the "Users" container.
12. Verify that the number of users has increased to 323, indicating that the script successfully added the users.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/d5ef4b01-609d-4fd8-a999-3564554e1fe7)

- By following these steps, you efficiently add a large number of users to Active Directory, streamlining the user management process and demonstrating the power of automation with PowerShell scripts.

## Creating a Windows 10 Virtual Machine in VirtualBox ##

In this step, we will create a new virtual machine for Windows 10 in VirtualBox. 

1. Open VirtualBox and click on the "New" button to create a new virtual machine.
2. Name the VM as Windows 10.
3. Machine Folder: Assign the VM to the appropriate folder (e.g., D:\VirtualMachine).
4. Type: Select Microsoft Windows.
5. Version: Choose Windows 10 (64-bit).
6. Memory Size: Allocate at least 2048 MB (2 GB) of RAM to the VM. More RAM (e.g., 4 GB) is recommended for better performance.
7. Allocate 2 CPUs to the VM.
8. File Location and Size: Set the size to at least 50 GB.
9. Review the configuration summary to ensure everything is correct:
- Name: Windows 10
- Machine Folder: D:\VirtualMachine
- Type: Microsoft Windows
- Version: Windows 10 (64-bit)
- Memory Size: 2048 MB (or more)
- Processors: 2 CPUs
- Hard Disk: 50 GB dynamically allocated
10. Click "Finish" to create the virtual machine.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9ec87837-8e31-4ece-b41d-58bd5cce86dd)

By following these steps, you create a new Windows 10 virtual machine in VirtualBox, ready for the next steps of installation and configuration.

**Configuring the Network Adapter for the Windows 10 VM**

Before installing Windows 10, we need to configure the network adapter for the virtual machine.

**Accessing VM Settings:**

1. In VirtualBox, select the Windows 10 VM and click on the "Settings" button.
2. Go to the "Network" tab.
3. Adapter 1: Ensure that "Enable Network Adapter" is checked.
4. Attached to: Select Internal Network.
5. Name: Choose intnet from the drop-down menu.
6. Click "OK" to save the settings.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/ca0ad048-9fe7-46a1-8888-a4dfb4fdcb7f)

**Installing Windows 10 on the Virtual Machine**

Now, we proceed with the installation of Windows 10 on the configured virtual machine.

**Starting the VM:**

1. Select the Windows 10 VM in VirtualBox and click on the "Start" button.
2. A message will prompt for a bootable medium.
3. Click on "Choose a disk file" and navigate to the location of the Windows 10 ISO file.
4. Select the ISO file and click "Mount."
5. Click on "Retry" to boot from the mounted ISO.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/24b29ae8-2934-4380-bbb2-07ead2a036ef)

**Beginning Windows 10 Setup:**

6. The Windows 10 setup wizard will start. Select the preferred language, time, and keyboard settings.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/c24ac4d9-77d5-43ec-a2dd-f0aed691594e)
  
7. Click "Next," then click on "Install now."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/f7376f5b-345e-4686-97d4-1825f3b04a8b)

8. When prompted for a product key, click "I don't have a product key."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/e1e208de-a455-494b-b67a-5e03acca4c5c)

9. Choose Windows 10 Pro (64-bit) and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/108a3f2c-2517-43f9-a5e1-36df3b40ee81)

10. Accept the license terms by checking the box and clicking "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/d0b9416c-2798-4128-9215-d94598913565)

11. Select "Custom: Install Windows only (advanced)."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/b50022f8-8f48-4152-bf5d-0d8c504eb1ba)

12 Select the hard drive (unallocated space) and click "Next."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/301bbab9-b9a1-4487-aa0d-6f4357baf53b)

-The installation process will begin. This may take several minutes to complete. Once the installation is complete, the VM will reboot automatically.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/8ffc8661-5ee2-4d4f-9aa7-a2a202745a5d)

**Initial Windows 10 Configuration**

After the installation and reboot, perform basic configuration for the network.



13. On the initial setup screen, choose "Continue with limited setup."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/319c8e44-137c-4723-9a74-33e5988412d2)


14.Follow the prompts to complete the basic setup, such as creating a user account and setting up preferences.
15. After a few minutes, the Windows 10 desktop screen will appear.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/bece25fc-4b39-412f-94c2-2367aeb2215e)

- By following these steps, you will have successfully configured and installed Windows 10 on the virtual machine, ready for further network and Active Directory configuration.

**Installing VirtualBox Guest Additions**

To enhance the performance and user experience of the Windows 10 virtual machine, we need to install VirtualBox Guest Additions.

**Renaming the PC and Joining the Domain**

Next, we will rename the Windows 10 machine to Client1 and add it to the Active Directory domain.

1. Right-click on the Start menu and select "System."
2. Click on "Rename this PC."
3. Enter Client1 as the new name and click "Next."
4. A prompt will ask you to restart the computer. Select "Restart later."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/588b779a-ff83-4451-9520-61c188888775)

**Joining the Domain:**

5. Go back to the "System" window.
6. Click on "Advanced system settings."
7. In the System Properties window, go to the "Computer Name" tab and click on "Change."
8. In the "Computer Name/Domain Changes" window, enter Client1 in the "Computer name" field.
9. Select the "Domain" option and enter mydomain.com in the "Domain" field.
10. Click "OK." A prompt will ask for domain credentials.
11. Enter the administrator username and password.
12. A message will appear saying "Welcome to the mydomain.com domain."

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/77e26ba9-ddad-4b61-957a-082155df9da7)

13. Click "OK" and restart the computer to apply the changes.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/6ffa5467-ff00-4e24-8692-598374f948f2)

**Verifying Domain Configuration**

After the reboot, log in with a domain user and verify the network configuration.

14. On the Windows login screen, click "Other user."
15. Enter the domain username (ghaith) and password (Password1).
16. Log in to the system.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/4b2bcc9e-508e-4fcb-ba4c-573b66373a47)


**Verifying Network Configuration:**

17. Open Command Prompt (cmd).
18. Type  ```ipconfig ``` and press Enter.
19. Verify that the IP address is within the range specified by the DHCP scope (e.g., 192.168.1.50 - 192.168.1.200).
20. Check that the Default Gateway is set to the IP address of the Domain Controller (e.g., 192.168.1.1).
21. Type  ```whoami ``` and press Enter.
22. Verify that the output shows mydomain\ghaith.

![image](https://github.com/GhaithXSS/Active-Directory-Project/assets/172057297/9d9fc1b0-55dc-47de-8c2d-8b7c1e9f1af2)

- By following these steps, you will have successfully installed the VirtualBox Guest Additions, renamed the Windows 10 machine, added it to the Active Directory domain, and verified the configuration. The Windows 10 machine is now integrated into your domain environment, with proper network and user configurations in place.

# Conclusion

**This project has demonstrated the complete setup and configuration of an Active Directory environment using VirtualBox. We successfully installed and configured Windows Server as a Domain Controller and a Windows 10 client, integrating them into a functional domain.**

Throughout the process, we covered essential steps including:

- Setting up VirtualBox and creating virtual machines.
- Installing Windows Server and configuring Active Directory.
- Installing Windows 10 and joining it to the domain.
- Configuring network settings, DHCP, and routing for seamless connectivity.
- Adding users to the Active Directory using a script for efficiency.
- Verifying the configurations to ensure proper domain functionality.
- By following this guide, you have gained hands-on experience in deploying and managing an Active Directory environment. This knowledge is fundamental for IT professionals and system administrators, providing a solid foundation for more advanced network and domain management tasks.

**Thank you for following along, and happy learning!**
