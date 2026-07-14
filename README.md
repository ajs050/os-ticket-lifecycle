# os-ticket-lifecycle

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle Examples</h1>
This repository demonstrates the ticket lifecycle inside osTicket. From creation to assignment, escalation, and resolution.
It simulates real help desk workflows and shows how IT support teams manage SLAs, departments, permissions, and user interactions.

This lab builds on the completed installation from the [osTicket: Prerequisites and Installation](https://github.com/ajs050/os-ticket-config) repository.<br />


<h2>🖥️ Environments and Technologies Used</h2>

Gain hands‑on experience with:

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows 11 (4 vCPUs)
- osTicket v1.15.8
- Web Browser (Admin Panel & Agent Panel)
- Gemini Ai


<h2>🎯 Purpose</h2>

Gain hands‑on experience with:
- Ticket creation and escalation
- SLA management
- Department visibility and permissions
- Agent vs. Admin workflows
- Real‑world help desk ticket intake and resolution

<h2>Lifecycle Steps</h2>

Step 1: Access osTicket

Using both website pages to understand the difference between an Admin and a SysAdmin Login Page.  
- Admin/Analyst Login Page: http://localhost/osTicket/scp/login.php
- End‑User Portal:  http://localhost/osTicket
- Agent Panel → Actual Help desk workers
- Admin Panel → System configuration, roles, SLAs, departments

  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/0bcef52d-f4b2-4b1c-bddb-c9fbf3ce2ec8" />

<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/b9ca9a87-c37c-4011-aeed-222486cc5bf5" />


<br />
<br />

Step 2: Configure Roles

Configuring a role of "Supreme Admin" that will have all permissions. 

- Admin Panel → Agents → Roles
- Create new role: Supreme Admin. Enable all permissions
- Roles determine what agents can see and modify.


<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/acc25c4b-db6c-4761-bc98-b1259594e633" />

<br />
<br />


Step 3: Configure Departments

Adding a  

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
