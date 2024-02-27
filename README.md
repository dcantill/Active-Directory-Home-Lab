<h1>Active Directory Home Lab 🧪</h1>

<h2>Description 📃</h2>
The project involves setting up a home lab environment using virtual machines managed by Active Directory to simulate an enterprise-level network. By deploying Windows Server 2019 and running a custom PowerShell script to create thousands of users, Active Directory will be used to centralize user authentication and several other access control features. This dynamic environment aims to replicate an enterprise-level network administration, serving as a valuable platform for  research and training.

<br />
<br />

<p align="center">
<img src="https://i.imgur.com/dpJMbuM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />

## Tools and Technologies Utilized ⚙️:

1. **Windows 10 ISO:** Deployed to mimic a client/user computer operating within the domain.
2. **Windows Server 2019:** Deployed as the Domain Controller to configure server management tools and features within the home lab.
3. **Oracle Virtualbox:** Utilized to deploy Windows 10 and Windows Server 2019 virtual machines.
4. **Windows PowerShell:** Integrated for generating thousands of "users" to manage in Active Directory.

<h2>Environments Used 💻</h2>

- <b>Windows 10 ISO</b> (22H2)
- <b>Windows Server 2019</b> (V1809)

<h2>Key Takeways 📝</h2>

- <b>Simulating a large-scale user network with virtual machines and Active Directory enables comprehensive testing and validation of network security measures, policies, and procedures within a controlled environment.
- <b>Implementing monitoring tools and custom PowerShell scripts provides real-time visibility into user activities, facilitates automated administrative tasks, and enhances incident response capabilities, contributing to a more secure and efficient network infrastructure.
- <b>Engaging in the setup and management of the Active Directory home lab fosters a deep understanding of network administration, cybersecurity principles, and scripting techniques, offering valuable hands-on experience and skill development opportunities.</b>

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
Edit the plaintext document to include your name, save it, and run it as administrator in Windows Powershell ISE:  <br/>
<img src="https://i.imgur.com/kSUVxzO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/nJnWd0U.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/v3TvKgz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open the Powershell script and set the Execution Policy to "unrestricted" (this is a security feature only allowed in a home lab setup):  <br/>
<img src="https://i.imgur.com/JRjtsVg.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HecDoqV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Explaining the script we will run...  <br/>
<img src="https://i.imgur.com/U2ITVaJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/7wtweCD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/i9sZWYn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. All users will use the same password:  <br/>
<img src="https://i.imgur.com/Yqrb8HA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Users will get their username by mixing their first initial and last name:  <br/>
<img src="https://i.imgur.com/zkMly4v.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. All users will be configured with the following settings for their profile:  <br/>
<img src="https://i.imgur.com/2vVKf6g.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Change the directory to where the .txt name file is located and ensure the document is located there:  <br/>
<img src="https://i.imgur.com/emDw16n.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run the script and wait for it to generate all users (make sure to run PowerShell ISE as administrator):  <br/>
<img src="https://i.imgur.com/qGdWHIQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ChPSUaz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/wNZiOY5.png" height="150%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/28Lp1eT.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open Active Directory Users and Computer and refresh your domain to view the created users:  <br/>
<img src="https://i.imgur.com/1ynKTa1.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Return to Oracle VirtualBox and create a new virtual machine:  <br/>
<img src="https://i.imgur.com/IsTFtfn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/d5C9Y6n.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/sJVl2pP.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adjust system and network settings then install the Windows 10 ISO Image:  <br/>
<img src="https://i.imgur.com/NFDIBCT.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/KW5eXDd.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/zGeeA2L.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/EOvUSQV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adjust system and network settings then install the Windows 10 ISO Image:  <br/>
<img src="https://i.imgur.com/2oxShSh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/bYKoThU.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/dfNp1x6.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/nLJQU7F.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Continue through the Windows OS setup and configure a local account:  <br/>
<img src="https://i.imgur.com/WrqFeH4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/W2J3quu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ebFeh8B.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/NK4AzWM.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the Windows 10 Client virtual machine, run "ipconfig" to verify your internet is functional:  <br/>
<img src="https://i.imgur.com/GI50tzI.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/T6Jqui3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Back in the Windows Server 2019 Domain Controller virtual machine, open Active Directory "DHCP" and add a router in the server options:  <br/>
<img src="https://i.imgur.com/mIET9UN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
Press "Refresh":  <br/>
<img src="https://i.imgur.com/yf514Ex.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
Add a router and Restart "All Tasks":  <br/>
<img src="https://i.imgur.com/uA0wlGF.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eQMB60v.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Back in the "Client" Virtual Machine, run "ipconfig /renew":  <br/>
<img src="https://i.imgur.com/AQLawSS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run "ping www.google.com to ensure the internet connectivity is running functionally:  <br/>
<img src="https://i.imgur.com/3CQkSAK.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Right-click on the Windows Home Button and open system and press "Rename this PC (advanced)":  <br/>
<img src="https://i.imgur.com/Dv1mwgZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
Rename the PC and connect it to our domain "mydomain.com":  <br/>
<img src="https://i.imgur.com/9rFFL93.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/lEtW20Z.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Y3Br6yN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://imgur.com/ezHDNw8.png" height="20%" width="20%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Active Directory, we now see the "CLIENT1" computer connected to the domain:  <br/>
<img src="https://imgur.com/6Ki1ZVZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://imgur.com/GRtZrsl.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the "CLIENT1" virtual machine, try signing into one of the generated users to mimic a domain user logging into their account:
<img src="https://imgur.com/aW5RR4P.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://imgur.com/h0MFOdX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
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
