<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- osTicket-Installation-Files
- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- VC_redist.x86.exe.
- MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- HeidiSQL

<h2>High Level Steps</h2>

- Create and log into Vitual Machine and download the osTicket-Installation-Files.zip within the VM
- Install PHP Manager for IIS and Install the Rewrite the Module
- Install VC_redist.x86.exe and MySQL5.5.62 to launch Configuration Wizard
- Open IIS as an Admin and Install osTicket
- Rename: ost-config.php and Install HeldiSQL
- Finsihing the setup of osTicket in the browser



<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/Rq4IaFM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>In this presentation, we will walk through the step-by-step installation of osTicket, a widely used open-source ticketing system, on a Windows 10 virtual machine hosted on Microsoft Azure. The process begins with creating the virtual machine with a name of osticket-vm, configured with 4 vCPUs. Once deployed, we log into the VM using Remote Desktop with the credentials (Username: labuser, Password: osTicketPassword1!). Inside the VM, we download and extract the osTicket-Installation-Files.zip to the desktop, creating a folder named osTicket-Installation-Files, which contains the necessary dependencies for installation.
</p>
<br />

<p>
<img src="https://imgur.com/nGd15j2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>Next, we install Internet Information Services (IIS) with CGI support, ensuring that World Wide Web Services and Application Development Features have CGI enabled. IIS is crucial as it allows us to host web applications like osTicket. After enabling IIS, we proceed with installing the PHP Manager for IIS and the IIS Rewrite Module from the osTicket installation files. These components will help configure and manage PHP settings within IIS, making sure osTicket runs smoothly. Additionally, we create the directory C:\PHP and extract PHP 7.3.8 into this folder, which is a required version for osTicket. We also install VC_redist.x86.exe, an essential Visual C++ Redistributable package, and then install MySQL 5.5.62, configuring it with the root username and password both set to root.

</p>
<br />

<p>
<img src="https://imgur.com/zL5a09R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>With IIS installed, we now configure it to recognize PHP. This is done by opening IIS as an Administrator, navigating to PHP Manager, and registering PHP by linking it to C:\PHP\php-cgi.exe. To apply the changes, we restart IIS by stopping and starting the server. Next, we proceed with installing osTicket version 1.15.8 by extracting the osTicket-v1.15.8.zip file from the installation folder. We move the upload folder to C:\inetpub\wwwroot and rename it to osTicket. Restarting IIS again ensures the newly added files are correctly recognized, and then we browse to the osTicket site by navigating to Sites -> Default -> osTicket in IIS and clicking *Browse :80 to open the web interface.
</p>
<br />

<p>
<img src="https://imgur.com/6MMZpti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>At this stage, osTicket may indicate that some PHP extensions are missing. To resolve this, we return to IIS, open PHP Manager, and enable the necessary extensions: php_imap.dll, php_intl.dll, and php_opcache.dll. After enabling these extensions, we refresh the osTicket installation page in our browser to confirm that the missing dependencies are now enabled. We then rename the configuration file by changing ost-sampleconfig.php to ost-config.php in C:\inetpub\wwwroot\osTicket\include. Following this, we adjust the file’s permissions by disabling inheritance, removing all previous permissions, and assigning “Everyone” full control to allow osTicket to make necessary changes.
</p>
<br />

<p>
<img src="https://imgur.com/6MMZpti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>We then proceed with the final osTicket setup in the browser by providing a Helpdesk Name and Default Email. Next, we install HeidiSQL, a database management tool, and use it to connect to MySQL with the root credentials. Within HeidiSQL, we create a new database called osTicket, which will store all ticket-related data. Returning to the osTicket installation interface, we input the database details: Database Name: osTicket, MySQL Username: root, and Password: root, and click Install Now! to complete the setup. If all previous steps were correctly followed, osTicket should now be installed without errors.
</p>
<br />

<p>
<img src="https://imgur.com/6MMZpti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>After installation, we access the osTicket Admin Panel at http://localhost/osTicket/scp/login.php and the End-User Support Portal at http://localhost/osTicket/.
</p>
<br />

<p>
<img src="https://imgur.com/6MMZpti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>By following these steps, we have successfully set up osTicket on an Azure VM, ensuring that it is configured with all required dependencies and security settings. This installation provides a robust helpdesk system that can be used to manage customer inquiries efficiently. Whether for IT support teams or customer service departments, osTicket offers an intuitive interface for ticket management, making it an excellent choice for organizations seeking a free yet powerful solution.
</p>
<br />
