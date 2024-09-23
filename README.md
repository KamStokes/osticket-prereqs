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

- Create an Azure Virtual Machine (Windows 10, 4 vCPUs recommended)
- Log into the VM with Remote Desktop
- Within the VM, download the following zip file: "[osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)". Unzip/extract the file onto your desktop. The folder should be called “osTicket-Installation-Files”.  The files in this folder will be used to install osTicket and some of the dependencies.
  
  

<h2>Installation Steps</h2>
<h3>1) Install/Enable IIS in Windows WITH CGI</h3>

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
Select uninstall a program underneath "Programs" 
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
Check the box that says "CGI". clcick "OK" and install the file
</p>

<p>
<h3>2) Install PHP Manager for IIS</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/36345bb0-cef4-4038-9a36-83e22c1dfb92)
</p>
<p>
Open the folder labeled “osTicket-Installation-Files” on your desktop, and open the file folder labeled “osTicket-Installation-Files”
</p>

<p>

![image](https://github.com/user-attachments/assets/7dd46474-092a-44ed-b02a-643d3bcd773d)
</p>
<p>
Install the PHP Manager labeled "PHPManagerForIIS_V1.5.0" 
<p>
<h3>3) Install Rewrite Module</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/7dd46474-092a-44ed-b02a-643d3bcd773d) 
</p>
<p>
Inside the same file folder, install the rewrite module file labeled "rewrite_amd64_en-US" 
</p>

<p>
<h3>4) Create the Directory C:\PHP</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/d01228fe-ebf1-4119-9f57-06155a3d0d97)
</p>
<p>
At the bottom left of your screen, right-click on the manilla folder. Open "File Explorer"
</p>

<p>

![image](https://github.com/user-attachments/assets/2997cc47-fa39-4163-b297-2d47deb3627a)
</p>
<p>
Click the dropdown arrow next to "This PC" and select "Windows (C:)"
</p>

<p>

![image](https://github.com/user-attachments/assets/ec0b29eb-b780-43bb-bc15-6ef8b756a07c)
</p>
<p>
Right-click anywhere on the white space to open this pop-up tab. Select "New" and select "Folder". Name this folder "PHP"
</p>

<p>
<h3>5) Unzip unzip PHP 7.3.8 into the “C:\PHP” folder</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/c0b057ce-fd18-4dd5-8161-816f8f971259)
</p>
<p>
From the "osTicket-Installation-Files", right-click on the zip file labeled "php-7.3.8-nts-Win32-VC15-x86" and click "Extract All"
</p>

<p>

![image](https://github.com/user-attachments/assets/7fa1e102-f233-4856-9a9b-4bb4f79bcc4a)
</p>
<p>
Type "C:\PHP" into the input box and click "Extract"
</p>

<p>
<h3>6) Install VC_redist.x86</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/732bed4f-5794-46b2-8d99-02e8dcc13316)
</p>
<p>
From the “osTicket-Installation-Files” folder, install "VC_redist.x86"
</p>

<p>
<h3>7) Install MySQL 5.5.62</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/4c5297f1-8d9d-4e1f-8e9d-87d920232fcc)
</p>
<p>
From the “osTicket-Installation-Files” folder, install "mysql-5.5.62-win32". Select "Typical" setup type. Click "finish" to Launch Configuration Wizard (after install) 
</p>

<p>

![image](https://github.com/user-attachments/assets/639058a4-c842-414c-b9f9-f7e317029369)
</p>
<p>
Once the Configuration Wizard is launched, select "Standard Configuration"
</p>

<p>

![image](https://github.com/user-attachments/assets/75340b23-8ffc-48cf-9779-9d48b7c46498)
</p>
<p>
Click "Next" until you arrive to this screen. For both input boxes type "root". Select "Next", "Execute", and "Finish"
</p>

<p>
<h3>8) Open IIS as an Admin</h3>
</p> 

<p>

![image](https://github.com/user-attachments/assets/3cfd5256-64f2-4c67-99a4-bf213ceb6ed1)
</p>
<p>
At the bottom of your desktop screen, type "IIS" into the search toolbar. Select "Run as administrator" on the right-hand side
</p>

<p>
<h3>9) Register PHP from within IIS</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/5dbc0399-c66a-48f9-b443-994b044696df)
  
</p>
<p>
Open "PHP Manager"
</p>

<p>

![image](https://github.com/user-attachments/assets/d75fd01e-4ac1-4850-a745-28fb084a35c0)
</p>
<p>
Select "Register New PHP version". Type "C:\PHP\php-cgi.exe" into the input bar and click "OK"
</p>

<p>
<h3>10) Reload IIS</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/2d551695-e930-4dd7-90b8-856bad0881bb) 
</p>
<p>
Right-click on "osTicketVM" and click "Stop". After a moment, right-click again and select "Start"
</p>

<p>
<h3>11) Install osTicket v1.15.8</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/358dffa5-64f3-45ab-bf30-0ac8360639d5)
</p>
<p>
From the “osTicket-Installation-Files” folder, single-click "osTicket-v1.15.8". Click  the pink-highlighted "Extract" and select "Extract all"
</p>

<p>

![image](https://github.com/user-attachments/assets/03fb9959-d847-4efc-a040-5bfeb2894ea3)
</p>
Select "Extract". Once extracted, a new window will open automatically

<p>

![image](https://github.com/user-attachments/assets/e9ac6b35-e1a3-4969-9485-c0b7995a21cc)
</p>
<p>
From the existing/new file explorer window, scroll down and select "Windows (C:)". Select "inetpub" folder --> "wwwroot" folder. From the window the computer opened, click and drag the "upload" folder into the "wwwroot" folder.
</p>

<p>

![image](https://github.com/user-attachments/assets/0b75baab-7c95-44d7-af61-0aea9d2425cc)
</p>
<p>
Right-clcik the "upload" folder and rename it to "osTicket"
</p>

<p>
<h3>12) Reload IIS</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/2d551695-e930-4dd7-90b8-856bad0881bb) 
</p>
<p>
Right-click on "osTicketVM" and click "Stop". After a moment, right-click again and select "Start"
</p>

<p>
<h3>13) Install osTicket (cont.)</h3>

![image](https://github.com/user-attachments/assets/f4fd7a20-f5d0-42c2-ab5e-48b0f2847282)  
</p>
<p>
Inside of the IIS Manager, click the dropdown arrow next to sites. Dropdown "Default Web Site. Single-click "osTicket". Click "Browse *:80 on the far right-hand side (a browser will open). Open "PHP Manager" and select "Enable or disable an extension".
</p>
 <p>

![image](https://github.com/user-attachments/assets/606faa54-5be0-4099-ab1d-4f529dfe9a99)

 </p>
 Enable the following extnesions: php_imap.dll | php_intl.dll | php_opcache.dll

<p>

![image](https://github.com/user-attachments/assets/23b5366c-7cfe-4647-b8ee-28a87724a738)

</p>
<p>
Refresh the osTicket browser that your computer opened
</p>
<p>
<h3>14) Rename: ost-config.php</h3>
</p>
<p>
  
![image](https://github.com/user-attachments/assets/d6b0eb36-ed04-40f0-a6b3-2d4fe3bc2edc)  
</p>
<p>
Inside of file explorer, go to "Windows (C:) --> "inetpub" --> "wwwroot" --> osTicket --> "include"
</p>

<p>

![image](https://github.com/user-attachments/assets/f72b3edc-6132-4187-aa96-80fb506307d3)
</p>
<p>
Scroll down to the bottom and right-click on "ost-sampleconfig.php". Rename this file to "ost-config.php". 
</p>
<p>
<h3>15) Assign Permissions: ost-config.php</h3>  
</p>
<p>

![image](https://github.com/user-attachments/assets/c19e11a3-e813-4db6-91d6-12c20fa7fe3e)
</p>
<p>
Right-click the newly named file and click "Properties" --> "Security" --> "Advanced" 
</p>

<p>

![image](https://github.com/user-attachments/assets/37752abd-e6a3-4b3d-90b7-32169e4172b8)  
</p>
<p>
Select "Diable inheritance" --> "Remove all inherited permissions from this object." Select "Add"
</p>

<p>

![image](https://github.com/user-attachments/assets/7e47de22-2c60-4379-915f-c9449820c317)
</p>
<p>
Click "Add" --> "Select a principal"
</p>

<p>

![image](https://github.com/user-attachments/assets/d20acafa-f3d9-4d76-806e-9ea05c18451c)  
</p>
<p>
In the text bar, type "evryone". Select "Check Names". Click "OK"
</p>

<p>

![image](https://github.com/user-attachments/assets/902fc0f3-ea9c-4afe-aaf1-20416e2b180f)
</p>
<p>
Check the box that says "Full Control" and select "OK". Select "Apply" and "OK"
</p>
<p>
<h3>16) Continue Setting up osTicket in the browser</h3>
</p>

<p>

![image](https://github.com/user-attachments/assets/3a44b308-e600-4cb7-8a52-0378179f9cbc)
</p>
<p>
Click "Continue" at the bottom of the screen
</p>
<p>
<b>System Settings</b>
</p>
<p>
Helpdesk Name: Anything you prefer
</p>
<p>
Default email: Anything you prefer
</p>
<p>
<b>Admin User</b> 
</p>
<p>
First Name: Anything you prefer 
</p>
<p>
Last Name: Anything you prefer
</p>
<p>
Email Address: Anything you prefer. (Make sure the admin email is different from the default email)
</p>
<p>
Username: adminuser
</p>
<p>
Password: Password1
</p>

<p>
<h3>17)  install HeidiSQL</h3>
</p>

<p>
  
![image](https://github.com/user-attachments/assets/28e5c552-0e93-4e1d-bedf-a25858b36f62)
</p>

<p>
From the “osTicket-Installation-Files” folder, install "HeidiSQL_". Click "Finish" and a new tab will open up. Select "Skip"
</p>

<p>

![image](https://github.com/user-attachments/assets/18de6bfc-3f1d-492c-a230-9f0cefa5e4af)
</p>
<p>
Select "New". For the password, type "root". Select "Open"
</p>

<p>

![image](https://github.com/user-attachments/assets/54d79481-f1a7-44ce-ae6b-f51769726285)
</p>
<p>
Right-click on "Unnamed" --> "Create new" --> Database
</p>

<p>

![image](https://github.com/user-attachments/assets/7e9a6c40-39cf-4dfd-9962-318509ab43c3) 
</p>
<p>
Name the database "osTicket". Select "OK"
</p>

<p>
<h3>18) Continue Setting up osTicket in the browser</h3>
</p>
<p>
MySQL Database: osTicket
</p>
<p>
MySQL Username: root
</p>
<p>
MySQL Password: root
</p>
<p>
Click “Install Now"
</p>
