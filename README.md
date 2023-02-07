<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2></h2>

Get more information on following:

- [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
- [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
- [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html) 
- [Agents](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html)
- [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html).
- [Service Level Agreement(SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)

<h2>Post Installation Setup Steps </h2>

<h3>Step 1: Log in into your osTicket Admin Panel </h3>

<p>
<img src="https://www.inmotionhosting.com/support/wp-content/uploads/2022/01/osticket-support-center-admin-1024x580.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Log in your username and password you setup last tutorial , If you miss the download and install setup osTicket 
  
<h3>Step 2: Configure Roles </h3>

<p align="center">
<img src="https://i.imgur.com/WBsMSsW.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/E5uOKgF.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>



- Make sure you are in admin panel (check top right to see which panel you are in)
	- If the top right says "agent" you are in the admin panel
- Select the Agents tab -> Roles -> Add New Role
	- Name : Supreme Admin
	- Select Permissions tab and check every box under the "Tickets", "Tasks" and "Knowledgebase" section
- Select Add Role
	


<h3>Step 3: Configure Departments</h3>

<p align="center">
<img src="https://i.imgur.com/UzSZ9GL.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Departments -> Add New Department 
	- Name: System Administrators
- Select Create Dept. 




<h3>Step 4:  Configure Teams
</h3>

<p align="center">
<img src="https://i.imgur.com/4EnXFT6.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Teams -> Add New Team
	- Name: Level II Support 
- Go to members tab and select yourself in "Select Agent" dropdown menu
- Select create team. 
	

<h3>Step 5: Allow anyone to create tickets</h3>

<p align="center">
<img src="" height="80%" width="80%" alt="Azure Free Account"/>

 Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Settings -> User Settings
	- Make sure box is unchecked: 
		- Registration Required: Require registration and login to create tickets 
			


<h3>Step 6: Configure Agents</h3>

<p align="center">
<img src="https://i.imgur.com/yVBvAE5.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>

-  Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Add New Agents
	- Name: Jane Doe
	- Email : jane.doe@osticket.com
	- Username: jane.doe
	- Click set password and uncheck box that says "send the agent a password reset email
		- Set your password to anything you like
		- uncheck box that says "require password change at next login
		- Select set
- Select Access tab 
	- Under Primary Department 
		- Select department dropdown menu -> System Administrators
		- Select Role dropdown menu -> Supreme Admin
	- Extended Accesss 
		- Select Department -> Support -> Add -> Supreme Admin
- Select Teams tab
	- Select team dropdown menu -> Level II Support
	- Select Add
- Select Create
- Create another agent and replace Jane with John.
	- Follow same steps as above except make some changes to Primary Department
		- Select department dropdown menu -> Support
		- Select Role dropdown menu -> View only
	- Extended Accesss 
		- Select Department -> Support -> Save Changes
 
     

<h3>Step 7: Configure Users
</h3>

- Make sure you are in Agent panel (check top right to see which panel you are in)
	- If the top right says "admin" you are in the agent panel
	
<p align="center">
<img src="https://i.imgur.com/UUqCK1d.png" height="80%" width="80%" alt="Azure Free Account"/>		
	
- Select Users tab to create user
	- Email Address: Karen@osticket.com
	- Full Name - Karen Karen
	- Select Add User
	
<p align="center">
<img src="https://i.imgur.com/wpTn12W.png" height="80%" width="80%" alt="Azure Free Account"/>			
	
 - Select user tab again to create another user
	- Email Address: Ken@osticket.com
	- Full Name - Ken Ken
	- Select Add User

<p align="center">
<img src="https://i.imgur.com/EXyy5Gq.png" height="80%" width="80%" alt="Azure Free Account"/>		

<h3>Step 8:  Configure Service Level Agreements (SLA)
</h3>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select Manage tab -> SLA -> Add New SLA Plan (We are creating 3)
	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/fMR4yMR.png" height="80%" width="80%" alt="Azure Free Account"/> <img src="https://i.imgur.com/3tQnihq.png" height="80%" width="80%" alt="Azure Free Services"/>
</p>

- Name: SEV-B
- Grace Period: 4
- Schedule dropdown menu: 24/7
- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/pAbQPEP.png" height="80%" width="80%" alt="Azure Free Account"/>

- Name: SEV-C 
- Grace Period: 8
- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S Holidays
- Select Add Plan

<p align="center">
<img src="https://i.imgur.com/5cgn0oz.png" height="80%" width="80%" alt="Azure Free Account"/>



<h3>Step 9:   Configure Help Topics
</h3>

-  Make sure you are in admin panel (check top right to see which panel you are in)
- Select Manage tab -> Help Topics -> Add New Help Topic (We will be adding 4)
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- Select Add Topic for each topic

<p align="center">
<img src="https://i.imgur.com/uFmSyqK.png" height="80%" width="80%" alt="Azure Free Account"/>

