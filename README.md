# UpdateServerIP_toStaticIP_ChangeHostname_EnableRemoteConnection

## Objective
[Brief Objective]

### GitHub Project Description

This project aims to explore updating a Windows Server 2025 virtual machine's IP address from dynamic to Static. We will also update the server's Hostname and enable remote connections. Please note that some information has been changed to minimize the security risk associated with this project.
- Updating Window Server 2025 IP address from dynamic to Static.
- Changing the Window Server Hostname.
- Enabling remote connection to the Windows Server virtual machine.

The goal of this project is to equip you with the knowledge and skills to apply best practices for installing VMware and Windows Server 2025 ISO, creating a Virtual Machine, and basic configuration. By the end of this project, you will be able to perform these tasks with ease and confidence.

[Tools Used]

VMware
Server Manager
Command Line
PowerShell Terminal

## Steps
[Dynamic IP to Static IP]


Launch your VM by selecting Power on your Virtual Machine. 



![image](https://github.com/user-attachments/assets/7bc3f9de-b559-44df-8580-c79f5a8089d0)

 

From Server Manager, select Local Server. Here we can see the computer name (hostname), whether the remote desktop is enabled or disabled, and IP connection information.


![image](https://github.com/user-attachments/assets/01a353dd-7388-476d-800b-fa20eea88753)

![image](https://github.com/user-attachments/assets/baf8fff4-14b7-446e-8bcc-8f2905f2a9cb)

 

To find your connection information, open the Start menu and run Command Prompt as an administrator. Type **ipconfig /all** and press Enter. Look for the line that says "DHCP Enabled." If it is set to Yes, then dynamic IP assignment is enabled. Ensure that your new IP address and subnet are in the same series.
 

![image](https://github.com/user-attachments/assets/25cbf06e-7cdd-444f-a4dc-885c82b93512)

![image](https://github.com/user-attachments/assets/bb911a36-98d1-4c76-8a76-60d26d535f4b)
![image](https://github.com/user-attachments/assets/8f8e127d-f25d-4a59-9af9-8bb4631ef5be)


 
 

From server manager, open the Ethernet information, select Ipv4 properties.
 

![image](https://github.com/user-attachments/assets/746e4af5-0a18-4277-bf9e-e61270a14df9)

![image](https://github.com/user-attachments/assets/44bcbd30-cf85-432f-bbf3-1cc8edde71f9)
 

To configure the IP address, go to the properties section and select the option to use the following IP address. Choose an IP address from the given series, for example, 192.168.202.125. Next, enter the subnet mask and default gateway. Make sure to prefer the DNS server provided in the command line prompt. Once you have completed these steps, click OK.
 
![image](https://github.com/user-attachments/assets/24b03eaf-1ed7-4f9a-a75f-51ea0be9ff34)



[Enable Remote Desktop]

To enable the Remote Desktop connection, double click on the disabled portion, navigate to the remote tab, select allow remote connections to this computer, click apply, and click okay.
 

![image](https://github.com/user-attachments/assets/003982a5-d8a0-4903-8fce-db5616233b84)

![image](https://github.com/user-attachments/assets/bc235a57-a203-4ecd-bc37-7287271b77a6)

 


[Update Hostname]


To update the computer name, click on the Computer Name field to access the system properties. Then, select the option to rename the server by clicking Change. Update the hostname, select Apply, and click OK to confirm the new computer name.
 
 

 ![image](https://github.com/user-attachments/assets/f5820039-f3b2-4fa1-a838-159496a560a1)

 ![image](https://github.com/user-attachments/assets/36afece4-42de-48c0-ae0e-b357fe021a1a)

 ![image](https://github.com/user-attachments/assets/0fae04fb-9497-4c8d-83b2-a8ad6c7bd44f)

 


[Server Update]


Restart your server and then open the Server Manager to verify that all the information has been updated. The hostname should be changed, Remote Desktop should be enabled, and the IP address series should reflect the new settings. Next, open your web browsers, and then launch the PowerShell terminal. In the PowerShell terminal, type **ping google.com**. If you receive a response from the packet, it indicates that the static IP address has been set up correctly.
 

![image](https://github.com/user-attachments/assets/17a43450-7a9e-4ce6-a886-939bb87eaf5d)

 ![image](https://github.com/user-attachments/assets/31cfd229-fcf4-4d7c-939d-a124580ec292)

![image](https://github.com/user-attachments/assets/419c14b0-4c7b-4d14-9ddb-42530f64474d)


This completes enabling of remote desktop connection, Host name update, and changing the servers' IP address from Dynamic to Static.
