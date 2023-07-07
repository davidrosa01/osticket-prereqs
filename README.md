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

- Install / Enable IIS in Windows WITH
CGI, Common HTTP Features and IIS Management Console
- Install PHP Manager for IIS
- Install the Rewrite Module
- Download PHP and unzip the contents into C:\PHP
- Install VC_redist.x86.exe
- Install MySQL 5.5.62


<h2>Finalizing osTicket Install</h2>

<p>
<img src="Screen Shot 2023-07-06 at 5.47.54 PM" height="80%" width="80%" alt=""/>
</p>

<p>

1. Open IIS as an Admin by right-clicking on "Internet Information Services (IIS)" in the Start menu and selecting "Run as administrator"
2. Register PHP from within IIS by adding a module mapping for PHP in IIS Manager
3. Reload IIS by stopping and starting the server to apply the changes
4. Download and extract osTicket v1.15.8 to your computer
5. Locate the 'upload' folder in the extracted osTicket files and copy it to 'c:\inetpub\wwwroot'
6. Find the copied 'upload' folder in 'c:\inetpub\wwwroot' and rename it to 'osTicket'

  </p>
  
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

7. Take note that certain extensions may not be enabled, which can cause issues
    - Return to IIS Manager and navigate to the "Default" site, then locate the "osTicket" folder
    - Double-click on the PHP Manager feature for the osTicket site
    - Within PHP Manager, click on the "Enable or disable an extension" option
    - Enable: php_imap.dll, php_intl.dll, php_opcache.dll
8. Refresh the osTicket site in your web browser to see the changes and ensure that the extensions are working correctly
9. In the "osTicket" folder, locate the file named "ost-config.php"
    - Disable permission inheritance for the "ost-config.php" file
    - Remove all existing permissions associated with the file    
10. Add new permissions for the "ost-config.php" file
    - Grant full access permissions to the "Everyone" user/group 

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

11. Click on the "Continue" button to proceed with the osTicket setup in your web browser
12. Enter the name of your helpdesk and the default email address that will receive emails from customers
13. Download and install HeidiSQL
    - Open HeidiSQL and create a new session
    - Connect to the newly created session in HeidiSQL
    - Within the connected session, create a new database and name it "osTicket"
14. Continue setting up osTicket in the browser
15. Click on the "Install Now!" button to proceed with the installation

</p>

<br />

<p>

16. Clean up
    - Delete the "C:\inetpub\wwwroot\osTicket\setup" folder to remove any setup files that are no longer needed
17. Set permissions to "Read" only
    - Locate the file "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
    - In the properties window, go to the "Security" tab
    - Select the appropriate user/group and set the permissions to "Read" only and click "Apply"

</p>




<p> 
  Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http: //localhost/osTicket/ 

</p>


