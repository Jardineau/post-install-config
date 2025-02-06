<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Agents
- Configure Users
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
  We will first configure roles. in your VM make sure that you log in in your admin account in osTicket: http://localhost/osTicket/scp/login.php.
  
  - Once in we will go to Admin Panel -> Agents -> Roles.
  - In this tutorial, we will add a role called "Supreme Admin" to provide full access. Note that this is not a recommended practice in real-world scenarios, as roles should typically be configured to grant specific permissions rather than full access to all users.


![image](https://github.com/user-attachments/assets/4bc70bf0-c0a5-411f-963f-c77fb1d2ab6e)

  - Go through the tabs and make sure you enable everything and add Role.

</p>
<p>
  
![image](https://github.com/user-attachments/assets/8aa52e94-cde4-4fe6-8b1b-d6731d16fe70)

Now let's Click the "Departments" button in the Agents tab. Here, you can create a new department. Each agent is assigned to a specific department based on their role within the helpdesk. In this tutorial, we will create the "System Administrators" department, where the Supreme Admins will be assigned. Other settings, such as SLAs, managers, and email configurations, can also be set up within the Departments tab.

![image](https://github.com/user-attachments/assets/3fbbb246-ff4b-4cb8-a24f-43caeac4acf5)

After adding the new department, we will proceed to create a team. This section allows you to organize teams for specific issues that may arise, such as a problem on a particular platform that a team is more proficient in handling. To create a team, go to:
- Admin Panel -> Agents -> Teams
- We will add a team called "Level II Support".
</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/78e71e2f-5a29-484c-b94e-57980defae3e)
</p>
<p>
Now that we have set up a new team, we will create a setting that allows anyone to create tickets. To do this, go to:
  -Admin Panel -> Settings -> User Settings

  We just want to make sure that the setting is UNCHECKED.
  
![image](https://github.com/user-attachments/assets/915cbe6c-6d8c-46b0-88b4-4013b529b0b3)

</p>
<br />

<p>
Now, we will create agents, who are the employees of the helpdesk responsible for resolving tickets submitted by end users. Agents are assigned to primary departments and given specific roles for tickets in their department. They can also be granted access to other departments and roles, depending on their responsibilities. Permissions, access, and teams are managed within the Agents tab.
  -Admin Panel -> Agents -> Add New
</p>
<p>
For this tutorial, we will create two agents: Jane Doe, who will have the Supreme Admin role with full access to all departments and teams, and John Doe, who will act as our first-line helpdesk agent. John will have limited access, allowing him to communicate with end users and escalate tickets to Jane Doe if necessary.

  - Before finishing the creation of each agent, make sure to set their passwords. To do this, unselect the option "Send the agent a password reset email", then manually enter a password for the agent. Additionally, unselect "Require change on next login" to prevent them from being prompted to change their password upon first login.
  ![image](https://github.com/user-attachments/assets/72273c71-80d4-4ce6-9e00-0cef0fd7209c)

 
  - Jane Doe
  
  ![image](https://github.com/user-attachments/assets/120b6173-a3d6-4542-b894-339651eeceac)
  ![image](https://github.com/user-attachments/assets/4c50f77e-667f-49b4-b48f-09b2b04ef8fd)
  ![image](https://github.com/user-attachments/assets/f4cb2ff6-d80c-4dba-af66-f554d4c6f1ef)

  - John Doe

  ![image](https://github.com/user-attachments/assets/1c9517f0-eaae-41d1-ba38-bfd6a066b936)
  ![image](https://github.com/user-attachments/assets/90def6e1-bafb-4168-9845-928bc126f430)
  ![image](https://github.com/user-attachments/assets/36e499dc-72e3-4bb8-acaf-90ad43fc0830)

After creating some agents, we will create users. Users are customers who create tickets when they encounter issues. A user is identified by their email address. 
- To create a user follow this path Agent Panel->Users->User Directory->Add new.
  ![image](https://github.com/user-attachments/assets/45762bd8-9982-42ef-9def-3791ca00cdb0)
  ![image](https://github.com/user-attachments/assets/0861a9e0-457e-48c0-9cd7-688868c8f291)

Now lets set up SLA to establish the expected time frame within which the help desk should resolve a ticket. To create an SLA plan, navigate to:
- Admin Panel -> Manage -> SLA Plans

Each SLA plan is associated with a schedule and includes a grace period. For instance, the SEV-A plan operates 24/7 with a one-hour grace period.

![image](https://github.com/user-attachments/assets/bf2c638e-e0c4-4107-b28e-74cbf8bc6343)

After setting up SLA plans, we can configure help topics, which help the end user categorize the type of issue they are encountering. Let's create a help topic for "Business Critical Outage," which may apply if customers cannot access mobile banking.
 -Admin Panel -> Manage -> Help Topics
 ![image](https://github.com/user-attachments/assets/81f07adc-ee75-4008-8529-e1e7441d84ae)

</p>
<br />
