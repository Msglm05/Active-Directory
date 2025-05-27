# Active-Directory Project
In this project I am going to go through Active Directory and it's useful features that are important and widely used in IT environments in a variety of use of cases. Some of the topics that are going to be covered in this project are;
- Setting a Static IP
- Installing Active Directory tools and configuring a new forest
- Setting up a domain name
- Creating a user
- Creating Groups
- Creating Organisational Units
- Creating User Accounts
- Creating Group Policy (password policies and mapping drives)
- Setting up DHCP and DNS
- Configuring File Sharing & Permissions
## Setting a Static IP
1. Go to Local Server on the left hand side of the screen, then click on the IPV4 address hyperlink
![Screenshot 2025-05-26 202933](https://github.com/user-attachments/assets/4f9b7104-cdf9-4553-ac1a-ec7b6ce2ec32)
2. Then click on the network adapter and then go to properties, then locate Internet Protocol version 4 and then click it. Here you will have the option to set up the IP Address, Subnet Mask and Default Gateway. You can use the servers current IP address which you would find with ipconfig in command prompt.
![image](https://github.com/user-attachments/assets/3d72ec40-71da-4879-8b6d-f0d142b73b38)
## Installing Active Directory tools and configuring a new forest
1. Go to Dashboard > Add Roles and Features > Click next until you reach server roles.
2. Locate Active Directory Domain Services and click it, then click add features
3. Keep clicking until you reach the install option
4. Before we leave this tab, make sure that the "promote this server to a Domain Controller" is clicked is this is what we need to carry out our configurations later on.
5. With the new page click on add a new forest, then type your root domain name (e.g. mydomain.local). Click next to create a password, then keep clicking next until you reach install.
6. The server would restart.

![image](https://github.com/user-attachments/assets/71c33666-c4eb-497a-84cf-39b13067c95d)
## Creating a user
1. Do a windows search of Active Directory Users and Computers
2. Locate your domain name on the left hand side of the panel and expand it
3. Right click Users > New > User
4. Enter in the details of this user, then click next and configure a password
5. Under the General tab, you can add a desription to the user, e.g. IT Staff
![image](https://github.com/user-attachments/assets/735f609c-1e7d-40ed-bceb-872d77045b32)
## Creating Groups 
You can create groups in areas such as the users area under your domain name or areas such as your organisational units.
1. Locate where you want to create the gorup and right click > Group
2. Enter group name, you can then move created users to this group and set configuartions such as assigning permissions and security policies and more.
3. For example, for your organisational unit for IT you can assign a group policy object that installs IT Specific software.
## Creating Organisational units
1. Now that your server has Active Directory configured, carry out a windows serach for "Active Directory Users and Computers".
2. Find your domain name from the lists > right click > New > Organisational Unit
3. Name your Organisational Unit, for example "Departments"
4. Under this Parent OU, You can create Sub OU's for your departments with the same process, for example IT.
5. Then within the IT department you can configure objects such as users, computers, printers etc through the same process.
##









