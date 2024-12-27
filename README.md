<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- **Microsoft Azure**: Demonstrating cloud platform proficiency with Virtual Machines and resource management.
- **Remote Desktop**: Leveraging remote tools for efficient system access and management.
- **Internet Information Services (IIS)**: Configuring and optimizing web servers for application hosting.

<h2>Operating Systems Used</h2>

- **Windows 10 (21H2)**: Configured to meet the requirements of a production-like environment.

<h2>List of Prerequisites</h2>

1. Create and manage a Virtual Machine in Azure:
   - Windows 10 with 4 vCPUs for optimal performance.
   - Configured secure access with credentials (`labuser`, `osTicketPassword1!`).

2. Download and manage installation files:
   - osTicket Installation Files.
   - PHP 7.3.8 for scripting capabilities.
   - MySQL 5.5.62 for database management.

3. Install and configure IIS with CGI support:
   - Ensured compatibility with web-based applications.

4. Install and configure necessary software:
   - PHP Manager for IIS.
   - Rewrite Module for URL management.
   - Visual C++ Redistributable (VC_redist.x86.exe).

5. Configure MySQL for database operations:
   - Standard Configuration with secure root credentials.

6. Set Up PHP and integrate it with IIS:
   - Registered PHP for seamless server-side scripting.

7. Use HeidiSQL for advanced database management:
   - Created and managed osTicket-specific databases.

<h2>Installation Steps</h2>

### Step 1: Virtual Machine Setup
1. Created an Azure Virtual Machine named `osticket-vm` with Windows 10 and 4 vCPUs.
2. Accessed the VM securely using Remote Desktop.

### Step 2: Install IIS and Dependencies
1. Enabled IIS with CGI to support web application hosting.
2. Installed and configured:
   - PHP Manager for IIS.
   - Rewrite Module for IIS.
3. Created and prepared the `C:\PHP` directory with PHP 7.3.8 files.
4. Installed Visual C++ Redistributable for system compatibility.

### Step 3: Install and Configure MySQL
1. Installed MySQL 5.5.62 with Standard Configuration.
2. Set root credentials (`root/root`) for secure database operations.

### Step 4: Configure IIS for osTicket
1. Registered PHP with IIS via PHP Manager for enhanced functionality.
2. Reloaded IIS to apply configurations and tested PHP functionality.

### Step 5: Install osTicket
1. Unzipped `osTicket-v1.15.8.zip` and deployed it to `C:\inetpub\wwwroot`.
2. Renamed the deployment folder to "osTicket" and reloaded IIS.
3. Enabled critical PHP extensions:
   - `php_imap.dll`
   - `php_intl.dll`
   - `php_opcache.dll`
4. Configured `ost-config.php` with secure permissions.

### Step 6: Finalize osTicket Setup
1. Completed browser-based setup, including:
   - Configuring Helpdesk Name and Default Email.
   - Setting up the MySQL database "osTicket".
2. Utilized HeidiSQL to create and manage the osTicket database.
3. Verified successful installation by accessing the osTicket login page.

### Step 7: Post-Installation Cleanup
1. Removed the `setup` directory to secure the installation.
2. Set `ost-config.php` to "Read" only to prevent unauthorized changes.

<h2>Skills Demonstrated</h2>

- **Cloud Resource Management**: Provisioning and managing virtual machines in Azure.
- **Web Server Configuration**: Expertise in setting up and configuring IIS.
- **Database Administration**: Managing MySQL databases with HeidiSQL.
- **Software Installation and Integration**: Seamless integration of PHP and osTicket components.
- **Problem-Solving**: Troubleshooting installation issues and ensuring system compatibility.

By following this guide, you will have successfully installed and configured osTicket on a Windows 10 virtual machine. This comprehensive process showcases proficiency in cloud platforms, system administration, and application deployment.
