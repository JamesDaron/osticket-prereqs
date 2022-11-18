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
Now that you have created your VM you will have to enable IIS. Simply access the control panel then select uninstall a program. Off to the left select "Turn windows features on or off". A list will appear then you will enable Internet Information Services.
</p>
<br />

<p>
<a href="https://imgur.com/9HTz9T3"><img src="https://i.imgur.com/9HTz9T3.jpg" title="source: imgur.com" /></a>
</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer
</p>
<br />
