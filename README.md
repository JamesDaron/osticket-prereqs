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

- Azure Virtual Machine
- OsTicket Installation Files
- Heidi SQL

<h2>Installation Steps</h2>

Welcome! First, we will need to create a Virtual machine using the Microsoft Azure portal. We will be using a VM which is a remote computer. We are using a VM in order to protect our physical machine in the event something unexpected occurs. Create a resource group and title it "osTicket". Afterwards create a VM with 2-4 CPUs. For this example we will be using 4 CPUs.

<p>
<a href="https://imgur.com/KkTwoEQ"><img src="https://i.imgur.com/KkTwoEQ.jpg" title="source: imgur.com" /></a>
</p>
<p>
Next, connect to your newly created VM using Remote Desktop using the public IPv4 address. If you are a Mac user you will have to download the Microsoft RDP.
</p>
<br />

<p>
<a href="https://imgur.com/Mq939fY"><img src="https://i.imgur.com/Mq939fY.jpg" title="source: imgur.com" /></a>
</p>
<p>
Now that you have created your VM you will have to enable IIS. Access the control panel then select uninstall a program. Select "Turn windows features on or off" which is located to the left. A list will appear and from there you will enable Internet Information Services.
</p>
<br />

<p>
<a href="https://imgur.com/9HTz9T3"><img src="https://i.imgur.com/9HTz9T3.jpg" title="source: imgur.com" /></a>
</p>
<p>
Now that you have enabled IIS you will need to install Web Platform Installer. A link below has been provided: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 This link will provide you with material that is required to download osTicket and continue the setup process. Once inside the provided link, click and install Web Platform Installer
</p>
<br />

<p>
<a href="https://imgur.com/PDq8gzi"><img src="https://i.imgur.com/PDq8gzi.jpg" title="source: imgur.com" /></a>
</p>
<p>
<a href="https://imgur.com/8jky0rf"><img src="https://i.imgur.com/8jky0rf.jpg" title="source: imgur.com" /></a>
</p>
Once you have installed Web Installer Platform open it. Go to the search bar and type "MySQL". From there, install MySQL 5.5. Afterwards install x86 version of PHP up until 7.3. There are some failed files such as C++ redistributable package as well as PHP 7.3.8 and PHP Manager, and IIS. The files for those listed and can be found inside the install link.
<br />

<p>
<a href="https://imgur.com/bo0ga6O"><img src="https://i.imgur.com/bo0ga6O.png" title="source: imgur.com" /></a>
</p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
<br />

<p>
<a href="https://imgur.com/1CZSW4x"><img src="https://i.imgur.com/1CZSW4x.jpg" title="source: imgur.com" /></a>
</p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
<br />

<p>
<a href="https://imgur.com/AgU0mWb"><img src="https://i.imgur.com/AgU0mWb.jpg" title="source: imgur.com" /></a>
</p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and obsereve the changes "Intl Extension" should now be enabled.
<br />

<p>
<a href="https://imgur.com/reRRVTB"><img src="https://i.imgur.com/reRRVTB.png" title="source: imgur.com" /></a>
</p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php Assign permissions to ost-config.php Disable inheritance->Removeall New Permissions->Everyone->all
<br />

<p>
<a href="https://imgur.com/Jy3QuLM"><img src="https://i.imgur.com/Jy3QuLM.png" title="source: imgur.com" /></a>
</p>
Afterwards continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets.
<br />

<p>
<a href="https://imgur.com/MAh3FMh"><img src="https://i.imgur.com/MAh3FMh.jpg" title="source: imgur.com" /></a>
</p>
<p>
<a href="https://imgur.com/IzWLIx8"><img src="https://i.imgur.com/IzWLIx8.jpg" title="source: imgur.com" /></a>
</p>
Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!” Congratulations, hopefully it is installed with no errors! Clean up Delete: C:\inetpub\wwwroot\osTicket\setup Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
<br />
