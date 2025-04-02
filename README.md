<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>osTicket Website</h2>

- ### [osTicket Installation Files](https://docs.osticket.com/en/latest/Getting%20Started/Installation.html)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS with CGI
- Installed PHP Manager for IIS
- Install URL Rewrite Module
- Configure PHP
- Install Visual C++ Redistributable
- Install MySQL
- osTicket Installation
- Configure PHP Extensions
- Configure osTickets Files
- Set Up osTicket in browser

<h2>Installation Steps</h2>


![Screenshot 2025-04-01 142049](https://github.com/user-attachments/assets/80cd9872-9500-4816-9049-2cfb2a5071d8)

<p>
In Windows Control Panel, navigate to Programs, and choose 'Turn Windows features on or off', then enable IIS and the following: World Wide Web Services > Application Development Features > CGI.
</p>
<br />


![Screenshot 2025-04-01 163451](https://github.com/user-attachments/assets/5e57d9d5-3326-431a-988d-a62f45cb9af1)

<p>
Open IIS as Admin. Install PHPManagerForIIS_V1.5.0.msi from osTicket-Installation-Files. Install rewrite_amd64_en-US.msi from the same folder. Make a C:\PHP folder. Unzip php-7.3.8-nts-Win32-VC15-x86.zip into it. Register PHP in IIS with C:\PHP\php-cgi.exe. Restart IIS. Install VC_redist.x86.exe from the folder. Install mysql-5.5.62-win32.msi from the folder.
<br />


![Screenshot 2025-04-01 164949](https://github.com/user-attachments/assets/1a545381-a6bf-4e90-89b7-d74f3f46344e)

<p>
Unzip osTicket-v1.15.8.zip from the folder. Copy upload to C:\inetpub\wwwroot. Rename it to osTicket. 
</p>
<br />


![Screenshot 2025-04-01 225346](https://github.com/user-attachments/assets/9a345d92-6346-44de-a513-7cbb3f0d9fa7)

<p>
Open PHP Manager. Enable php_imap.dll, php_intl.dll, php_opcache.dll. Refresh the site in your browser.
</p> 
<br />


![Screenshot 2025-04-01 230141](https://github.com/user-attachments/assets/4ae2a4e6-b9c4-40a2-9bce-daf9d2398215)

<p>
Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php. 
</p>


![Screenshot 2025-04-01 230717](https://github.com/user-attachments/assets/7c529cf9-bacf-4d01-b299-55e5b72295cf)

<p>
Set its permissions: disable inheritance, remove all, give Everyone full control. (note: this only for turtorial purposes)
</p>


![Screenshot 2025-04-01 231226](https://github.com/user-attachments/assets/1b9deac6-d329-484f-ad4c-65812af3580b)

<p>
Go to http://localhost/osTicket/. Click "Continue". Set Helpdesk Name and Default Email. Install HeidiSQL from the folder. Open it. Create a root/root session. Connect. Make a database called osTicket. In the browser, set MySQL Database to osTicket, Username to root, Password to root. Click "Install Now!".
</p>


![Screenshot 2025-04-01 231857](https://github.com/user-attachments/assets/88ac9008-5f89-4488-91c5-b85a5d553b9e) ![Screenshot 2025-04-01 231927](https://github.com/user-attachments/assets/431393ca-d874-4550-bfbb-5cb84c2af215)

<p>
Check http://localhost/osTicket/scp/login.php for admin login. Check http://localhost/osTicket/ for end users. Ensure no errors. Now you should have access to osTicket as an Admin and a User.
</p>
