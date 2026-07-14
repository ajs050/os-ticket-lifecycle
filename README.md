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

Adding a Department for SysAdmins. Admin Panel → Agents → Departments

- Parent Department: Top‑Level Department
- Name: SysAdmins
- Departments control ticket visibility and assignment.
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/de4dd50c-dfc2-4819-9180-2feb89fa7691" />


  
<br />
<br />


Step 4: Configure Teams

Adding an Online Banking Team, consisting of people from different departments. 

- Admin Panel → Agents → Teams
- Create team: Online Banking
- Teams allow agents from different departments to collaborate.
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/ff2f00dc-c789-496c-981b-c49968220116" />


<br />
<br />


Step 5: Configure User Settings

Configuring user settings to simulate an environment where an unregistered user can create a ticket.


- Admin Panel → Settings → User Settings
- UNCHECK: “Require registration and login to create tickets ”
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/e4b111c8-cd16-43dd-92aa-2dab3dcfc292" />


<br />
<br />


Step 6: Configure Agents (Help Desk Workers)

Creating our actual Help Desk Workers involved in this simulation. 

- Admin Panel → Agents → Add New
- Agents represent internal IT staff.
- Jane: SysAdmins	department, Supreme Admin Role, Online Banking Team
- John: Support department, View Only
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/f8383fe6-5db8-4ea2-b01b-a86b7a33a0e2" />


<br />
<br />

Step 7: Configure Users (Customers)

These simulate end‑users submitting tickets.

- Agent Panel → Users → Add New
- Karen & Ken
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/0c2902e5-704f-4a2b-b300-74fb076fd1db" />



<br />
<br />

Step 8: Configure SLAs (Service Level Agreements)

Creating SLA which are used as target goals you have to meet as a help desk worker. Promise between the team and user, how quickly you assign a ticket, reach out to the user, communicate with the user, etc
 

- Sev-A: Grace Period of 1 Hour, in a 24/7 schedule 
- Sev-B: Grace Period of 4 hours, in a 24/7 schedule 
- Sev-C: Grace Period of 8 Hours, during regular Business Hours
- SLAs define urgency and response expectations.
  
<img width="1708" height="935" alt="image" src="https://github.com/user-attachments/assets/73e2f407-e285-49b9-9acc-52d6c5fe4c20" />


<br />
<br />

Step 9: Configure Help Topics

Creating Help Desk Topics that categorize the incoming tickets. 
 

- Admin Panel → Manage → Help Topics: 
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
- Other
  
<img width="1708" height="860" alt="image" src="https://github.com/user-attachments/assets/cdaa382d-575b-4f14-91d3-d01ca90c34e7" />

<br />
<br />
