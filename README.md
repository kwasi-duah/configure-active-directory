<p align="center"> <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/> </p> <h1>Setting Up Active Directory in Azure: Easy Walkthrough</h1> This tutorial explains how to set up and use Active Directory (a tool to manage users and computers) inside Microsoft Azure. It's like creating a big address book for a computer network that keeps everything organized! 🖥️
<h2>What You Need</h2>
Microsoft Azure: A place to create virtual computers (called Virtual Machines or VMs).
Remote Desktop: A way to connect to those virtual computers.
Active Directory Domain Services: The tool we’ll set up to manage users and permissions.
PowerShell: A helper tool to automate tasks.
<h2>What We’re Using</h2>
Windows Server 2022 (for the main computer running the directory).
Windows 10 (for a normal computer connecting to the network).
<h2>What We’ll Do</h2>
Create the virtual computers in Azure.
Make sure they can "talk" to each other.
Install Active Directory and set it up.
Create admin and regular user accounts.
Add a computer to the network.
Allow users to log in remotely.
Add more users to the directory.
<h2>Step-by-Step Guide</h2>
Step 1: Create Virtual Computers in Azure
We’ll create two virtual computers:

DC-1 (Domain Controller): Think of this as the boss computer that keeps everything in check.
Client-1: A regular computer that will connect to the boss computer.
Here’s how it looks:

<p align="center"> <img src="https://i.imgur.com/gaAzjvb.png" alt="Creating the Domain Controller"/> </p>
Step 2: Make Sure They Can Talk to Each Other
We’ll send a “ping” from Client-1 to DC-1 (a way for one computer to say, “Hi, are you there?”).
If the ping doesn’t work, we’ll allow it by turning on a setting in the firewall.
<p align="center"> <img src="https://i.imgur.com/8o3OfjY.png" alt="Ping Success"/> </p>
Step 3: Install and Set Up Active Directory
On DC-1, we’ll install Active Directory, which turns it into the "Directory Boss."

We’ll create a domain (like a team name) called myadproject.com.
<p align="center"> <img src="https://i.imgur.com/zi15fw4.png" alt="Domain Setup"/> </p>
Step 4: Create Admin and Regular User Accounts
In Active Directory, we’ll:

Create folders (called Organizational Units) to organize users: Admins and Employees.
Add an admin user (e.g., Jane Admin) and give them special permissions.
<p align="center"> <img src="https://i.imgur.com/v02CBPI.png" alt="Organizing Users"/> </p>
Step 5: Add Client-1 to the Domain
Client-1 will join the team! This connects it to the domain (myadproject.com), so it follows the boss computer’s rules.

<p align="center"> <img src="https://i.imgur.com/50wszcP.png" alt="Joining Domain"/> </p>
Step 6: Set Up Remote Desktop for Users
We’ll allow regular users to use Remote Desktop to log in to Client-1.

<p align="center"> <img src="https://i.imgur.com/8BfpT3s.png" alt="Remote Desktop Settings"/> </p>
Step 7: Add More Users with a Script
Instead of adding users one by one, we’ll run a PowerShell script to quickly create lots of users.

These users will be part of the Employees group.
We’ll log in with one of these accounts to make sure it works.
<p align="center"> <img src="https://i.imgur.com/ZZCfiCp.png" alt="User Accounts"/> </p>
<h2>Clean Up</h2> When you’re done, don’t forget to delete everything in Azure to avoid charges!
<h2>Final Thoughts</h2> This walkthrough is a great way to learn about setting up Active Directory and managing a network. It’s like being the librarian of a big digital library!
