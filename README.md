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
<p align="center">
  <img src="https://i.imgur.com/UucYORd.png" width="80%" alt="Enabling IIS"/>
</p>
<p>
Within Azure, click "virtual machines" at the top of the home page. Next, click the "Create" button at the top right of your screen and select "Virtual machine." 
Next, input your project details. 
<ul>
<li>Under resource groups, create a new one for this project.</li>
<li>Under Image, select "Windows 10 Pro, Version 22H2 - x64 Gen2."</li>`
<li>Under size, select 2 vcpus.</li>
<li>At the bottom check the licensing box.</li>
</ul>
You can give your virtual machine any name you would like. I would suggest documenting the username and password you create for your virtual machine, as we will need them to log in later.
</p>
<p>
Then click "Review + create" in the bottom right of your screen, and click "create" in the bottom right of the next screen.
Once your virtual machine has been created you can remotely connect to it.
</p>
<p>
First, open the "Remote Desktop Connection" application, which you can find by searching for it in the start menu.
</p>
<p>
Next, within Azure, view your virtual machine and copy it's public ip address on the right side of the screen. Paste the address into the Remote Desktop Connection application and click "connect."
</p>
Then, enter the username and password you created for your virtual machine and click "connect."
</p>

---

### Step 2: Download the [osTicket-installation-files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) and Unzip It Onto Your Desktop

<p align="center">
  <img src="https://i.imgur.com/NTmTyX2.png" width="80%" alt="Installing PHP"/>
</p>
<p>
First, copy this link into the browser on the virtual machine you created in step 1. Your browser will ask if you would like to download this file, click "Download anyway." 
</p>
<p>
Once the file is downloaded, click the manila folder in the top right,
right click the file named "osTicket-Installation-Files," and extract the file to your desktop.
</p>

---

### Step 3: Install / Enable IIS in Windows

<p align="center">
  <img src="https://i.imgur.com/nEFFoR7.png" width="80%" alt="Installing PHP"/>
</p>
<p>
Within your virtual machine, open the start menu and open Control Panel. Click "Uninstall a program."
</p>
<p align="center">
  <img src="https://i.imgur.com/Pivdke3.png" width="80%" alt="Installing PHP"/>
<p>
  Click "Turn Windows features on or off" on the left side of the screen.
</p>
<p align="center">
  <img src="https://i.imgur.com/cSUnM8k.png" width="80%" alt="Installing PHP"/>
<p>
Check the "Internet Information Services" box and expand it by clicking on the plus sign to the left of the box.
</p>
<p>
Expand "World Wide Web Services."
</p>
Expand "Application Development Features" and check the box next to "CGI." Then click "OK."


### Step 4: Download and Install osTicket

> Replace this section with a real screenshot of the osTicket installation page when available.

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
