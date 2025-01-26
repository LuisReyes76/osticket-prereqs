<h1>Work in Progress 
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Remote login
- osTicket Installation
  

<h2>Installation Steps</h2>

<p>
</p>
<p>
Hi and welcome to my first tutorial. The first thing that we will need to create is a Virtual Machine "VM" using Microsoft Azure. We are using a VM in order to protect our physical machine just in case something goes wrong. Create a resource group and title it "osTicket-vm". Afterwards create the VM with 2-4 CPUs. I will be using 2 CPUs as you can see on the image below.

![image](https://github.com/user-attachments/assets/1cc8aa24-9855-4863-8800-64442644bcf7)


The next step is going to be to remote access to that virtual machine. If you are using windows hit the start buttom and search "Remote Desktop Connection" on a Mac just search for "Microsoft Remote Desktop"


![image](https://github.com/user-attachments/assets/3c20db7d-0a33-407b-8d27-46f18b196106)


Don't forget to get the public IP address for the virtual machice "VM" you would need that to log into that VM. You can find it on you VM page on the "Essentials' area as you can see on the image below.

![image](https://github.com/user-attachments/assets/7c5e90e9-b96c-42c2-bef5-600530f6ab92)



<p>
The first thing we need to do after you connect to you VM you would need to Install / Enable IIS in Windows WITH CGI. To do this click on the start menu and search "Control Panel" then click on Programs andclick on " Turn Windows features on or off". 

![image](https://github.com/user-attachments/assets/47794452-106a-491d-b124-c70ff6f2fe5f)




Frist click on Internet Information Services "IIS" -> [X] then go to World Wide Web Services -> Application Development Features -> [X] CGI and hit ok. Below you can see the image on what you are looking for.

![image](https://github.com/user-attachments/assets/cada54fd-370f-4d48-bedf-26549a7b0e82)

Here is a link on the files you will need for the next steps -> https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

After you go to the link above and download the Zip file, you are going to un-zip and intstall the file called "PHPManagerForIIS_V1.5.0". Then install the file called "rewrite_amd64_en-US". Once you are done with this, you are going to create the directory C:\PHP (Folder) in your c: drive. The reason you are going making the new folder is because you need to un-zip a file called "php-7.3.8-nts-Win32-VC15-x86" which will go into that folder.

![image](https://github.com/user-attachments/assets/b5ea5e7f-05dd-444f-880e-cb6f49b1c843)

Next, From the “osTicket-Installation-Files” folder, install "VC_redist.x86.exe" and "mysql-5.5.62-win32.msi". When you are installing "mysql-5.5.62-win32.msi" make sure you are follow these step, Typical Setup ->
Launch Configuration Wizard (after install) -> Standard Configuration -> Username: root and Password: root (Please don't use root in real life). This needs to be done to make osTicket work.


Open IIS as an Admin, Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe). 

![image](https://github.com/user-attachments/assets/4873df76-0b4d-4886-b4f4-183c77fbea5c)

Reload IIS (Open IIS, Stop and Start the server)

![image](https://github.com/user-attachments/assets/5235e635-5a90-4685-a001-1220e8bb115c)

Now lets install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”. Open IIS, Stop and Start the server. Now we are going to try and open osTicket. With IIS, Go to sites -> Default -> osTicket
On the right, click “Browse *:80”. If you did everything right it should like the image below.

![image](https://github.com/user-attachments/assets/dfd52ee3-9886-443d-aee0-90b6db718059)


Note that some extensions are not enabled, Go back to IIS, sites -> Default -> osTicket. Double-click PHP Manager, Click “Enable or disable an extension”. Enable: php_imap.dll, php_intl.dll and php_opcache.dll.
Refresh the osTicket site in your browser, observe the changes

![image](https://github.com/user-attachments/assets/7375a107-3a91-4965-ac7d-d1522c31e40d)


</p>
<br />
