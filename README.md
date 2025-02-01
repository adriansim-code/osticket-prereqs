<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/WRr7XhbUlJg?si=gnZ_EBKK91zSslm4)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Virtual Machine – A VM to host the osTicket system.
- Windows Server with IIS – Internet Information Services for web hosting.
- PHP – Required to run osTicket scripts.
- osTicket Software – The core application to be installed.


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/4Bg7V9y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Start by logging into the Azure Portal and navigating to the Virtual Machines service. Click "+ Create" and select "Azure Virtual Machine". Once it's running, navigate to Virtual Machines in Azure, select your VM, and click Connect > RDP to download the remote desktop file. Use this file to log in to your VM with the previously set credentials. Now, your VM is ready for the osTicket installation process.
</p>
<br />

<p>
<img src="https://i.imgur.com/dLxPCrL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager, select your server, and double-click Handler Mappings. Click Add Module Mapping, enter *.php as the request path, select FastCGI Module, and browse to the PHP executable (C:\PHP\php-cgi.exe). Click OK, then restart IIS. To verify the installation, create a file named info.php in the C:\inetpub\wwwroot directory with the following content: <?php phpinfo(); ?>. Open a web browser and navigate to http://localhost/info.php. If you see the PHP info page, PHP is successfully installed.
</p>
<br />

<p>
  <img src="https://i.imgur.com/VsHIy3e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open a web browser and navigate to http://localhost/setup. Follow the installation wizard, entering your database details (server: localhost, user: root, password: your MySQL root password, database: osticket). Create an admin account, finalize the setup, and delete the setup directory for security purposes. osTicket is now fully installed and ready for use.
</p>
