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

- Create an Azure Virtual Machine (Windows 10, 4 vCPUs)
- Log into the VM with Remote Desktop
- Within the VM, download the [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) and unzip/extract it onto your desktop. The folder should be called “osTicket-Installation-Files”
  
  

<h2>Installation Steps</h2>

<p>
  
![image](https://github.com/user-attachments/assets/05b0ef56-8e02-4248-bcec-9d3a2694b51f)

</p>
<p>
Click the start menu and open the Control Panel
</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/bdb15fe2-b316-4d05-bdd6-abc34d47c935)

</p>

<p>
Select uninstall a program underneath "Programs" (Although no programs will be uninstalled)
</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/692be41a-1d40-4680-8124-4aecc8348aff)
  
</p>
<p>
On the lefthand side, select "Turn Windows features on or off"
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/5e4e0154-0268-4550-a898-0343250cfa59)


</p>
<p>
Check the box that says "Internet Information Services". Clcik the plus sign to expand it further, expand "World Wide Web Services", and expand "Application Development Services"
</p>

<p>

![image](https://github.com/user-attachments/assets/a78a2bc6-28f9-496c-93f2-cdfa00f4b8fa)

</p>
<p>
Check the box that says "CGI". clcick "OK" and instaall the file
</p>


