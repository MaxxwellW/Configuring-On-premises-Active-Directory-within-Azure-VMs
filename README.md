<p align="center">
<img src="https://i.imgur.com/bLpBiQ8.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises File Sharing Configuration through the Cloud</h1>
This tutorial outlines the implementation and allocation of file sharing within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computers)
- Remote Desktop
- File Explorer

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

- Creating Files & Creating Permissions as Admin for file sharing
- Attempting to access files as Newtork User
- Attempting to Create within Files as Newtork User

<h2>Demonstration and Steps</h2>

On DC-1, on the C:\ drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”
<p>
<img src="https://i.imgur.com/n0oLLHo.png" />
</p>
<p>


Set the following permissions (share the folder)

</p>
<br />

<p>
<img src="https://i.imgur.com/XddNo2X.png" />
</p>
<p>
 “read-access”, Group: “Domain Users”, Permission: “Read”



</p>
<br />

<p>
<img src="https://i.imgur.com/LFC4KvP.png" />
</p>
<p>
 “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”
<p>
<img src="https://i.imgur.com/lGLAI4w.png" />
</p>
<p>
“no-access”, Group: “Domain Admins”, “Permissions: “Read/Write”
Do not assign anything to the "accounting" file
<p>
<img src="https://i.imgur.com/FnlDv0c.png" />
</p>
<p>

Attempt to access each file shares as a normal user
<p>
<img src="https://i.imgur.com/j1g6P0z.png" />
</p>
<p>
Since there no share properties for "accounting" then it does not show for the user.
<p>
Try to create new text document in "read-access" 
<p>
<img src="https://i.imgur.com/zarPGzx.png" />
</p>
<p>
  
Create a new text document in "write-access"

<p>
<img src="https://i.imgur.com/7nuKflc.png" />
</p>
<p>
And as shown, the user is free to perform certain file share actions due to prior configuration
