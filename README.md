# Active-Directory Project
In this project I am going to go through Active Directory and it's useful features that are important and widely used in IT environments in a variety of use of cases. Some of the topics that are going to be covered in this project are;
- Changing the PC's name
- Setting a Static IP
- Installing Active Directory tools and configuring a new forest
- Setting up a domain name
- Creating Organisational Units
- Creating User Accounts
- Creating Group Policy (password policies and mapping drives)
- Setting up DHCP and DNS
- Configuring File Sharing & Permissions
## Changing the Pc's name
1. Go to Settings > System > About > Rename this PC
2. Type in your preffered name, for example WindowsServer
3. Resart the Pc and verify if the name change has been successful. 
## Setting a Static IP
1. Go to Local Server on the left hand side of the screen, then click on the IPV4 address hyperlink
![Screenshot 2025-05-26 202933](https://github.com/user-attachments/assets/4f9b7104-cdf9-4553-ac1a-ec7b6ce2ec32)
2. Then click on the network adapter and then go to properties, then locate Internet Protocol version 4 and then click it. Here you will have the option to set up the IP Address, Subnet Mask and Default Gateway. You can use the servers current IP address which you would find with ipconfig in command prompt.
   
![image](https://github.com/user-attachments/assets/4d899861-c16a-47b7-8424-1b95f1377833)
## Installing Active Directory tools and configuring a new forest
1. Go to Dashboard > Add Roles and Features > Click next until you reach server roles.
2. Locate Active Directory Domain Services and click it, then click add features
3. Keep clicking until you reach the install option
4. Before we leave this tab, make sure that the "promote this server to a Domain Controller" is clicked is this is what we need to carry out our configurations later on.
5. With the new page click on add a new forest, then type your root domain name (e.g. mydomain.local). Click next to create a password, then keep clicking next until you reach install.
6. The server would restart.

![image](https://github.com/user-attachments/assets/71c33666-c4eb-497a-84cf-39b13067c95d)
## Creating Organisational units
1. Now that your server has Active Directory configured, carry out a windows serach for "Active Directory Users and Computers".
2. Find your domain name from the lists > right click > New > Organisational Unit
3. Name your Organisational Unit, for example "Departments"
4. Under this Parent OU, You can create Sub OU's for your departments with the same process, for example IT.
5. Then within the IT department you can configure objects such as users, computers, printers etc through the same process.
   
![image](https://github.com/user-attachments/assets/d985b88d-299b-4a56-a6de-ea2a8653fe66)![image](https://github.com/user-attachments/assets/28a747a9-7910-4f62-81d2-87ba9d387d59)
## Joining a Computer to a Domain
1. For this section, you will need a Windows 10 Pro or Enterprise Virtual Machine configured and running.
2. Open Ethernet settings > Change adapter options.
3. The DNS server settings has to be changed here so that the client can establish communication with the Windows server.
4. Double click Ethernet > properties > TCP/IPV4 > "Use the following DNS server addresses". For preffered DNS, use the Domain Servers IP address and alterate can be 8.8.8.8.
5. Verify that you can communicate with the domain server by pinging its IP address, using the command ping in command prompt.
6. To join the domain  









