<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

STEP 1:

Welcome to my first in-depth IT tutorial! In this session, we’ll begin by setting up a Virtual Machine (VM) using the Microsoft Azure portal (portal.azure.com). A VM acts as a remote computer, allowing us to work in a secure environment without impacting our physical machine. This helps prevent potential system issues and provides a clean setup for repeatedly testing and replicating our lab.
Start by creating a resource group and naming it "osTicket". Then, proceed to create a VM with 2-4 CPUs—for this tutorial, I’ll be using 4 CPUs.

![image](https://github.com/user-attachments/assets/169d4df9-9cbc-436e-a447-41c3d16b2c88)

STEP 2:

Next, if you're using a Mac, you must download Microsoft Remote Desktop from the App Store to connect to your newly created VM. Use the Microsoft Remote Desktop (RDP) app on your Mac and enter the public IPv4 address to establish the connection. If you're on a Windows device, you can connect using Remote Desktop Connection.

![image](https://github.com/user-attachments/assets/95037a62-06bb-4406-bac4-cf510a28539f)

STEP 3:

Now that you're connected to your VM, the next step is to enable IIS. Go to the Control Panel, then select Uninstall a program. On the left, click Turn Windows features on or off. A list will pop up, and from there, enable Internet Information Services.

![image](https://github.com/user-attachments/assets/1c631a9e-d2c1-4a6c-8016-b381f1b5b095)

STEP 4:

With IIS enabled, the next step is to install the Web Platform Installer. You can find everything you need to get osTicket set up by following this link:[ Web Platform Installer Download](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0). Just click the link, download the installer, and run it to move forward with the setup. From the “osTicket-Installation-Files” folder, we will install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) and the Rewrite Module (rewrite_amd64_en-US.msi)

![image](https://github.com/user-attachments/assets/8a94079e-240e-4798-8a49-7ea89b44f8a7)

STEP 5:

Next, make a new folder called PHP on your computer C:\. Then, go to the osTicket-Installation-Files folder and find the file named php-7.3.8-nts-Win32-VC15-x86.zip. Right-click on the file and choose to unzip it into the C:\PHP folder you just created.

![image](https://github.com/user-attachments/assets/9e36b690-47bc-47e5-aba9-c226edb3c0ce)


STEP 7:

In the “osTicket-Installation-Files” folder, find and run VC_redist.x86.exe to install it.
Next, in the same folder, find and run mysql-5.5.62-win32.msi to install MySQL.

![image](https://github.com/user-attachments/assets/1976ecd7-32a8-4c76-8ffb-e29dbf9d29aa)

STEP 8:

Open Internet Information Services(IIS) as an Administrator (right-click and choose "Run as Administrator"). In IIS, select osTicket  > sites > default website. look for PHP Manager and click on it. Then, click Register PHP and select this file: C:\PHP\php-cgi.exe. To finish, restart IIS by stopping the server and starting it again.

![image](https://github.com/user-attachments/assets/14841298-1458-41bf-9aff-1908c0217c17)


STEP 9:
Find the "osTicket-Installation-Files" folder on your computer. Inside, you’ll see a file called "osTicket-v1.15.8.zip"—right-click it and select Extract or Unzip to open it. You’ll now see a folder named "upload". Copy this folder. Go to "C:\inetpub\wwwroot" (this is where your website files are stored). Paste the "upload" folder into "C:\inetpub\wwwroot". Rename the "upload" folder to "osTicket" (right-click, select Rename, and type osTicket).

![image](https://github.com/user-attachments/assets/f0aeb083-9b48-46fa-9d58-9eb1a3648568)


STEP 10:

Restart IIS by opening it, stopping the server, and then starting it again. Next, go to Sites > Default > osTicket. On the right side, click *"Browse :80" to open osTicket.

![image](https://github.com/user-attachments/assets/bae48a2e-6dca-4630-b00a-21cf7a62977b)

STEP 11:

Some features are turned off, so go to IIS > Sites > Default > osTicket, open PHP Manager, click Enable or disable an extension, Enable php_imap.dll, php_intl.dll, and php_opcache.dll, then refresh the osTicket page in your browser to see the changes.

![image](https://github.com/user-attachments/assets/9bc85459-8ffe-42b2-a166-511cde1f7ced)

STEP 12:




















