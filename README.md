<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines how to create users, departments, teams, permissions, and help topics in the open-source help desk ticketing system osTicket. <br />


<h2>Video Demonstration</h2>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Log-ins & Users</h2>

Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 

End Users osTicket URL:
http://localhost/osTicket 


<h2>Configuration Steps</h2>

<p>
<img width="1914" height="1077" alt="1" src="https://github.com/user-attachments/assets/d445457d-9fa4-4d05-89e2-0e80757ce482" />
</p>
<p>
Starting by creating a role. Log in as admin, on the Admin Panel under the Roles tab, select Add New Role.
</p>
<br />

<p>
<img width="1915" height="1079" alt="2" src="https://github.com/user-attachments/assets/507d1655-a32d-49f8-83fb-e4c53891cf9e" />
<p>
Make the name Supreme Admin, Select Permissions, select all the boxes under the tabs Tickets and Tasks, select Add Role.
</p>
<br />

<p>
<img width="1912" height="1079" alt="3" src="https://github.com/user-attachments/assets/0a0fb8a4-548c-4c61-a4f9-688a5ef0093d" />
</p>
<p>
Create a new department for SYS Admins by going to the admin panel, selecting agents→Departments, then selecting Add New Department.
</p>
<br />

<p>
<img width="1919" height="1079" alt="4" src="https://github.com/user-attachments/assets/9ae96145-117e-46f0-90be-aa50c20ced45" />
</p>
<p>
Name: SysAdmins and click Create Dept
</p>
<br />

<p>
<img width="1919" height="1079" alt="5" src="https://github.com/user-attachments/assets/9101d383-2c07-4570-bf1d-51067911852c" />
</p>
<p>
It's possible to create different teams if you have people in different departments. Go to the Admin panel→Agents→Teams→Add New Team
</p>
<br />

<p>
<img width="1914" height="1079" alt="6" src="https://github.com/user-attachments/assets/735054b0-fc6a-42e9-9122-b802c4f6d353" />
</p>
<p>
Create a new team named Online Banking.
</p>
<br />

<p>
<img width="1915" height="1079" alt="7" src="https://github.com/user-attachments/assets/22cf3376-558a-458d-b047-546ceca8639e" />
</p>
<p>
Change settings so users who are not set up in the system can create tickets. On the Admin panel, select Settings→Users, and uncheck “require registration and login to create tickets”.
</p>
<br />

<p>
<img width="1915" height="1079" alt="8" src="https://github.com/user-attachments/assets/637821dd-dd6a-4f9e-a0fd-0e3c7474e323" />
</p>
<p>
Now, to create some Agents. These are users responding to tickets we will create in a later lab. On the Admin Panel, go to Agents and select Add New Agent.
</p>
<br />

<p>
<img width="1914" height="1079" alt="9" src="https://github.com/user-attachments/assets/53b33e2d-6c9e-48e8-af20-14f5ce5eee91" />
</p>
<p>
Start with JaneDoe@loginPacific.com. User name: Jane. Under the Access tab, select SysAdmins as the department & SupremeAdmin as the Role. Make her part of the Online Banking Team. Click create and make the password: Password1
</p>
<br />

<p>
<img width="1913" height="1079" alt="10" src="https://github.com/user-attachments/assets/8f7cafa3-7dbd-432b-9e47-18da8d87b305" />
</p>
<p>
Create another Agent user. This time, it will be John Doe. His department will be Support, with the role set to view-only. Click create and make the password: Password1
</p>
<br />

<p>
<img width="1916" height="1079" alt="11" src="https://github.com/user-attachments/assets/c2b374ab-0ca5-4785-a6fb-96bfe7c643f6" />
</p>
<p>
Create a user. This will be an employee who needs to create a ticket. Go to Agents Panel and select users→Add User. Create a user named Karen.
</p>
<br />

<p>
<img width="1919" height="1078" alt="12" src="https://github.com/user-attachments/assets/c55acab9-0630-4548-bc26-57b9ebea8b1b" />
</p>
<p>
Now we need to configure the SLA’s. An SLA is a Service Level Agreement that includes response and resolution times, as well as responsibilities. Go to the Admin panel, select Manage→SLA→Add New SLA Plan.
</p>
<br />

<p>
<img width="1916" height="1078" alt="13" src="https://github.com/user-attachments/assets/a3c632e2-0a89-458f-b74b-090bff1d5914" />
</p>
<p>
The 1st SLA will be named Sev-A. Set the grace period to 1 hour and schedule 24/7.
The 2nd SLA will be named SEV-B. Set the grace period to 4 hours and schedule 24/7
The 3rd SLA will be named SEV-C. Set the grace period to 8 hours and the schedule to Business hours.
</p>
<br />

<p>
<img width="1916" height="1079" alt="14" src="https://github.com/user-attachments/assets/b5c69832-e791-4d07-b20a-1fb53043e5d2" />
</p>
<p>
The last thing to do before moving forward with working on some tickets is to set up some help topics. This is for end users creating a ticket. 
Go to Manage→Help Topics→Add new Help Topic.
</p>
<br />

<p>
<img width="1913" height="1079" alt="16" src="https://github.com/user-attachments/assets/71fe42fd-9a5c-4554-9250-4f7c9d77333b" />
</p>
<p>
Make five topics.
The 1st Topic will be Business Critical Outage, and the Parent Topic will be Report a Problem
The 2nd Topic will be Personal Computer issue, and the Parent Topic will be Report a Problem.
The 3rd Topic will be Equipment Request, and the Parent Topic will be General Inquiry.
The 4th Topic will be Password Reset, and the Parent Topic will be Report a Problem.
The 5th Topic will be Other, and the Parent Topic will be General Inquiry.
<br />

<p>


