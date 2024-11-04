**Installation Prerequisites for osTicket**<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket : Prerequisites and Installation</h1>
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
- Notetaking application (Notes for MacOS or Sublime)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/MfsS98Q.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Sign in to Azure Portal
   - Navigate to the [Azure Portal](https://portal.azure.com) and sign in with your Microsoft account credentials. After a successful sign-in, the user will be directed to the Azure dashboard. Navigate to the Virtual Machines icon by clicking on it.  
</p>
<br />

<p>
<img src="https://i.imgur.com/W2prigH.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: On the Virtual Machines page, create a new virtual machine (VM) by clicking on "Create" and selecting "Azure virtual mchine " from the drop down menu list. This will initiate the configuration of the virtual machine beginning with the Basic settings.
</p>
<br />

<p>
<img src="https://i.imgur.com/WNH8m6Y.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
- Remember to save these credenials in a preferred notetaking app like Notes for MacOS, since they'll be needed later on 
- Under the "Inbound port rules" section, "Public inbound ports" will be preselcted by Azure to allow traffic from selected ports. Leave the selected inbound ports: RDP (389) as is
- Please be mindful of the costs of hosting virtual machines on Azure, since it varies depending on a given geographical area
- Remember to check the licensing box and then click on the box "Next : Disks" to continue to the Disk selection page
</p>
<br />

<p>
<img src="https://i.imgur.com/6vPvZB9.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Configure Disks 
   
- Given this virtual machine setup, the Disk selection on this page will be left as is, since it satisfies our lab prerequisites. If it changes for any reason, please use the drop down menus available to configure the OS Disk to match those in the above image
- Click the "Next: Networking" tab to proceed to the Networking page
</p>
<br />

<p>
<img src="https://i.imgur.com/918sEWv.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Configure Networking
   
- On the Networking page, leave everything as is and proceed by clicking on the "Review + Create" tab   
</p>
<br />

<p>
<img src="https://i.imgur.com/hrFZUeU.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Review + Create
   
- On this page, click on the "Review + Create" tab to validate the creation of the WindowsOS virtual machine
- Wait till Microsift Azure validates the process. When the "Validation passed" notification appears on top of the page, proceed to click on the "create" tab below to initiate the creation of the virtual machine 
</p>
<br />

<p>
<img src="https://i.imgur.com/HiJ2YJn.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Deployment in progress:
   
- The deployment of the virtual machine might take some time. Please sit tight. Grab a cup of coffee or tea as you wait. 
</p>
<br />

<p>
<img src="https://i.imgur.com/iSRDmyA.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8: Deployment complete
   
- The notification "Your deployment is complete" confirms the successful creation and hosting of the osTicket virtual machine on Microsoft Azure. Congrats! 
</p>
<br />

<p>
<img src="https://i.imgur.com/AFdCJdL.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9: Navigate back to Azure Services by clicking on the Home tab and navigate to the osTicket Virtual machine by clicking on the Virtual machine tab   
</p>
<br />

<p>
<img src="https://i.imgur.com/5664TXh.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10: On the Virtual machines page, copy the public IP address of the osTicket-VM and save it on an application like Notepad (WindowsOS), Sublime, or Notes (MacOS)
</p>
<br />

<p>
<img src="https://i.imgur.com/qx1VrwT.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 11: Start osTicket-VM 
   
- Proceed to start osTicket-VM by selecting the "Name" box and then click on the "Start" icon 
- Proceed to the Virtual machine confirmation dialogue box
</p>
<br />

<p>
<img src="https://i.imgur.com/kbtgDiu.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 12: Confirm the Virtual machine selection
   
- Proceed by clicking "Yes"
- This will start the osTicket-VM   
</p>
<br />

<p>
<img src="https://i.imgur.com/zk4e0gw.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 13: Check the Notifications box to confirm the Start command was properly executed 
</p>
<br />

<p>
<img src="https://i.imgur.com/pQMZxtx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 14: If not previously installed, proceed to install and open the Windows App (formerly Remote Desktop) on MacOS 

- On Windows App, click on the (+) icon and select "Add PC" to open the "Add PC" dialogue box  
</p>
<br />

<p>
<img src="https://i.imgur.com/PSBUfFN.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 15: Configure the added PC on Windows App

- Retrieve the saved osTicket-VM Public IP address from Step 10 saved on the preferred Note taking APP
- In the Edit PC dialogue box, paste the copied osTicket-VM Public IP address in the "PC name box"
- In the "Friendly name box", type the name "osTicket" and click save
- This will then prompt the opening of the credentials box  
</p>
<br />

<p>
<img src="https://i.imgur.com/4Z90tvS.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 16: Enter Your Credentials

- Retrieve the saved Username and Password for the osTicket-VM previously saved on the preferred Notetaking app in Step 3
- Enter those credentials into the Username and Password boxes respectively
- Click "Continue"
</p>
<br />

<p>   
<img src="https://i.imgur.com/1g1DTQh.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 17: Connect to the RDP Host
   
- RDP stands for Remote Desktop Protocol, which is a proprietary protocol developed by Microsoft. It allows users to connect to another computer over a network connection, using a graphical interface. The "RDP host" refers to the computer that you are connecting to using RDP. This host computer runs the Remote Desktop Services, formerly known as Terminal Services, which enable the remote access
- Role: The RDP host is the target machine that you want to access remotely. It should have Remote Desktop (Windows App) enabled and properly configured to accept incoming RDP connections
- Operating System: Typically, the RDP host runs a version of Windows that supports Remote Desktop Services, such as Windows Server editions or Professional/Enterprise versions of Windows desktop operating systems
- Network Configuration: To access an RDP host over the internet, network configurations such as port forwarding (commonly port 3389) and firewall settings may need to be adjusted to allow RDP traffic
- Security: Using RDP involves security considerations, such as ensuring strong passwords, using network-level authentication, and potentially employing VPNs or other security measures to protect the remote connection
- Usage: Commonly used for administering servers, accessing work computers from home, or providing technical support.   
</p>
<br />

<p>
<img src="https://i.imgur.com/JBGmOwH.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 18: osTicket-VM WindowsOS login interface

- Wait for the osTicket-VM to login
- After the login process, the privacy settings page will emerge
</p>
<br />

<p>
<img src="https://i.imgur.com/KWBIloU.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 19: Privacy Setup page
   
- On the privacy page, set all the highlighted boxes to "NO" because the osTicket-VM lab doesn't require nor depend on those settings to function
- Click the accept button to proceed
</p>
<br />

<p>
<img src="https://i.imgur.com/FNRTFPX.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 20: Launch Microsoft Edge to begin the installation of the osTicket dependencies required for the smooth operation of the osTicket web application
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />





