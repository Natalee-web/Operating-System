# Project: User & File Management (Windows PowerShell)
Operating Systems and You – Becoming a Power User

###  Project Overview
This project demonstrates proficiency in core Operating System internals using the Windows Command Line Interface (CLI). It covers user account creation, security group management, Access Control Lists (ACLs), and automated package installation.

---
  Steps Taken

 1. User and Group Management
I utilized administrative PowerShell to establish a secure user environment.
* **Command used:** `New-LocalUser -Name "Course_Trainee"`
* **Action:** Created a new local user and a custom local group called `Project_Group`.
* **Verification:** Used `Get-LocalGroupMember` to confirm the user was successfully nested within the group.
 <img width="800" height="247" alt="powershell1" src="https://github.com/user-attachments/assets/7ee8c77c-1246-4596-8bc0-91e59a26bbac" />


 2. File System Permissions
To demonstrate knowledge of file systems and security:
* **Command used:** `icacls "C:\ProjectData" /grant "Project_Group:(OI)(CI)R"`
* **Action:** I created a new directory and modified its **Access Control List (ACL)**.
* **Result:** This ensured the **Principle of Least Privilege**, granting the group Read-only access while protecting the root system.
 <img width="811" height="266" alt="powershell2" src="https://github.com/user-attachments/assets/0a704e9a-56d2-422e-a9ff-198e28128cc3" />


 3. Package Management
Instead of using a GUI, I managed software deployment via the CLI.
* **Command used:** `winget install Notepad++.Notepad++`
* **Action:** Used the **Windows Package Manager (Winget)** to search for and install a software package.
* **Reasoning:** CLI installation is more efficient, scriptable, and secure than manual web downloads.
  <img width="837" height="288" alt="powershell3" src="https://github.com/user-attachments/assets/2e3c2fe5-7544-42ca-833b-3404b25849eb" />

Evidence of Completion
<img width="986" height="623" alt="powershell4" src="https://github.com/user-attachments/assets/92209d0c-60da-4535-b929-67b218ad1c8e" />

 Key Concepts Learned
* **Least Privilege:** Only giving a user the exact permissions they need.
* **CLI Efficiency:** Managing an OS faster through PowerShell than a GUI.
* **Package Repositories:** Using trusted sources like Winget for software integrity.
