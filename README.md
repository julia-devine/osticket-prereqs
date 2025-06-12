<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket Logo" width="250"/>
</p>

<h1 align="center">osTicket Installation Guide</h1>
<p align="center">
  Step-by-step tutorial for setting up the open-source ticketing system <strong>osTicket</strong> on a Windows environment.
</p>

---

##  Technologies and Environments Used

- **Microsoft Azure** – Virtual Machines / Computer
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
<li>Under Image, select Windows 10 Pro, Version 22H2 - x64 Gen2.</li>
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
<li>Right click the file named osTicket-Installation-Files and extract the file to your desktop</li>
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

---

### Step 5: Unzip the php-7.3.8-nts-Win32-VC15-x86.zip Folder Into the C:\PHP Directory
In order to complete this step we first need to create a PHP folder in our C Drive.
<p>
  <ul>
    <li>Open a new file explorer tab by right clicking the manila folder in your taskbar. Click File Explorer.</li>
    <li>On the left side of the screen click Windows (C:).</li>
    <li>Right click anywhere within the File Explorer window and click New > Folder and name the folder PHP.</li>
  </ul>
  </p>
  <p align="center">
  <img src="https://i.imgur.com/PTm0AQv.png" width="80%" alt="Installing PHP"/>
<p>
    <li>Back in the osTicket-Installation-Files folder right click the php-7.3.8-nts-Win32-VC15-x86.zip folder and extract it to the C:\PHP folder you created previously.</li>
</p>

---

### Step 6: Install VC_redist.x86.exe and MySQL 5.5.62
<p>
  MySQL is a database that osTicket will use to store all of our data, such as user accounts and ticketing information.
  <ul>
    <li>In the osTicket-Installation-Files folder double click VC_redist.x86.exe and follow the installation steps.</li>
    <li>In the osTicket-Installation-Files folder double click mysql-5.5.62-win32.msi. Select Next > Next > Typical > Install.</li>
    <li>Once installed you will be prompted to finish the setup. Before you click Finish, check the box labeled Launch the MySQL Instance Configuration Wizard > Finish. The configuration Wizard should automatically launch.</li>
  </ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/8XsXRaU.png" width="80%" alt="Installing PHP"/>
<p>
  <ul>
    <li>Winthin the Configuration Wizard select Next > Standard Configuration > Next > Next.</li>
  </ul>
  On the next screen you are prompted to enter a password. You may chose any password you would like. I would suggest documenting the password as it will be used for both the username and password.
</p>
<p>
  <ul>
    <li>Click Next > Execute > Finish.</li>
  </ul>
</p>

---

### Step 7: Configure PHP
<p>
  <ul>
    <li>Search for IIS in the start menu.</li>
    <li>Right click IIS and Run as administrator.</li>
     </ul>
</p>
<p>
Next, we are going to register PHP from within IIS, making the web server aware PHP exists on the computer.

<ul>
  <li>Double click PHP Manager > Register new PHP version and select the PHP folder you made in step 5 > php-cgi > Open > OK. </li>
</ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/DExwFsE.png" width="80%" alt="Installing PHP"/p>
<p>
  Finally, we are going to reload the web server.
  <ul>
    <li>On the left side of the screen click osticket-vm (osticket-vm\Juliadevine). (The name of your vm will vary)</li>
    <li>On the right side of the screen click stop. Once it has fully stopped click start.</li>
  </ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/8sJSUs9.png" width="80%" alt="Installing PHP"/>
</p>

---

### Step 8: Install osTicket v1.15.8
<p>
  <ul>
    <li>Back in the osTicket-Installation-Files folder unzip the osTicket-v1.15.8.zip folder.</li>
    <li>Right click the manila folder in your taskbar at the bottom of your screen and select file explorer to open a new window. </li>
    <li>On the left side of the window select Windows (C:) > inetpub > wwwroot, and copy the upload folder from the osTicket-v1.15.8 folder into c:\inetpub\wwwroot.</li>
  </ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/lUXmYRE.png" width="80%" alt="Installing PHP"/p>
  <ul>
    <li>Within c:\inetpub\wwwroot, Rename the upload folder to osTicket</li>
    <li>Follow Step 7 to reload IIS.</li>
  </ul>
</p>

---

### Step 9: Enable Extensions
<p>
First, we will browse to the osTicket site to ensure it loads properly and no mistakes have been made.
  <ul>
    <li>Within IIS Manager, select PHP Manager</li>
    <li>On the left side of the window select the drop down for osTicket-vm(osticket-vm\Juliadevine) > Sites drop down > Default Web Site drop down > and select osTicket</li>
    <li>On the right side of the window click Browse*:80 (http)</li>
  </ul>
</p>
<p align="center">
  <img src="https://i.imgur.com/skThztQ.png" width="80%" alt="Installing PHP"/p>
<p>
This is what you should see pop up.
</p>
<p align="center">
  <img src="https://i.imgur.com/JTFOFDT.png" width="80%" alt="Installing PHP"/p>
