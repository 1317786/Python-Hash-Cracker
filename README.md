<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
This project is designed to deepen understanding of Windows Server 2019 by configuring and managing a domain controller within a virtualized network. We will explore essential network services such as DNS and DHCP, and learn how to manage user and group policies effectively. This hands-on experience will not only enhance practical skills in network administration but also provide insights into the critical role of Active Directory in maintaining organizational security and efficiency. <br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Server 2019</b>

<h2>Takeaways</h2>

- <b>Active Directory Setup and Configuration</b>: Successfully established a home lab environment featuring Active Directory on Windows Server 2019. Demonstrated competency in setting up a virtual network using Oracle VirtualBox, installing and configuring a domain controller, and setting up necessary network interfaces for internal and external communications. This hands-on experience solidified foundational skills in managing Active Directory roles and features.

- <b>Domain and Network Services Implementation</b>: Gained practical experience in configuring DNS and DHCP services essential for network management within the Active Directory framework. Proficient in creating and managing Active Directory objects such as users, groups, and organizational units, enhancing skills in network resource administration and user management.

- <b>Security Policy and Access Management:</b>: Developed a thorough understanding of group policies and user access management within Active Directory. Implemented security policies that enforce user authentication and authorization practices, improving the security posture of the network. This project showcased the ability to manage and secure network resources effectively through Active Directory.

<h2>Program walk-through:</h2>

<p align="center">
Create the first VM which will also act as our Domain Controller and house Active Directory: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure 2 network adapters with one being used to connect to the outside internet and the other being used to connect to Virtual Box private network that the clients can connect to:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install Active Directory and create Domain name: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure NAT and Routing so clients on the private network can reach the internet through the Domain Controller:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure DHCP on Domain Controller so when Windows 10 machine is created it can automatically get an IP address:  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Powershell script that will create 1k+ users in Active Directory:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create second VM and install Windows 10 on it which will connect to the private virtual box network. Will then be named CLIENT1 and we will log into it with one of the domain accounts:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
