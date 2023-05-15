# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>
</p>
<p>
To begin, our first step will be to create a Virtual Machine through the Microsoft Azure portal. The Virtual Machine (VM) functions as a remote computer, and we will be utilizing it to safeguard our physical machine in case of any potential damage. Let's start by creating a resource group and naming it "osTicket". Following that, we can proceed to create a VM with 2-4 CPUs. 

 <img src="https://i.imgur.com/Jbtu809.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>Next, you can easily connect to your newly created VM by using Remote Desktop Protocol (RDP) and the public IPv4 address associated with it. 
</p>
<img src="https://i.imgur.com/S0j08P8.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
</p>
<p>
Next, you can easily connect to your newly created VM by using Remote Desktop Protocol (RDP) and the public IPv4 address associated with it.
</p>  
<img src="https://i.imgur.com/SdlRwfh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<p>
Once you are connected to your VM, you need to enable Internet Information Services (IIS). To do this, follow these steps: access the Control Panel, select "Uninstall a program," then choose "Turn Windows features on or off" on the left-hand side. A list will appear, and you can enable Internet Information Services from there.

 </p>
 <img src=https://i.imgur.com/lIAW8i0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>
Now that IIS is enabled, the next step is to install the Web Platform Installer. To download the necessary files for setting up osTicket, you can access the provided link: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. Simply click on the link and proceed to install the Web Platform Installer from there. This installer will provide you with all the required materials to get osTicket up and running smoothly.

</p>
<img src=https://i.imgur.com/TFHCo5t.png

 <p>
To proceed with the installation, let's navigate to the installation folders. First, download and install PHP Manager for IIS by executing the file "PHPManagerForIIS_V1.5.0.msi" from the Installation Files. Afterward, install the Rewrite Module by running the file "rewrite_amd64_en-US.msi" from the same folder. Once both installations are complete, create a new directory named "C:\PHP" on your system. These steps will help ensure the necessary components are set up properly for the next phase of the installation process
 
</p>
<img src="https://i.imgur.com/fwOgSLT.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p> 
 
<p>
Within PHP Manager, proceed to enable three specific extensions: php_imap.dll, php_intl.dll, and php_opcache.dll. Once these extensions are enabled, reload IIS Manager to ensure the changes take effect. Now, navigate to "Sites > Default > osTickets" in IIS Manager. On the right side of the interface, click on "Browse *:80" to effortlessly open the osTicket web-interface. By following these instructions, you will successfully enable the necessary extensions and gain access to the osTicket web-interface through IIS Manager.

</p>
<img src="https://i.imgur.com/0lBLso9.png "60%" width="60%" alt="Disk Sanitization Steps"/>

<p> By following the aforementioned steps, your setup should resemble somthing like this.

                                                                                       

</p>
<img src="https://i.imgur.com/fLBjpG4.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
</p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</P>
<img src="https://i.imgur.com/9TEYn0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<img src="https://i.imgur.com/F2aCjWX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket
Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and obsereve the changes "Intl Extension" should now be enabled. 

 <img src="https://i.imgur.com/MnCmrTq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
In clonclusion 
 
 
 
