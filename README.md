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

- OS Ticket
- PHP
- PHP Manager
- IIS Rewrite Module
- Microsoft Visual C++ Redistributable
- MySQL
- HeidiSQL

<h2>Installation Steps</h2>
After downloading all the prerequisites go to control panel, turn Windows features on or off, and enable the following.
Internet Information Services, and CGI. (Internet Information Services World Wide Web Services -> Application Development Features)
</p>
<p>
<img src="https://i.imgur.com/FzvTdiX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager and IIS Rewrite Module.
</p>
<br />
<p>
<img src="https://i.imgur.com/xgYdUM5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/18il4Md.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Crate a folder in C: drive named PHP, and transfer the contents of the PHP zip file into the PHP file in C: Drive.
</p>
<br />
<p>
<img src="https://i.imgur.com/kdjHyZC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/m5y3aAa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Microsoft Visual C++ Redistributable and MySQL 

Note: for MySQL use Typical Setup, and Standard Configuration

Note: MySQL and HeidiSQL use the same password
</p>
<br />
<p>
<img src="https://i.imgur.com/CqiOBdo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ZsOJjo6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Start Internet Information Services Manager as admin, go to PHP manager,register new php version, and select the php-cgi.exe from Your C: Drive
</p>
<br />
<p>
<img src="https://i.imgur.com/94CRsFT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GxwLujF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/tGcnVUp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ezauWJW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Copy the upload folder from the zip OSticket folder to wwwroot (C:\inetpub). rename upload to osticket
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS Manager. 
  
Use the drop down to get to osticket,double click on PHP Manager click on Enable or Disable an extention, and enable the following 
  
  php_imap.dll 
  
  php_intl.dll 
  
  php_opcache.dll

</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to the include folder in C: Drive (C:\inetpub\wwwroot\osticket) and rename ost-sampleconfig.php to ost-config.php.asd
Then, disable inheritence (right click ost-config, properties, security, advance) and add new full access permissions (still in advance settings, add, select new principal, type everyone, full control)
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Intall HeidiSQL and create a new session with the password you created from MySQL. 
  
Then add a new database named os ticket ( right click on Heidi, Create new, Database)
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to IIS Manager go to os ticket through the drop down and click on Browse*:80, click continue, enter your user and password from HeidiSQL MYSQL Database is Osticket.
Fill in the rest of the information by tourself then click install.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Delete the setup folder (C:\inetpub\wwwroot\osTicket) and change ost-config.php to read only
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Congrats you've install os ticket for guest login use http://localhost/osTicket/

For agents and admins use  http://localhost/osTicket/scp/login.php
