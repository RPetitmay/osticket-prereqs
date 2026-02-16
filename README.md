<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Notepad/Notes App (Needed for saving usernames and passwords)

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
<img src="https://i.imgur.com/jZQWfUC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/JzPEKNQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
<ol>
            <li>If using <strong>Windows</strong>, open <strong>Remote Desktop Connection</strong>.</li>
            <li>If using <strong>macOS</strong>, open the <strong>Windows Remote Desktop app</strong>.</li>
            <li>Enter the <strong>IP address</strong> of your virtual machine.</li>
            <li>Enter the <strong>username</strong> associated with the virtual machine.</li>
            <li>Enter the <strong>password</strong> for the virtual machine.</li>
            <li>If you need connection details, locate them in the <strong>Azure Portal</strong> under the <strong>Virtual Machine</strong> section.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/Cz95LZp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
             <h3>osTicket Installation File Transfer and Extraction</h3>
<ol>
            <li>Log in to your virtual machine (VM) successfully.</li>
            <li>Copy and paste the link to the <strong>osTicket Installation Zip Folder</strong> onto your VM.</li>
            <li>Download the folder but do not extract or unzip it.</li>
            <li>Open <strong>File Explorer</strong> and locate the downloaded <strong>osTicket Installation Zip Folder</strong>.</li>
            <li>Drag or move the downloaded folder from <strong>File Explorer</strong> to the <strong>desktop</strong> for easy access.</li>
            <li>Right-click the zipped folder and select <strong>"Extract All"</strong> to unzip the files.</li>
            <li>Once the extraction is complete, a new <strong>unzipped folder</strong> should appear on the desktop.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/SQV1HJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>         
             <h3>Enable CGI for IIS on a Virtual Machine</h3>
<ol>
            <li>Open a web browser and enter <strong>127.0.0.1</strong> in the address bar.</li>
            <li>Confirm that an error page appears, indicating that CGI is not yet enabled.</li>
            <li>Open the <strong>Control Panel</strong> on the virtual machine.</li>
            <li>Click on <strong>Programs</strong>, then select <strong>Programs and Features</strong>.</li>
            <li>Within <strong>Programs and Features</strong>, click <strong>Turn Windows features on or off</strong>.</li>
            <li>In the <strong>Windows Features</strong> window, locate <strong>Internet Information Services folder</strong> and check the box to enable it.</li>
            <li>Expand the <strong>Internet Information Services</strong> folder. </li>
            <li>Check and expand the <strong>Web Management Tools</strong> folder. Ensure that the folders under this folder are all checked.</li>
            <li>Check and expand the <strong>World Wide Web Services</strong> folder. Ensure that the folders under this folder are all checked</li>
            <li>Check and expand the <strong>Application Development Features</strong> folder.</li>
            <li>Only check the box next to <strong>CGI</strong> to enable it.</li>
            <li>Click <strong>OK</strong> to apply the changes.</li>
            <li>Once the changes have been applied, reopen the web browser.</li>
            <li>Enter <strong>127.0.0.1</strong> in the address bar again.</li>
            <li>Confirm that the IIS (Internet Information Services) page now displays, indicating that CGI has been successfully enabled.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/W7cAAAH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
            <h3>Locate and Install Required Components</h3>
        <ol>
            <li>Navigate to the unzipped <strong>osTicket Installation File</strong> folder on your desktop.</li>
            <li>Open the folder and locate the executable file named <strong>"PHPManagerForIIS"</strong>.</li>
            <li>Double-click the file and follow the installation instructions.</li>
            <li>In the same folder, find the <strong>Windows Installer package</strong> named <strong>"rewrite_amd64"</strong>.</li>
            <li>Install the package by double-clicking the file and following the installation steps.</li>
            <li>Open <strong>File Explorer</strong> and navigate to the <strong>C:\ drive</strong>.</li>
            <li>Create a new folder and name it <strong>"PHP"</strong>.</li>
            <li>Within the <strong>osTicket Installation File</strong> folder, locate the directory named <strong>"php-7.3.8-nts-Win32-VC15-x86"</strong>.</li>
            <li>Right-click the folder and select <strong>"Extract All"</strong>.</li>
            <li>Click <strong>"Browse"</strong> and navigate to the <strong>C:\ drive</strong>.</li>
            <li>Select the newly created <strong>PHP</strong> folder and click <strong>"Select Folder"</strong>.</li>
            <li>Click <strong>"Extract"</strong> to complete the process.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/Ys3z4vn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
             <h3>Installation and Configuration Guide</h3>
<ol>
            <li>Install the application file <strong>"VC_redist.x86"</strong>.</li>
            <li>Install <strong>"mysql-5.5.62-win32"</strong>.</li>
            <li>During installation, select <strong>"Typical"</strong> as the setup type.</li>
            <li>After installation, launch the MySQL application.</li>
            <li>When prompted, select <strong>"Standard Configuration"</strong>.</li>
            <li>Set up a <strong>username and password</strong> (ensure you remember these credentials).</li>
            <li>Complete the installation by following the remaining prompts.</li>
            <li>Open <strong>Internet Information Services (IIS) Manager</strong> as an administrator from the Start menu.</li>
            <li>Locate and open <strong>"PHP Manager"</strong>.</li>
            <li>Click <strong>"Register a new PHP version"</strong>.</li>
            <li>In the file explorer window, navigate to <strong>C:\PHP</strong> and select the application file <strong>"php-cgi.exe"</strong>.</li>
            <li>Return to the <strong>IIS Manager</strong> home page.</li>
            <li>Under the <strong>Actions</strong> panel, click <strong>"Restart"</strong> to apply the changes.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/nqzMj67.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
            <h3>osTicket Installation Guide</h3>
<ol>
            <li>Navigate to the <strong>osTicket-Installation-Files</strong> folder.</li>
            <li>Locate the compressed (zipped) folder named <strong>"osTicket-v1.15.8"</strong>.</li>
            <li>Extract all files from the zipped folder.</li>
            <li>Once extraction is complete, an unzipped folder named <strong>"osTicket-v1.15.8"</strong> should appear.</li>
            <li>Open the <strong>"osTicket-v1.15.8"</strong> folder and locate the <strong>"upload"</strong> folder.</li>
            <li>Copy the <strong>"upload"</strong> folder to <strong>C:\inetpub\wwwroot</strong>.</li>
            <li>Rename the copied <strong>"upload"</strong> folder to <strong>"osTicket"</strong>.</li>
            <li>Restart the <strong>IIS Manager</strong> server.</li>
            <li>In <strong>IIS Manager</strong>, locate the <strong>"Connections"</strong> panel on the left.</li>
            <li>Expand <strong>"Sites"</strong>, then expand <strong>"Default Web Site"</strong>.</li>
            <li>Select <strong>"osTicket"</strong>.</li>
            <li>On the right panel, click <strong>"Browse *:80 (http)"</strong>.</li>
            <li>The <strong>osTicket installer page</strong> should now open in a web browser.</li>
            <li>The page should display the message: <em>"Thank you for choosing osTicket."</em></li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/zaCGLkJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
           <h3>osTicket Configuration Guide</h3> 
<ol>
            <li>Open <strong>IIS Manager</strong> and return to the <strong>Home</strong> screen.</li>
            <li>In the left panel, double-click <strong>osTicket</strong> to open its settings.</li>
            <li>Locate and open <strong>PHP Manager</strong>.</li>
            <li>Under <strong>PHP Manager</strong>, find <strong>PHP Extensions</strong> and select <strong>"Enable and disable an extension"</strong>.</li>
            <li>Enable the following PHP extensions:</li>
            <li><strong>php_imap.dll</strong></li>
            <li><strong>php_intl.dll</strong></li>
            <li><strong>php_opcache.dll</strong></li>
            <li>Refresh the <strong>osTicket installer page</strong> to apply the changes.</li>
            <li>Navigate to the following file path: <strong>C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php</strong>.</li>
            <li>Rename <strong>ost-sampleconfig.php</strong> to <strong>ost-config.php</strong>.</li>
            <li>Right-click the <strong>ost-config.php</strong> file and select <strong>Properties</strong>.</li>
            <li>Go to the <strong>Security</strong> tab and click <strong>Advanced</strong>.</li>
            <li>Click <strong>Disable Inheritance</strong>, then select <strong>"Remove all inherited permissions from this object"</strong>.</li>
            <li>Click <strong>Add</strong>, then select <strong>"Select a principal"</strong> in the top left corner.</li>
            <li>Enter a user or object name and select <strong>Check Names</strong> to grant full permissions to the osTicket configuration file.</li>
            <li>For this lab, the object name is <strong>Everyone</strong>.</li>
            <li>Under <strong>Basic permissions</strong> select <strong>Full Control</strong>.</li>
            <li>Click <strong>OK</strong>, then click <strong>Apply</strong> to finalize the changes.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/53GE1kz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
             <h3>osTicket Installation and Database Setup</h3>
<ol>
            <li>Open the osTicket Installer in your browser and click <strong>Continue</strong>.</li>
            <li>Fill in the system settings for your online helpdesk.</li>
            <li>Before clicking <strong>Install Now</strong>, return to the osTicket Installation Files folder and install <strong>HeidiSQL</strong>.</li>
            <li>After installation, HeidiSQL will launch automatically; click <strong>New</strong>.</li>
            <li>Under the <strong>Settings</strong> tab enter the same password you used earlier when setting up the SQL server. Click <strong>Open</strong>.</li>
            <li>Right-click <strong>Unnamed</strong> on the left panel, click <strong>Create New</strong> and then click <strong>Database</strong>.</li>
            <li>Name the database <strong>osticket</strong> and click <strong>OK</strong>.</li>
            <li>Return to the browser, complete the database settings, and click <strong>Install Now</strong>.</li>
            <li>Congratulations! You have successfully completed the osTicket setup.</li>
        </ol>
</p>
<br />

<h2>Conclusion</h2>

In conclusion, I 
