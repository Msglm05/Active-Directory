# Active-Directory Project
❗More details on the Extneded Active Directory project can be found on my Linkedin https://www.linkedin.com/in/mahmutsaglam/details/projects/

In this project I am going to go through Active Directory and it's useful features that are important and widely used in IT environments in a variety of use of cases. Some of the topics that are going to be covered in this project are;
## Table of contents
- [Installing Active Directory tools and configuring a new forest](#installing-active-directory-tools-and-configuring-a-new-forest)
- [Configure network settings for the server](#configure-network-settings-for-the-server)
- [Creating a user](#creating-a-user)
- [Creating Groups](#creating-groups)
- [Creating Organisational Units](#creating-organisational-units)
- [Creating Group Policy Objects](#creating-group-policy-objects)
- [Setting account lockout policy](#setting-account-lockout-policy)

## Installing Active Directory tools and configuring a new forest
1. Go to Dashboard > Add Roles and Features > Click next until you reach server roles.
2. Locate Active Directory Domain Services, then click add features
3. Keep clicking until you reach the install option
4. Before we leave this tab, make sure that the "promote this server to a Domain Controller" is clicked as this is what we need to carry out our configurations later on.
5. With the new page click on add a new forest, then type your root domain name (e.g. mydomain.local). Click next to create a password, then keep clicking next until you reach install.
6. The server would restart.
   
![image](https://github.com/user-attachments/assets/71c33666-c4eb-497a-84cf-39b13067c95d)
   
## Configure network settings for the server
1. Go to Local Server on the left hand side of the screen, then click on the IPV4 address hyperlink
![Screenshot 2025-05-26 202933](https://github.com/user-attachments/assets/4f9b7104-cdf9-4553-ac1a-ec7b6ce2ec32)
2. Then click on the network adapter and then go to properties, then locate Internet Protocol version 4. Here you will have the option to set up the IP Address, Subnet Mask and Default Gateway.

<img width="400" height="650" alt="image" src="https://github.com/user-attachments/assets/2902db49-fb40-4664-bc2d-76c5bdb88b4f" />

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
2. Enter group name, you can then move created users to this group and set configuartions such as assigning permissions, security policies and more.
3. For example, for your organisational unit for IT you can assign a group policy object that installs IT Specific software.
## Creating Organisational units
1. Now that your server has Active Directory configured, carry out a windows serach for "Active Directory Users and Computers".
2. Find your domain name from the lists > right click > New > Organisational Unit
3. Name your Organisational Unit, for example "Departments"
4. Under this Parent OU, You can create Sub OU's for your departments with the same process, for example IT.
5. Then within the IT department you can configure objects such as users, computers, printers etc through the same process.
## Creating Group Policy Objects 
1. On the server machine go to settings, under Administrative Tools select Group Policy Management
2. Under the domain, go to group policy objects 
3. For testing purposes, create a folder on a drive of the server machine, for example on drive C. Right click the folder that you have created > properties > sharing (share over the network) > advanced sharing (NTFS permissions), here you can share the folder and set permissions.
4. NTFS Permissions can then be used to enforce what users are able to do with the files/folders
   
![Screenshot 2025-05-28 074532](https://github.com/user-attachments/assets/f1f6aa2e-9d71-4882-a36d-886cc498e913)

4. Open up Group Policy Management > under domain locate Group Policy Objects > right click and new > then name, e.g. Mapped drive for HR
5. Right click Mapped drive > edit > under User Configuration Expand preferences > expand Windows Settings > then locate Drive Maps.
6. Right click empty space > New > Mapped Drive > set the option to create > put in the file path of the shared folder that you created > assign a drive letter and then press apply.
7. You can then link this Mapped Drive GPO under you Organisational units that you have created in Active directory.
8. You can do this by locating the OU in the Group Policy Management console > right click > link existing GPO.
![Screenshot 2025-05-28 075801](https://github.com/user-attachments/assets/6b961d27-a1c6-49c2-99eb-d31ae8dc7253)
## Setting account lockout policy
1. Create a new GPO called "Account lockout Policy" under your domain in the Group Policy Objects section.
2. Then right click this GPO > Edit > Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy.
3. Here you can confiure your settings and apply where you desire.
<img width="689" height="141" alt="image" src="https://github.com/user-attachments/assets/e70753d3-e6af-4b0b-8564-63283ce503d9" />












