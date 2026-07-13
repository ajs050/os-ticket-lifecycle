# os-ticket-lifecycle

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle Examples</h1>
This repository demonstrates the ticket lifecycle inside osTicket. From creation to assignment, escalation, and resolution.
It simulates real help desk workflows and shows how IT support teams manage SLAs, departments, permissions, and user interactions.

This lab builds on the completed installation from the [osTicket: Prerequisites and Installation](https://github.com/ajs050/os-ticket-config) repository.<br />


<h2>🖥️ Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Windows 11 (4 vCPUs)
- osTicket v1.15.8


<h2>🎯 Purpose</h2>

Gain hands‑on experience with:
- Azure VM deployment
- IIS and PHP configuration
- Database setup and integration
- osTicket installation and initial configuration

<h2>Installation Steps</h2>

Step 1: Create Azure VM

Creating a Windows Virtual Machine through an Azure Subscription. 
- Name: osticket-vm
- OS: Windows 11
- Credentials: labuser / osTicketPassword1! (for lab use only)
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/5b382ca4-a27e-4a89-a700-25996200e2d3" />


<br />
<br />

Step 2: Install Requirements

We will first enable IIS with CGI through the Windows Control Panel. Then, after extracting the ZIP folder available on the OS's website, we will install the following items. 

- PHP Manager
- Rewrite Module
- VC Redistributable
- MySQL. Launch Standard Configuration, and create credentials for the database  

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/0dcd30df-363b-4fe1-bd68-96d336468de6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/3f8068bf-c86e-4c7c-8f9a-8af9d261fc7f" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/e412b0a8-120b-4528-bc7b-f53d3df611a2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/c6742f4e-7dfe-41df-8846-9e02cde66fd1" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/159162a1-c57d-4e98-9685-af234a3ba754" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/138c1e87-586b-4cd8-9f77-9aa081a6c249" />

<br />
<br />


Step 3: Configure PHP and IIS


We will create a PHP Folder (C:\PHP) in Windows (C:) and unzip the PHP 7.3.8 files into this folder. Afterwards: 

- Open IIS as Administrator.
- Register PHP in IIS via PHP Manager → C:\PHP\php‑cgi.exe.
- Reload IIS (Stop and Start the server).
  
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/660e107b-d915-47c0-925d-190586a64c0e" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/b2f574f3-94d5-4f19-87cb-c0abe1499ac7" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/9ac0f390-aac7-4eeb-8496-b2ea035350c2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/03bf5b9d-2900-43bf-9650-389d7f70b402" />

  
<br />
<br />


Step 4: Install osTicket


After we unzip osTicket‑v1.15.8.zip from the osTicket‑Installation‑Files folder, we will: 

- Copy the upload folder into C:\inetpub\wwwroot.
- Rename upload to osTicket.
- Reload IIS (Stop and Start the server).
- Browse to http://localhost/osTicket to confirm the installation page loads.
  
<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/026325db-c27e-41e7-8195-bfe763b12ef2" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/1a8c284c-aedb-4084-baae-542f95f67ba6" />

<img width="1708" height="880" alt="image" src="https://github.com/user-attachments/assets/90d603e4-e6ca-4a70-b804-cba4218eaff3" />


<img width="1708" height="1070" alt="image" src="https://github.com/user-attachments/assets/429d6f9d-8c1e-4b06-b05c-2d776cd38786" />




<br />
<br />


Step 5: Post‑Installation Setup

We're not finished just yet! Just a few last configurations left. 


- Enable Required PHP Extensions in IIS: IIS → Sites → Default → osTicket. Double‑click PHP Manager.
- Click “Enable or disable an extension”. Enable php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket website afterwards to make sure changes went through.
- Rename Configuration File (From: C:\inetpub\wwwroot\osTicket\include\ost‑sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost‑config.php)
- Assign Permissions within the ost‑config.php file. Right-click → Properties → Security → Advanced. Disable inheritance → Remove All. Then, Add → Select a principal → Enter Everyone → Check Names → OK → Full Control
- Continue Setup in OsTicket Browser
- Install HeidiSQL from the osTicket‑Installation‑Files folder. Open HeidiSQL → Create new session, provide credentials from earlier installation → Right‑click Unnamed → Create New Database → Name: osTicket
- Provide the last details for the database settings, then hit install!!
  
<img width="1708" height="797" alt="image" src="https://github.com/user-attachments/assets/6b2cc219-111a-4444-a497-16e94590b60d" />


<img width="1708" height="961" alt="image" src="https://github.com/user-attachments/assets/99759263-ba0f-4706-bb38-2604867d6da8" />


<img width="1708" height="776" alt="image" src="https://github.com/user-attachments/assets/0aa67a35-7b0c-459b-a6ac-187af793fd49" />



<img width="1708" height="863" alt="image" src="https://github.com/user-attachments/assets/73cb270f-7100-40ca-8f3a-ef43d53a621c" />

<img width="1708" height="863" alt="image" src="https://github.com/user-attachments/assets/ffad7c65-b0e1-433c-8c6c-7b60e2f5d6cb" />

<img width="1708" height="863" alt="image" src="https://github.com/user-attachments/assets/edb19baf-6096-4fd6-a1dc-14e0158e4dd8" />

<img width="1708" height="863" alt="image" src="https://github.com/user-attachments/assets/55942a21-cdbe-4432-a495-89c4f770c5ce" />

<br />
<br />

After this, osTicket will be installed and accessed at last for both admins and users. 🎉 🎊

<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/edc8ce54-bd18-482b-af29-2617844152ea" />
