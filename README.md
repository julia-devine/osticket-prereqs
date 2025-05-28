<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket Logo" width="250"/>
</p>

<h1 align="center">osTicket Installation Guide</h1>
<p align="center">
  Step-by-step tutorial for setting up the open-source ticketing system <strong>osTicket</strong> on a Windows environment.
</p>

---

## 📺 Video Demonstration

- ▶️ [How To Install osTicket with Prerequisites](https://www.youtube.com) *(YouTube)*

---

## 🧰 Technologies and Environments Used

- **Microsoft Azure** – Virtual Machines / Compute
- **Remote Desktop Protocol (RDP)**
- **Internet Information Services (IIS)**
- **PHP, MySQL**
- **osTicket**

---

## 🖥️ Operating System

- **Windows 10** (Version 21H2)

---

## ✅ Prerequisites

Ensure the following are installed or set up prior to osTicket installation:

1. Microsoft Web Platform Installer
2. Internet Information Services (IIS)
3. PHP Manager for IIS
4. MySQL Database Server
5. osTicket Installation Files

---

## ⚙️ Installation Steps

Below are the general steps to install and configure osTicket. Replace the placeholder text with real steps if needed.

### Step 1: Setup Windows VM and Enable IIS

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Enabling IIS"/>
</p>
<p>
Start by creating a Windows VM on Azure. Use the Server Manager to enable IIS and install required roles and features.
</p>

---

### Step 2: Install PHP and Configure IIS

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing PHP"/>
</p>
<p>
Use the Web Platform Installer to install PHP and the necessary IIS extensions. Ensure PHP Manager is properly configured.
</p>

---

### Step 3: Install and Configure MySQL

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="MySQL Configuration"/>
</p>
<p>
Download and install MySQL Server. Create a database and user account specifically for osTicket.
</p>

---

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

## 📬 Contact & Portfolio

> Replace this with your actual contact info or GitHub/LinkedIn profile links.

---
