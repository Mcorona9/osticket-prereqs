
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This lab outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />





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
<p>
Once you are connected to your VM, you need to enable Internet Information Services (IIS). To do this, follow these steps: access the Control Panel, select "Uninstall a program," then choose "Turn Windows features on or off" on the left-hand side. A list will appear, and you can enable Internet Information Services from there.
</p>  
<img src="https://i.imgur.com/SdlRwfh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<p>


 </p>
 <img src="https://i.imgur.com/eJ1MzcR.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.imgur.com/fLBjpG4.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<p>
To enable additional extensions in IIS Manager, you can follow these steps. First, navigate to Sites -> Default -> osTicket in the IIS Manager interface. Once you've reached the osTicket site, double-click on PHP Manager. This will open the PHP Manager window. From there, click on the "Disable or enable an extension" option. In the list of extensions, locate and enable "php_intl.dll" and "php_opcache.dll". After enabling these extensions, don't forget to refresh the osTicket webserver to apply the changes. Take a moment to observe the changes, ensuring that the "Intl Extension" is now successfully enabled. By following these steps, you will be able to enable the specified extensions and witness the desired changes in the osTicket webserver.

</p>
<img src="https://i.imgur.com/0lBLso9.png "60%" width="60%" alt="Disk Sanitization Steps"/>

<p> By following the aforementioned steps, your setup should resemble somthing like the image above.

                                                                                       

</p>

<p>
To complete the task, navigate to the directory C:\inetpub\wwwroot\osTicket\include\ and locate the file named ost-sampleconfig.php. Rename this file to ost-config.php. Next, right-click on ost-config.php and select "Properties." In the Properties window, go to the "Security" tab and click on the "Edit" button. From the list of group or user names, choose "Everyone" and grant "Full control" permissions. Apply the changes and disable inheritance, removing any existing permissions inherited from the parent folder. These steps will successfully rename the file, assign necessary permissions, and disable inheritance for ost-config.php.


</p>
<p>

</P>
<img src="https://i.imgur.com/9TEYn0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>
After completing the previous steps, proceed to set up osTicket in your browser. Click on the "Continue" button to proceed. You will be prompted to provide a name for your Helpdesk, so choose a name that suits your preference. Additionally, select a default email address that will receive emails from customers who submit tickets. This email address will serve as the point of contact for customer inquiries.
</p>
<img src="https://i.imgur.com/F2aCjWX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>

 <img src="https://i.imgur.com/MnCmrTq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
With the successful completion of the osTicket setup, you can now expect osTicket to be fully operational and running smoothly. Congratulations on reaching this milestone! Now, let's proceed to the next task: post-installation configuration.
 
 
 
