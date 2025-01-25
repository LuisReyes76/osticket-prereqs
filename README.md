<h1>Work in Progress 
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
- Remote login
- osTicket Installation
  

<h2>Installation Steps</h2>

<p>
</p>
<p>
Hi!, and welcome to my first tutorial. First thing that we will need to create is a Virtual Machine "VM" using Microsoft Azure. We will be using a VM which is a remote computer, We are using a VM in order to protect our physical machine just in case something breaks. Create a resource group and title it "osTicket-vm". Afterwards create the VM with 2-4 CPUs. In this example I will be using 2 CPUs. As you can see on the image below.

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

</p>
<br />
