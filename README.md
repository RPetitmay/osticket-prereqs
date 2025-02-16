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

- Basic/General Understanding of Microsoft Azure
- Azure Subscription/Azure Account(Portal) created
- Resource Group created within your Azure portal
- Windows 10 Virtual Machine(Azure) created within your Azure portal with the Resource Group you've created previously
- <a href= "https://remote-desktop-connection.en.softonic.com/">Remote Desktop Connection(Windows)</a> application or <a href="https://apps.apple.com/us/app/windows-app/id1295203466?mt=12">Windows App(MacOS)</a> application installed onto your PC.
- <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Zip File</a> installed onto PC (needed later for extraction of files)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/jZQWfUC.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Remote Desktop Connection if your using Windows or Windows App if your are using MacOS. Enter the IP address, username and password of your Virtual Machine. All the information needed can be found in your Azure protal virtual machine section. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Cz95LZp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After successfully logging in, copy and paste the link of the osTicket Installation Zip File onto your VM. Download(donot unzip) the folder. Locate the downloaded folder in file explorer, drag/move the folder onto your Desktop from file explorer. Afterwards right-click the folder, click extract all and then click extract. 
</p>
<br />

<p>
<img src="https://i.imgur.com/SQV1HJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After successful extraction, click the Start menu and type "Control Panel" and hit enter to open the Control Panel. After that click "Programs" and then under Programs and Features click "Turn Windows features on and off". Check/Click the box next to Internet Information Services and expand the folder. Under this folder locate folder named "World Wide Web Services" and expand the folder, then locate folder named "Application Development Features" and expand it, lastly check the box next to "CGI" and click ok to apply changes to you VM's window features. To confirm that the changes have been applied, go on the web browser and search 127.0.0.1 and it should display an IIS(Internet Information Services) page for windows.
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

