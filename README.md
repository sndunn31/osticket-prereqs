<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial guides you through a step by step process of creating a virtual machine and then outlines the installation process of osTicket within the virtual machine.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Cloud Platform
- Subscription
- Resource Group
- Virtual Network
- Subnet

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/OQ4sRhe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Through the Azure portal create a resource group. Let's name it "osTicket Setup" afterwards search "Virtual Machines" and create a Virtual Machine using Windows 10. Next, click create; A virtual network and subnet will be created for you.
</p>
<br />

<p>
<img src="https://i.imgur.com/nYKfjUm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After logging into the virtual machine, click Windows icon and go to Control Panel. Next, click "uninstall a program", select "Turn Windows features on or off". Look for "Internet Information Services", check box then click "OK"
</p>
<br />

<p>
<img src="https://i.imgur.com/5TdUbB2.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and Install "Web Platform Installer 5.1"
</p>
<br />

<p>
<img src="https://i.imgur.com/gPAoJeq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within Web Platform Installer, search "MySQL 5.5" then select ADD.
</p>
<br />

<p>
<img src="https://i.imgur.com/Qqcxl0Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search for PHP in search bar then add versions PHP 5.6.31 and PHP 7.0.33 (x86) through 7.3 (x86) and make sure you only select the versions ending with (x86). Once done, click "Install"
</p>
<br />

<p>
<img src="https://i.imgur.com/MM0cBCa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Download osTicket v1.15.8 2. Go to File Explorer > Downloads > Right click "osTicket" file and select "Extract All" 
</p>
<br />

<p>
<img src="https://i.imgur.com/kzM6PhH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After extraction is complete. Copy and paste the "upload" folder into c:\inetpub\wwwroot, then rename "upload" folder to "osTicket" within "wwwroot" folder
</p>
<br />

<p>
<img src="https://i.imgur.com/4tmfrwo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS from within Windows then to your right press "restart". 
</p>
<br

<p>
<img src="https://i.imgur.com/N6nHVcC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Double click sites > Default > osTicket. On the right, click "Browse *.80"
</p>
<br />

<p>
<img src="https://i.imgur.com/4xtVnRa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This window should pop up afterwards, showing osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/w7COmaM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS > Under "osTicket" folder, double click "PHP Manager" > "Enable or disable an extension" > Enable: 1. php_imap.dll 2. php_intl.dll 3. php_opcache.dll > Refresh "osticket" website
</p>
<br />

<p>
<img src="https://i.imgur.com/5QXseKU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From File Explorer select "This PC" > Windows (C:) > inetpub > wwwroot > osTicket > include > rename "ost-sampleconfig.php" to "ost-config.php"
</p>
<br />
