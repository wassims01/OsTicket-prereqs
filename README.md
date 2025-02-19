<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install IIS 
- Install PHP Manager for IIS
- Install Rewrite Module 
- Create PHP Directory 
- nstall Visual C++ Redistributable
- Install MySQL
- Enable Required PHP Extensions 


<h2>Installation Steps</h2>
Step 1: Create an Azure Virtual Machine

<p>
  <img src="https://i.imgur.com/tPtwjD9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log in to Azure Portal :

  Go to Azure Portal and log in with your credentials.

Create a Windows 10 VM :

Click on "Create a resource" > "Virtual Machine" .
Fill in the required details:
Subscription : Choose your subscription.
Resource Group : Create a new one or use an existing one.
Virtual Machine Name : osticket-vm.
Region : Choose your preferred region.
Image : Select Windows 10 Pro, Version 22H2 - Gen2 (or the latest available version).
Size : Choose a VM size with at least 4 vCPUs (e.g., Standard D4s v3).
Username : labuser.
Password : osTicketPassword1!.
Networking Configuration :
Ensure that Public inbound ports are set to allow RDP (3389) .
Review + Create :
Review all settings and click "Create" to deploy the VM.
Connect to the VM via Remote Desktop :
Once the VM is deployed, go to the VM's overview page.
Click "Connect" > "RDP" .
Download the RDP file and connect using the credentials 
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
