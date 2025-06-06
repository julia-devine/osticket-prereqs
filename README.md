<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket Logo" width="250"/>
</p>

<h1 align="center">osTicket Installation Guide</h1>
<p align="center">
  Step-by-step tutorial for setting up the open-source ticketing system <strong>osTicket</strong> on a Windows environment.
</p>

---

##  Technologies and Environments Used

- **Microsoft Azure** – Virtual Machines / Compute
- **Remote Desktop Protocol (RDP)**
- **Internet Information Services (IIS)**
- **PHP, MySQL**
- **osTicket**

---

##  Operating System

- **Windows 10** (Version 21H2)

---

##  Prerequisites

Ensure the following are installed or set up prior to osTicket installation:

1. Microsoft Web Platform Installer
2. Internet Information Services (IIS)
3. PHP Manager for IIS
4. MySQL Database Server
5. osTicket Installation Files

---

##  Installation Steps

Below are the general steps to install and configure osTicket.
### Step 1: Create an Azure Virtual Machine
<p>
<ul>
<li>Within Azure, click virtual machines at the top of the home page.</li>
<li>Click the Create button at the top right of your screen and select Virtual machine.</li>
<li>Input your project details. </li>
<li>Under resource groups, create a new one for this project.</li>
<li>Under Image, select "Windows 10 Pro, Version 22H2 - x64 Gen2."</li>
<li>Under size, select 2 vcpus.</li>
<li>At the bottom check the licensing box.</li>
</ul>
</p>
<p>
You can give your virtual machine any name you would like. I would suggest documenting the username and password you create for your virtual machine, as we will need them to log in later.
</p>
<p>
<ul>
<li>On the bottom right of your screen select Review + create > create.</li>
</ul>
Once your virtual machine has been created you can remotely connect to it.
</p>
<p>
<ul>
<li>Open the Remote Desktop Connection application</li>
<li>Within Azure, view your virtual machine and copy it's public ip address on the right side of the screen, and Paste the address into the Remote Desktop Connection application and click connect.</li>
<li>Enter the username and password you created for your virtual machine and click connect.</li>
</ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/UucYORd.png" width="80%" alt="Enabling IIS"/>
</p>
---

### Step 2: Download the [osTicket-installation-files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) and Unzip It Onto Your Desktop

<p>
<ul>
<li>First, copy this link into the browser on the virtual machine you created in step 1. Your browser will ask if you would like to download this file, click Download anyway.</li>
<li>Once the file is downloaded, click the manila folder in the top right.</li>
<li>Right click the file named "osTicket-Installation-Files" and extract the file to your desktop</li>
</ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/NTmTyX2.png" width="80%" alt="Installing PHP"/>
</p>
---

### Step 3: Install / Enable IIS in Windows
<p>Internet Information Services (IIS) is a web server software that will provide us with the environment to host web applications such as osTicket, while allowing users access via a web browser.</p>
<p>
<ul>
<li>Within your virtual machine, open the start menu and open Control Panel.</li>
<li>Under Programs select Uninstall a program.</li>
</ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/nEFFoR7.png" width="80%" alt="Installing PHP"/>
</p>
<ul>
<li>Select Turn Windows features on or off on the left side of the screen.</li>
</ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/Pivdke3.png" width="80%" alt="Installing PHP"/>
<p>
  <ul>
  <li>Check the Internet Information Services box > World Wide Web Services > Application Development Features, and check the box next to CGI.</li>
  <li>Click OK</li>
  </ul>
</p>

<p align="center">
  <img src="https://i.imgur.com/cSUnM8k.png" width="80%" alt="Installing PHP"/>
<p>

### Step 4: Install PHP Manager and the Rewrite Module
<p>
  <ul>
   <li>In the osTicket-Installation-Files folder double click PHPManagerForIIS_V1.5.0 and follow the steps to install PHP Manager.</li>
   <li>Repeat the same steps for rewrite_amd64_en-US. </li>
  </ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/CmbLzbt.png" width="80%" alt="Installing PHP"/>
<p>

1. Download osTicket from the official website.
2. Extract files into `C:\inetpub\wwwroot\osTicket`.
3. Run the setup from your browser via `http://localhost/osTicket`.

---

### Step 5: Final Configuration and Test

- Complete the web-based setup.
- Assign proper file permissions.
- Verify that tickets can be created and emails are functioning.

---

##  Contact & Portfolio

> Replace this with your actual contact info or GitHub/LinkedIn profile links.

---
