<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

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
After successfully logging in, copy and paste the link of the osTicket Installation Zip Folder onto your VM. Download(donot unzip) the folder. Locate the downloaded folder in file explorer, drag/move the folder onto your desktop from file explorer. Afterwards extract(unzip) all files from within the zipped folder. To do so, right-click the folder, click extract all and then click extract. No need to change the extraction location.
</p>
<br />

<p>
<img src="https://i.imgur.com/SQV1HJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After successful extraction, go to the Start menu and type "Control Panel" and hit enter to open the Control Panel. After that click "Programs" and then under "Programs and Features" click "Turn Windows features on and off". Check/Click the box next to Internet Information Services and expand the folder. Under this folder locate another folder named "World Wide Web Services" and expand the folder, then locate another folder named "Application Development Features" and expand it, lastly check the box next to "CGI" and click ok to apply changes to you VM's window features. To confirm that the changes have been applied, go on the web browser and search 127.0.0.1 on the search bar and it should display an IIS(Internet Information Services) page for windows.
</p>
<br />

<p>
<img src="https://i.imgur.com/W7cAAAH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Locate the unzipped osTicket Installation folder on your desktop, enter the folder, and look for a file application called "PHPManagerForIIS" and install it. On the same folder locate windows installer package called "rewrite_amd64" and install it. Open up a new file explorer window and go to your windows C drive, then add a new folder and name it "PHP". Within the osTicket Installation Folder locate another folder called "php-7.3.8-nts-Win32-VC15-x85" and extract the files from this folder onto the folder named PHP that you created earlier. To do so, right click on the folder, click extract all, then click browse and look for the PHP folder which is under the Windows C: drive and then click "Select folder" and then click extract.
</p>
<br />

<p>
<img src="https://i.imgur.com/Ys3z4vn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install application file called "VC_redist.x86". Next install application file called "mysql-5.5.62-win32". During installation make sure to choose "Typical" for setup type. After that, launch the application. Once there you are prompted to select a Server Instance Configuration, make sure you choose "Standard Configuration". Then, you will set up a username and password. After that finish the rest of the installation. Open IIS as an admin. To do so, search IIS on windows search bar, then select "Run as administrator". Once the application is open look for "PHP Manager" and double click to open. Then click "Register a new PHP version". From here you will browse your file explorer(...) and look for a application file called "php-cgi". This file is located under the PHP folder you created earlier within your windows C drive(C:\PHP\php-cgi.exe). Return to IIS Manager home page 
and click "Restart" under the actions panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/nqzMj67.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under the osTicket-Installation-Files folder locate a Compressed(zipped folder named "osTicket-v1.15.8") and extract all files. Once extraction is complete, a folder(unzipped) named "osTicket-v1.15.8", should have appeared. Next, within this folder copy the "upload" folder onto "C:\inetpub\wwwroot" and rename the upload folder as "osTicket". Then reload/restart the IIS manager server. On the left hand side of IIS Manager home, under connections look for "Sites" then expand it and look for "Default Web Site" and expand it and click on "osTicket". Afterwards, on the right panel click "Browse *:80(http)". This should have opened osTicket installer page on the browser, with a message saying "thank you for choosing osTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/zaCGLkJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From here go back to IIS Manager home, double-click osTicket on the left panel and look for PHP Manager. Under PHP Manager look for PHP Extensions, then look for "Enable and disable an extension" and open it. Now you will enable the following extensions, php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket installer page, to see the changes of the extensions added. From the following file path "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" rename the file ost-sampleconfig.php to ost-config.php. Go to the Properties of the file, then go to the Security tab, then go to Advanced and click "Disable Inheritance" and then click "Remove all inherited permissions from this object". Click add and on the top left hand corner click "Select a principal" and add a user/enter an object name by typing a name and then select Full Control, to give full permission to osTicket configuration. To finalize, click "Ok" and "Apply".
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to osTicket Installer on your browser and click continue. Afterwards fill in the system settings for your online helpdesk. Before clicking Install Now, go back to the osTicket Installation folder
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
