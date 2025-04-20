<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="300"/>
</p>

<h1 align="center">osTicket - Prerequisites and Installation</h1>
<p>This tutorial outlines the prerequisites and step-by-step installation process of the open-source help desk ticketing system, osTicket.</p>

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
</ul>

<h2>Operating System Used</h2>
<ul>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>Installation Steps</h2>

<p><strong>Initial Preparation:</strong><br>
All necessary installation files for the osTicket setup were gathered and organized in one directory, including PHP, MySQL, PHP Manager for IIS, and supporting tools like Visual C++ Redistributable and URL Rewrite module to streamline the installation process.</p>
<img src="https://github.com/user-attachments/assets/17808195-6f0e-4b5b-b648-cddcad501b4f" width="600"/>

<h3>Step-by-Step Instructions</h3>
<ol>
  <li><strong>Create Azure VM and Set Up Credentials</strong></li>
  <li><strong>Log in to the VM via Remote Desktop</strong></li>
  <li><strong>Download and Extract osTicket Installation Files</strong></li>
  
  <li><strong>Install IIS with CGI Support</strong><br>
    Control Panel → Programs → Turn Windows features on or off → Check IIS, World Wide Web Services, Application Development Features, and CGI.
    <br><img src="https://github.com/user-attachments/assets/6e87ea67-612f-4644-9d1a-f5f018b85fbd" width="600"/>
  </li>

  <li><strong>Install PHP Manager for IIS</strong></li>
  <li><strong>Install IIS Rewrite Module</strong></li>

  <li><strong>Set Up PHP Directory and Install PHP</strong><br>
    Created a directory (C:\PHP) and installed PHP to support osTicket.
    <br><img src="https://github.com/user-attachments/assets/eac461d9-e336-417e-bcc3-eeaba9270173" width="600"/>
    <br><em>Extracting PHP Files to C:\PHP</em>
    <br><img src="https://github.com/user-attachments/assets/ea9aac4b-b696-4c0c-bd85-7c87d90def70" width="600"/>
  </li>

  <li><strong>Install Visual C++ Redistributable</strong></li>

  <li><strong>Install MySQL and Configure Database</strong><br>
    MySQL is used as the backend for storing tickets, users, and settings.
    <br><img src="https://github.com/user-attachments/assets/6355d6f1-c4fd-4406-afa5-aa20d22e319a" width="600"/>
    <img src="https://github.com/user-attachments/assets/079b9076-d561-47ad-85a9-4dda1c06623c" width="600"/>
    <img src="https://github.com/user-attachments/assets/86af05c2-8c37-4b1b-bd6f-4bab26472e40" width="600"/>
    <img src="https://github.com/user-attachments/assets/75e2075f-a2c7-4adf-beeb-91618111aa91" width="600"/>
  </li>

  <li><strong>Register PHP with IIS</strong><br>
    Ensures IIS can properly execute PHP scripts for osTicket.
    <br><img src="https://github.com/user-attachments/assets/8e807ea6-e848-4c0c-9afa-685930211b4d" width="600"/>
    <br><em>Restart IIS</em>
    <br><img src="https://github.com/user-attachments/assets/2967bd39-ad29-4869-8da7-c6bee0c37471" width="600"/>
  </li>

  <li><strong>Install osTicket v1.15.8</strong><br>
    Extracted the osTicket \"upload\" folder into <code>C:\inetpub\wwwroot</code>.
    <br><img src="https://github.com/user-attachments/assets/37b20590-3757-4c00-9076-275fa2fa0ec3" width="600"/>
    <img src="https://github.com/user-attachments/assets/ccb816dc-5048-4d4a-a0c3-42a2522d6ce6" width="600"/>
    <img src="https://github.com/user-attachments/assets/ce57a767-e9e3-4f4d-8ce4-93cb3dbe17d3" width="600"/>
  </li>

  <li><strong>Enable Required PHP Extensions</strong><br>
    Enabled:
    <ul>
      <li>php_imap.dll</li>
      <li>php_intl.dll</li>
      <li>php_opcache.dll</li>
    </ul>
    <img src="https://github.com/user-attachments/assets/e6292e67-51b8-47fd-acf5-1d7e0fc725a8" width="600"/>
    <img src="https://github.com/user-attachments/assets/c1afbdb0-3e57-46a6-bad5-ab6b99c287bb" width="600"/>
  </li>

  <li><strong>Configure osTicket Settings</strong><br>
    Renamed the sample file to <code>ost-config.php</code> to allow installation.
    <br><img src="https://github.com/user-attachments/assets/4c4c4983-0dca-441f-932d-642ef8ce7568" width="600"/>
  </li>

  <li><strong>Set File Permissions</strong><br>
    Gave full control to <code>ost-config.php</code> to allow read/write.
    <br><img src="https://github.com/user-attachments/assets/470b2967-7b2f-427f-84ec-3d25435b8b89" width="600"/>
  </li>

  <li><strong>Finalize osTicket Setup in Browser</strong><br>
    Configured site details and created the primary admin user.
    <br><img src="https://github.com/user-attachments/assets/99e5768d-dd36-453d-acf1-29207b199a92" width="600"/>
  </li>

  <li><strong>Create Database in HeidiSQL</strong><br>
    Created a MySQL database called <code>osTicket</code> to store ticket data.
    <br><img src="https://github.com/user-attachments/assets/eaadaa0c-0bcb-489b-acdb-1d90afc1bbf7" width="600"/>
  </li>

  <li><strong>Complete osTicket Installation</strong><br>
    Connected osTicket to the MySQL database using credentials.
    <br><img src="https://github.com/user-attachments/assets/59bfec85-0786-40ee-ba7f-d37c0a392006" width="600"/>
  </li>

  <li><strong>Verify Installation and Access Helpdesk</strong><br>
    Logged into the staff panel and verified default ticket creation.
    <br><img src="https://github.com/user-attachments/assets/b1777fff-db3a-4c5f-a67f-d3b87e072cd3" width="600"/>
  </li>
</ol>

<p>This concludes the full installation and configuration of a functional osTicket helpdesk system on a Windows environment using IIS and MySQL.</p>




