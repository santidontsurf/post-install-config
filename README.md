<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Installation Configuration</h1>
This tutorial outlines the recommended post-installation configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Post-Installation</h2>

<p>
</p>
<p>
Now that we have successfully installed osTicket alongside all it's dependencies we can focus on systems administration. There are two links that will be important for this section. The first: http://localhost/osTicket/scp/login.php this is the admin login page from where you can login using the admin account created on the first part of this tutorial, we will do most all of the configurations from this side of osTicket. The second: http://localhost/osTicket is the end-user side of osTicket from where tickets can be submitted for you to work on. Click on the first link and log in. The main page should look something like this: 
</p>
<p align="center">
<img alt="Screenshot 2025-06-16 at 10 33 44 AM" src="https://github.com/user-attachments/assets/2a41b0bd-2f63-4e4c-8dbf-20e9e3bb91f3" height=80% width=80%/>
</p>
<br />
<p>As of now, the main page is set on the Agent panel, which allows you to work on tickets but doesn't give you access to all the administrative tools that we want to use. To use these tools, click on "Admin Panel" on the upper-right corner of the page to access the administrative side of osTicket. On this new page, go to Agents -> Roles to see the hierarchy of access that different roles have on osTicket, we will create a new role by clicking on the right-side icon "Add New Role".</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 10 49 16 AM" src="https://github.com/user-attachments/assets/525a714b-c5bb-4187-828a-da8441bbc60b" height=80% width=80% />
</p>
<br />
<p>We will name this role "Supreme Admin" and click on Permissions to choose how much access we want this new role to have. There are tabs on the Permissions page: Tickets, Tasks, and Knowledgebase. We will check every single permission on all three of these to give the admin complete access to all configurations, then click Add Role at the bottom to create this new role.</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 10 55 38 AM" src="https://github.com/user-attachments/assets/3a8d7c3b-175d-46f9-a91f-41d82f81d69c" height=80% width=80%/></p>
<br />
<p>Next we are going to check the departments in osTicket. Department configuration affects ticket visibility, where you can choose if tickets assigned to a department can be seen by only that department or by everyone in the system. Go to Agents -> Departments to see the current departments that we have, we will create a new department by clicking "Add New Department". Here we will create a Top-Level Department called "System Aministrators" where our Supreme Admin will be assigned to. Leave most of the configurations as they are, then scroll down and click "Create Dept".</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 09 25 AM" src="https://github.com/user-attachments/assets/279d82fe-d80c-4da9-844e-01fc39a301c1" height=80% width=80% />
</p>
<br />
<p>Under the Agent page travel to Teams page where we will create a new team. With Teams, we can have people from different departments joined together under a single team for tickets that require the assistance of various key role players. Under teams there is already a Level I Support Team so we will create a new team by clicking on "Add New Team" and titling the team "Level II Support" then click "Save Changes".
</p>
<p align="center"><img  alt="Screenshot 2025-06-16 at 11 14 48 AM" src="https://github.com/user-attachments/assets/892d0956-dd07-46e1-883e-b6eddded4447" height=80% width=80%/>
</p>
<br />
<p>Next, we will examine the authentication settings to make sure that an important setting for the purpose of this tutorial is active. We will travel to Settings -> Users and under the authentication settings make sure that "Require registration and login to create tickets" is unchecked. If it is already unchecked nothing needs to be done, but if it is checked, just uncheck it and click "Save Changes" at the bottom.</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 23 34 AM" src="https://github.com/user-attachments/assets/27fbcde5-0152-4ab4-9b6d-e13626e7d072" height=80% width=80%/>
</p>
<br />
<p>We now have created a new role, a new department, and a new team for our organization. It is now time to create Agents. Still in the Admin panel, travel to Agents and click "Add New Agent".</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 26 31 AM" src="https://github.com/user-attachments/assets/e840749b-31cb-4dc2-b24f-a05fe4999a4c" height=80% width=80% />
</p>
<br />
<p>In the agent creation page we will name this agent Jane Doe and add an email and username. Then click "Set Password" and make sure that both "Send the agent a password reset email" and "Require password change at next login" are unchecked, then create a password and click "Set". For the sake of this lab, the username will be "jane" and the password "janedoe". </p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 30 27 AM" src="https://github.com/user-attachments/assets/81ff1a25-d2c8-4be5-8b27-b6c98ec6558b" height=80% width=80% />
</p>
<br />
<p>Under the Access tab for this new agent, we will assign Jane to two departments. Her primary department will be "System Administrators" and her role will be "Supreme Admin" and under Extended Access select "Support" as her secondary deparmment with the same role. Under the Teams tab we will add her to the Level II Support Team then click "Create" to add Jane as an agent.</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 37 29 AM" src="https://github.com/user-attachments/assets/95546086-2187-4d58-b5bd-238a8cdce9fc" height=80% width=80%/>
</p>
<br />
<p>With an agent finnally created, we will now create some users. Click on Agent Panel on the upper right of the page and once you're in the Agent Panel, click on the Users tab, then "Add User". </p>
<p align="center"><img  alt="Screenshot 2025-06-16 at 11 39 51 AM" src="https://github.com/user-attachments/assets/dd5fa15e-68d0-429b-9ea1-65c677542c5c" height=80% width=80%  />
</p>
<br />
<p>Create two users named Karen and Ken. All that is needed is a name for the user and an email.</p>
<p align="center"><img alt="Screenshot 2025-06-16 at 11 43 25 AM" src="https://github.com/user-attachments/assets/3dc64bb9-5f8d-43bd-b862-acd60381c769" height=80% width=80%/>
</p>
<br />
<p>Next, we will create Service-Level Agreements (SLA's) which determine the severity of a ticket and how soon it should be resolved. To do this we will travel back to the Admin Panel and into the Manage tab. Under the manage tab click on SLA click "Add New SLA Plan".</p>
<p align="center"><img alt="Screenshot 2025-06-18 at 10 12 27 AM" src="https://github.com/user-attachments/assets/9a1af8d3-4d63-4c7b-a1ee-96ba16fa9649" height=80% width=80%/>
</p>
<br />
<p>In this page we will create three types of SLA based each with different ticket severity. The first SLA will be "Sev-A" for the most important tickets. Sev-A will have a grace Period of 1 hour and a schedule of 24/7. The second SLA will be "Sev-B" with a grace period of 4 hours and a schedule of 24/7. Lastly, SLA "Sev-C" with a grace period of 8 hours and a schedule of 24/5 (Business hours). Follow the example below to create all three SLA's.
</p>
<p align="center"><img alt="Screenshot 2025-06-18 at 10 17 59 AM" src="https://github.com/user-attachments/assets/8ab09826-7d22-4245-bcb7-998870fc90a5" height=80% width=80% />
</p>
<br />
<p>The last step to finish all osTicket configurations is to create some Help Topics to better classify each ticket submitted by an end-user. On the same Manage tab through which we accessed SLA, click on Help Topics on the far left, then click "Add New Help Topic".</p>
<p align="center"><img alt="Screenshot 2025-06-18 at 10 23 53 AM" src="https://github.com/user-attachments/assets/4e76812e-72f0-4f5d-aed9-392711419fe6" height=80% width=80%/>
</p>
<br />
<p>For this lab we will only need to create one more Help Topic. Call this topic "Business Critical Outage" and choose "Report a Problem" as the Parent Topic for it, then click "Add Topic" at the bottom.</p>
<p align="center"><img alt="Screenshot 2025-06-18 at 10 26 08 AM" src="https://github.com/user-attachments/assets/cd5a3052-2b70-489f-816c-0d327ce8150c" height=80% width=80%/>
</p>
<br />
<p>Congratulations! You have successfully configured osTicket to be ready to use and are almost done with this tutorial! For the final part travel to:</p>
  
[osTicket: Ticket Lifecycle Examples](https://github.com/santidontsurf/ticket-lifecycle)






