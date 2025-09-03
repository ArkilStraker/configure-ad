# Configure-AD
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 Pro (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- install Active Directory Domain Services
- Promote as a DC: Setup a new forest as mydomain.com
- Create an Organizational Unit (OU) called “_EMPLOYEES” and a new OU named “_ADMINS”
- Create a Domain Admin user within the domain
- Join Client-1 to your domain (mydomain.com)

<h2>DConfiguration Steps</h2>

<p>
<img width="374" height="287" alt="image" src="https://github.com/user-attachments/assets/1fd6350f-89fb-4bb4-9684-835f4ba3e68f" /> <img width="420" height="202" alt="image" src="https://github.com/user-attachments/assets/9117e333-22ff-4f65-b822-1c33f19d4585" />


</p>
<p>
Installing Active Directory Domain Services on a Windows Server VM transforms it into a Domain Controller, giving you centralized control to manage users, computers, groups, security policies, everything in your IT environment. It’s the foundation for building a secure, scalable Windows-based network; whether on-prem or in the cloud (e.g., Azure).
</p>
<br />

<p>
<img width="349" height="137" alt="image" src="https://github.com/user-attachments/assets/c4b4b7b2-8fe1-47d4-a625-99158968cc77" /> <img width="494" height="262" alt="image" src="https://github.com/user-attachments/assets/cc3fdedf-adb6-4e20-bb02-641f49dc1262" />

</p>
<p>
By promoting the server to a Domain Controller and creating a new forest named mydomain.com, you’ve built the foundation of an Active Directory environment. This DC now handles authentication, identity management, and DNS resolution within the new domain. From here, additional DCs, users, and computers can be added to grow the network.
</p>
<br />

<p>
<img width="563" height="441" alt="image" src="https://github.com/user-attachments/assets/c44c12f4-27be-42f0-84a9-b6138c160c72" />

  <img width="279" height="189" alt="image" src="https://github.com/user-attachments/assets/8b38c6e6-3f65-4a9c-a74d-dc9f0d6506e7" /> <img width="293" height="188" alt="image" src="https://github.com/user-attachments/assets/91838074-7167-4da6-ac9f-5055272583f2" />


</p>
<p>
By creating the _EMPLOYEES and _ADMINS OUs, you’ve structured your Active Directory environment into two logical groups: one for standard employees and one for privileged administrators. This makes it easier to apply policies, manage accounts, and maintain a secure, organized directory.
</p>
<br />

<p>
<img width="368" height="324" alt="image" src="https://github.com/user-attachments/assets/77b22986-9cc1-4703-960f-6803429a535a" /> <img width="281" height="296" alt="image" src="https://github.com/user-attachments/assets/66037c5b-7207-4345-a69c-41e340283995" />
  <img width="273" height="279" alt="image" src="https://github.com/user-attachments/assets/e853f93e-bf62-4daa-9f51-64e647f2ccb6" /> <img width="211" height="310" alt="image" src="https://github.com/user-attachments/assets/4d8082eb-ccab-417f-a897-9342f7ba89e9" /> <img width="230" height="340" alt="image" src="https://github.com/user-attachments/assets/78cd8095-ab14-4a45-b53b-6e701f0b4be2" />





</p>
<p>
Creating a new user and adding them to the Domain Admins group, you give that account full administrative rights across the entire domain. This is best practice over relying solely on the built-in Administrator account. The new Domain Admin can now log in, manage AD resources, and administer the forest and domain.
</p>
<br />

<p>
<img width="473" height="150" alt="image" src="https://github.com/user-attachments/assets/41a9457d-ee45-4d9b-b992-5fdb5933d714" /> <img width="211" height="273" alt="image" src="https://github.com/user-attachments/assets/bc88e286-dbc2-4339-9e10-e2fa72d3f765" />
<img width="495" height="364" alt="image" src="https://github.com/user-attachments/assets/a05bcd8d-b159-4e87-bce9-9c9360e969ac" /> <img width="393" height="141" alt="image" src="https://github.com/user-attachments/assets/3a923451-a3a5-4f35-8a5e-0dd01944596f" />



</p>
<p>
By joining Client-1 to mydomain.com, the machine is now managed by the Domain Controller. Users can log in with domain accounts, policies can be applied, and IT admins can centrally manage the computer. This step integrates Client-1 into the Active Directory environment, making it part of the secure, organized domain network.
</p>
<br />
