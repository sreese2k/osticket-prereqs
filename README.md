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

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/Rq4IaFM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>In this project, we installed osTicket, a helpdesk system used for managing support tickets. First, we set up a Virtual Machine (VM) with Windows or Linux and installed the required software: a web server (IIS), PHP, and MySQL. These tools help osTicket run smoothly by handling web pages, scripting, and database storage.

</p>
<br />

<p>
<img src="https://imgur.com/nGd15j2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>Next, we downloaded osTicket from the official website and placed its files in the correct web directory. On Windows, we used the inetpub/wwwroot folder for IIS. We then configure the MySQL database, creating a new database and user specifically for osTicket. After setting correct permissions, we proceed with the web-based installation, where we enter the database details and create an administrator account.

</p>
<br />

<p>
<img src="https://imgur.com/zL5a09R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>After installation, we secured the system by updating the ost-config.php file and adjusting settings in the osTicket dashboard. This included setting up email notifications, ticket categories, and user roles. If needed, we installed extra plugins for more features, like email integration and reporting.

</p>
<br />

<p>
<img src="https://imgur.com/6MMZpti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>Finally, we test osTicket by submitting and resolving sample tickets to verify functionality. We check the email piping feature to ensure tickets can be created via email and confirm that the system correctly tracks, assigns, and resolves support requests. This installation process gives us hands-on experience with server setup, database management, and helpdesk operations, making osTicket a valuable tool for IT support teams.

</p>
<br />
