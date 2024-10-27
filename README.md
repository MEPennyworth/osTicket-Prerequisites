**# osTicket-Prerequisites**<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Windows App for MacOS (Formerly Remote Desktop)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- MacOS </b> (Sequoia 15.1)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine Windows 10, 4 vCPU's
- Windows Server
- Web Server
- osTicket v1.15.8
- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Rewrite Module (rewrite_amd64_en-US.msi)
- Redistributable Package for Microsoft C++ (VC_redist.x86.exe)
- MySQL (mysql-5.5.62-win32.msi) Database
- HeidiSQL Database
- Notepad

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/GHoz8Uj.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Sign in to Azure Portal
   - Go to the [Azure Portal](https://portal.azure.com) and sign in with your Microsoft account credentials. After a successful sign-in, the user will be directed to the Azure dashboard. Navigate to the Virtual Machines icon by clicking on it.  
</p>
<br />

<p>
<img src="https://i.imgur.com/49mhExu.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: On the Virtual Machines page, create a new virtual machine (VM) by clicking on "Create" and selecting "Azure virtual mchine " from the drop down menu list. This will initiate the configuration of the virtual machine beginning with the Basic settings.
</p>
<br />

<p>
<img src="https://i.imgur.com/s60wcaO.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Configure Basic Settings
   
- Subscription: In the subscription box, select the preferred one for the virtual machine set-up
- Resource group: In this box, create a new "Resource group" and name it "osTicket" by clicking on "Create new"
- Virtual machine name: In this box, enter a unique name within the Resource group for the virtual machine, in this case, "osTicket-VM"
- Region: Select the region where you want your VM to be hosted. Based on my location, I chose -  (US) East US 
- Availability options: In this box, the "Availability zone" option is preselected by Azure based on the redundancy needs of this virtual machine
- Security type: Leave as is - "Trusted launch virtual machines"
- Image: Use the drop down menu to select the preferred image for the virtual machine by choosing "Windows 10 Pro, version 22H2 - x64 Gen2"
- Size: Select "standard_d2s_v3 - 2vcpus, 8 GiB memory ($70.08/month) Price will vary based on region
- Username: Enter a username for the administrator account
- Password: Enter a strong password
- Under the Inbound port rules, Public inbound ports will be preselcted by Azure to allow traffic from selected ports. Leave the selected inbound ports: RDP (389) as is
- Remeber to check the licensing box and then click on the box "Next : Disks" to continue to the Disk selection page

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
