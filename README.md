<h1>Active Directory Home Lab 🧪</h1>

<h2>Description 📃</h2>
The project entails setting up a virtual machine on Microsoft Azure to function as a honeypot, monitoring real-time RDP brute-force attacks globally. A tailored PowerShell script is used to gather and sift through Windows Event Viewer logs, identifying failed login attempts to the virtual machine by attackers and then utilizing a third-party API data collection tool to plot their geographic locations.
<br />

## Tools and Technologies Utilized ⚙️:

1. **Windows 10 ISO:** Deployed for creating and managing the honeypot environment.
2. **Windows Server 2019:** Employed to meticulously sift through Windows Event Viewer logs, isolating failed RDP events.
3. **Oracle Virtualbox:** Utilized to establish a secure connection with the virtual machine.
4. **Windows PowerShell:** Integrated for tracking and analyzing geographical data via API.

<h2>Environments Used 💻</h2>

- <b>Windows 10 ISO</b> (22H2)
- <b>Windows Server 2019</b>

<h2>Key Takeways 📝</h2>

- <b>Running a honeypot on a virtual machine allows for isolation from the rest of the network, minimizing the risk of compromising other systems if the honeypot is breached.
- <b>Running the honeypot exposed me to a diverse array of attacker tactics, granting me invaluable insights into their behaviors, motivations, and techniques for breaching systems.
- <b>Building the honeypot required a multifaceted skill set encompassing networking, system administration, scripting, and data analysis. This journey significantly enhanced my proficiency in these areas.

<h2>Project Walk-Through 🚶:</h2>

<p align="center">
Install Oracle Virtual Box + Extension Pack: <br/>
<img src="https://i.imgur.com/EbXqRzn.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XuLwYKt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install Windows 10 ISO (64-bit) + Windows Server 2019 ISO (64-bit):
<br />
<img src="https://i.imgur.com/uAw1Ipp.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/fbMUoBE.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Launch Oracle Virtual Box + Create New: <br/>
<img src="https://i.imgur.com/aF72NrO.png" height="25%" width="25%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XP3TnaL.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a New Virtual Box Instance: <br/>
<img src="https://i.imgur.com/duSTaFZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/0dWXEzM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/GURL48r.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Before launching the VM, configure these "Network" tab settings: <br/>
<img src="https://i.imgur.com/hsDgWr5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Usk4nHs.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/YP8RhPT.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now launch the VM and Install Windows Server 2019: <br/>
<img src="https://i.imgur.com/SuXMVNf.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/JxlCsyk.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Choose the Custom Installation: <br/>
<img src="https://i.imgur.com/0Up0E1M.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/KVtNIkP.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/IW77iIM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now create an Administrator password and log into VM: <br/>
<img src="https://i.imgur.com/EKs5FtQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/5GV4S4e.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
In VM, press "Insert Guest Additions CD Image" and Install to provide better mouse input:  <br/>
<img src="https://i.imgur.com/d4EeVKV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/CxBZq8X.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eLds6y9.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/0qmqeyG.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/o3xKXH1.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/R8x1Moo.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Choose to "Reboot Later" and manually shut down the VM: <br/>
<img src="https://i.imgur.com/tgQiu7V.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/BQaQZZ3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open the Domain Controller VM again and log in:  <br/>
<img src="https://i.imgur.com/dDA6I2l.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/kZGOcpR.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the bottom right, open Network tab on the taskbar and configure the "Internet" and "Internal" Networks:  <br/>
<img src="https://i.imgur.com/8F6Xvwo.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/oTCF0aw.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/IiVP80g.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Ei3j2xO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/llRzmJY.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Hnb8OrJ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/hTkS0xE.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rH0lxvS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to "Internal Network" Properties and configure the following static IPv4 address:  <br/>
<img src="https://i.imgur.com/hO8rXh0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/RbUpK0y.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Rename the PC to "DomainController" and Reboot:  <br/>
<img src="https://i.imgur.com/W06Eyql.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/7Oc1LOE.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/CjNPPpd.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DJnIFgV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open "Server Manager" and Install "Active Directory Domain Services":  <br/>
<img src="https://i.imgur.com/RDrrUod.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/9FRYxH3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/et8fk04.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/FcbHm0k.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Dnm2qkH.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/AziqZyz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/uuq1CJr.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/9FTNClY.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Deploy the Active Directory Domain Services and Reboot the PC:  <br/>
<img src="https://i.imgur.com/EDX9D4h.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Zypsbap.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/9QEJb2U.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3RCkA3t.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/TdxiDs6.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Q4GPtO2.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Lg9Yyes.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/gmMdqDp.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/fGoZ5VH.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/CPtbtjc.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sign in again and open "Active Directory Users and Computers":  <br/>
<img src="https://i.imgur.com/at5zEjA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/8CMilW1.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Within "mydomain.com" create a new Organizational Unit (OU) called "ADMINS":  <br/>
<img src="https://i.imgur.com/w3VJE3W.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new administrator user and assign administrator privileges:  <br/>
<img src="https://i.imgur.com/jbooPKH.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/BgOkRDy.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rIbA3j5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rDRDHNd.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sign out of the current account and sign into the newly created administrator account:  <br/>
<img src="https://i.imgur.com/uOaBabh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HWtkph5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
In "Server Manager," go to "Add roles and features" and enable "Remote Access" and "Routing":  <br/>
<img src="https://i.imgur.com/mRlfhSS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DLPeXqF.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DjrMkTq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/D3k8NqL.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to "Tools" in the top right corner and right-click on "DOMAINCONTROLLER (local)" to configure a "NAT Internet Connection":  <br/>
<img src="https://i.imgur.com/HjLLUrD.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/MQtHSH0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/7Y0ofcX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/M2y61fw.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to "Add Roles and Features" and we are going to add a DHCP Server for the network:  <br/>
<img src="https://i.imgur.com/FQPsUv4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/4bQeZWu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/I7eiduq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Under "Tools" open "DHCP" and create a new scope:  <br/>
<img src="https://i.imgur.com/VEMivTN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/QUU6uZl.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/P4J0RCl.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DCOVQ8c.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/nEDQyQq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/hFRhyGG.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/IoRCUij.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/cB0Xx9n.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
*this next config is only suitable for home lab setups (allowing the domain controller to access the internet to install the "fake users" Powershell script:  <br/>
<img src="https://i.imgur.com/PkkOL6D.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/qXHkgGb.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/shkP3iD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Hh35TsO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/cvLvFaM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add in your unique API key into the script:  <br/>
<img src="https://i.imgur.com/hdVlVQD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Q4gZpXk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Save the Script onto Desktop:  <br/>
<img src="https://i.imgur.com/oUXyydG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run the script and go to C:\ProgramData\$($LOGFILE_NAME) on the VM to access the log file login attempts are pasted to:  <br/>
<img src="https://i.imgur.com/U2ITVaJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/7wtweCD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/i9sZWYn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Copy the Notepad on the VM and paste it into a Notepad on the Host PC:  <br/>
<img src="https://i.imgur.com/v38roHM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Save the Notepad on the Host PC to the desktop:  <br/>
<img src="https://i.imgur.com/sZdcjnL.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a custom log from the notepad note on the Host PC and route it from the log on the VM:  <br/>
<img src="https://i.imgur.com/xPA6sWm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/bmCgzQN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Copy and paste the "Query_Log_Organizer" and run:  <br/>
<img src="https://i.imgur.com/CUIfxcV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open MS Sentinel and Create a new workbook:  <br/>
<img src="https://i.imgur.com/1jUOPkE.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add a new query and run "Query_Log_Organizer":  <br/>
<img src="https://i.imgur.com/FXH9DVk.png" height="15%" width="15%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Yug7svW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now wait a few hours for attackers to attempt to brute force login to the VM:  <br/>
<img src="https://i.imgur.com/qRSEf7q.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WhHVJRs.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DrAGkKD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
