# Active-Directory Project
In this project I am going to go through Active Directory and it's useful features that are important and widely used in IT environments in a variety of use of cases. Some of the topics that are going to be covered in this project are;
## Table of contents
- [Setting a Static IP](#setting-a-static-ip)
- [Installing Active Directory tools and configuring a new forest](#instaling-active-directory-tools-and-configuring-a-new-forest)
- [Creating a user](#creating-a-user)
- [Creating Groups](#creating-groups)
- [Creating Organisational Units](#creating-organisational-units)
- [Creating Group Policy Objects](#creating-group-policy-objects)
- [Setting account lockout policy](#setting-account-lockout-policy)
  
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
1. Locate where you want to create the group and right click > Group
2. Enter group name, you can then move created users to this group and set configuartions such as assigning permissions and security policies and more.
3. For example, for your organisational unit for IT you can assign a group policy object that installs IT Specific software.
## Creating Organisational units
1. Now that your server has Active Directory configured, carry out a windows serach for "Active Directory Users and Computers".
2. Find your domain name from the lists > right click > New > Organisational Unit
3. Name your Organisational Unit, for example "Departments"
4. Under this Parent OU, You can create Sub OU's for your departments with the same process, for example IT.
5. Then within the IT department you can configure objects such as users, computers, printers etc through the same process.
## Creating Group Policy Objects 
1. On the server machiene go to settings, under Administrative Tools select Group Policy Management
2. Under the domain, go to group policy objects 
3. For testing purposes, create a folder on a drive of the server machine, for example on drive C. Right click the folder that you have created > properties > sharing > advanced sharing, here you can share the folder and set permissions.
   
![Screenshot 2025-05-28 074532](https://github.com/user-attachments/assets/f1f6aa2e-9d71-4882-a36d-886cc498e913)

5. Open up Group Policy Management > Under domain locate Group Policy Objects > right click and new > Then name, e.g. Mapped drive
6. Right click Mapped drive > edit > under User Configuration Expand preferences ? expand Windows Settings > then locate Drive Maps.
7. Right click empty space > New > Mapped Drive > put in the file path of the shared folder that you created > assign a drive letter and then press apply.
8. You can then link this Mapped Drive GPO under you Organisational units that you have created in Active directory.
9. You can do this by locating the OU in the Group Policy Management console > right click > link existing GPO.
![Screenshot 2025-05-28 075801](https://github.com/user-attachments/assets/6b961d27-a1c6-49c2-99eb-d31ae8dc7253)
## Setting account lockout policy
1. Create a new GPO called "Account lockout Policy" under your domain in the Group Policy Objects section.
2. Then right click this GPO > Edit > Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy.
3. Here you can confiure your settings and then link to your desired OU you want this to apply too.
![image](https://github.com/user-attachments/assets/65f1b9ff-0eb6-4456-bf3c-f7af0adc2408)











