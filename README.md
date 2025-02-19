<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/9-Lji9myM-o)

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
Step 2: Download and Unzip osTicket Installation Files

<p>
<img src="https://i.imgur.com/GfV4Hmr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install IIS :
Open Server Manager .
Click "Add roles and features" .
In the Web Server (IIS) section, enable the following:
World Wide Web Services > Application Development Features > CGI .
Install PHP Manager for IIS :
Navigate to the osTicket-Installation-Files folder.
Run PHPManagerForIIS_V1.5.0.msi and follow the installation wizard.
Install Rewrite Module :
Run rewrite_amd64_en-US.msi from the same folder
</p>
<br />


<p>
Step 3: Install and Configure IIS with CGI

 <img src="https://i.imgur.com/fu8JC6W.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Install IIS :
Open Server Manager .
Click "Add roles and features" .
In the Web Server (IIS) section, enable the following:
World Wide Web Services > Application Development Features > CGI .
Install PHP Manager for IIS :
Navigate to the osTicket-Installation-Files folder.
Run PHPManagerForIIS_V1.5.0.msi and follow the installation wizard.
Install Rewrite Module :
Run rewrite_amd64_en-US.msi from the same folder.
<p>
Step 4: Set Up PHP
  <img src="https://i.imgur.com/bkl9Rxj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Create PHP Directory :
Create a folder at C:\PHP.
Unzip PHP :
Extract php-7.3.8-nts-Win32-VC15-x86.zip into C:\PHP.
Install Visual C++ Redistributable :
Run VC_redist.x86.exe from the osTicket-Installation-Files folder.
Register PHP in IIS :
Open IIS as an administrator.
Go to PHP Manager > Register new PHP version .
Point to C:\PHP\php-cgi.exe.
Reload IIS :
Stop and start the IIS server from the IIS Manager.
<p>

  Step 5: Install osTicket

  
<img src="https://i.imgur.com/uxLjnEQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Prepare osTicket Files :
Unzip osTicket-v1.15.8.zip from the osTicket-Installation-Files folder.
Copy the upload folder into C:\inetpub\wwwroot.
Rename upload to osTicket.
Reload IIS :
Stop and start the IIS server again.
Enable Required PHP Extensions :
Open IIS Manager.
Go to Sites > Default Web Site > osTicket .
Double-click PHP Manager .
Enable the following extensions:
php_imap.dll
php_intl.dll
php_opcache.dll.
Rename ost-sampleconfig.php :
Navigate to C:\inetpub\wwwroot\osTicket\include.
Rename ost-sampleconfig.php to ost-config.php.
Set Permissions for ost-config.php :
Right-click ost-config.php > Properties > Security .
Disable inheritance and remove all inherited permissions.
Add a new permission for Everyone with Full Control .

</p>
Step 6: Complete osTicket Installation
<img src="https://i.imgur.com/Rt1ooja.pngheight="80%" width="80%" alt="Disk Sanitization Steps"/>
Access the Installation Page :
Open a browser and go to http://localhost/osTicket/setup.
Follow the on-screen instructions:
Helpdesk Name: Enter a name for your helpdesk.
Default Email: Enter an email address for customer support.
MySQL Database: osTicket.
MySQL Username: root.
MySQL Password: root.
Finalize Installation :
Click "Install Now!" .
If successful, you should see a confirmation message.

<br />
