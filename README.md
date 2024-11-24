# UpdateServerIP_toStaticIP_ChangeHostname_EnableRemoteConnection

## Objective
[Brief Objective]

### GitHub Project Description

The goal of this project is the exploration of updating a Window Server 2025 virtual machine IP address from dynamic IP to a Static IP address. We also be updating the Host name of the server and enabling remote connection. Please note some information has been changed to minimize security risk associated with this project.

- Updating Window Server 2025 IP address from dynamic to Static.
- Changing the Window Server Host name.
- Enabling remote connection to the Window Server virtual machine.
  

The goal is to make it easier to learn and apply best practices for installation of VMware, Window Server 2025 Iso, creation of the Virtual Machine and basic configuration.


[Tools Used]

VMware
Server Manager
Command Line
PowerShell Terminal


## Steps
[Dynamic IP to Static IP]


Launch your VM by selecting Power on your Virtual Machine. 


![image](https://github.com/user-attachments/assets/7bc3f9de-b559-44df-8580-c79f5a8089d0)

 

From Server Manager, select Local Server. Here we can see the computer name (host name), whether remote desktop is enabled or disabled, and IP connection information.


![image](https://github.com/user-attachments/assets/01a353dd-7388-476d-800b-fa20eea88753)

![image](https://github.com/user-attachments/assets/baf8fff4-14b7-446e-8bcc-8f2905f2a9cb)

 

From the start menu, run Command Prompt as an administrator, type **Ipconfig/all** and press enter to find your connection information. If you see DHCP Enabled set to Yes, that means dynamic IP is enabled. Your new IP address and subnet needs to be of the same series.
 

![image](https://github.com/user-attachments/assets/25cbf06e-7cdd-444f-a4dc-885c82b93512)

![image](https://github.com/user-attachments/assets/bb911a36-98d1-4c76-8a76-60d26d535f4b)
![image](https://github.com/user-attachments/assets/8f8e127d-f25d-4a59-9af9-8bb4631ef5be)


 
 

From server manager, open the Ethernet information, select Ipv4 properties.
 

![image](https://github.com/user-attachments/assets/746e4af5-0a18-4277-bf9e-e61270a14df9)

![image](https://github.com/user-attachments/assets/44bcbd30-cf85-432f-bbf3-1cc8edde71f9)
 

From properties, select the option use the following IP Address: and create an IP address a part of the series provides from the command line: prompt. Example 192.168.202.125, from here, enter the subnet mask, default gateway, and prefer the DNS server provided by the command line prompt. Once complete click ok.
 
![image](https://github.com/user-attachments/assets/24b03eaf-1ed7-4f9a-a75f-51ea0be9ff34)



[Enable Remote Desktop]

To enable the Remote Desktop connection, double click on the disabled portion, navigate to the remote tab, select allow remote connections to this computer, click apply, and click okay.
 

![image](https://github.com/user-attachments/assets/003982a5-d8a0-4903-8fce-db5616233b84)

![image](https://github.com/user-attachments/assets/bc235a57-a203-4ecd-bc37-7287271b77a6)

 


[Update Hostname]

To update the computer name, click on the field to take to you into the system properties. Select rename server name by clicking change, update the host name, select apply and click okay to update the computer name.
 
 

 ![image](https://github.com/user-attachments/assets/f5820039-f3b2-4fa1-a838-159496a560a1)

 ![image](https://github.com/user-attachments/assets/36afece4-42de-48c0-ae0e-b357fe021a1a)

 ![image](https://github.com/user-attachments/assets/0fae04fb-9497-4c8d-83b2-a8ad6c7bd44f)

 


[Server Update]

Now restart your server and open Server Manager to verify that all information has been changed. The host name should be updated, the remote desktop should be enabled, and IP address series updated. Web browsers should open and next we will open up the power shell terminal. From the PowerShell terminal type **ping google.com** When you packet responses, this completes verify the Static IP Address was setup correctly. 
 

![image](https://github.com/user-attachments/assets/17a43450-7a9e-4ce6-a886-939bb87eaf5d)

 ![image](https://github.com/user-attachments/assets/31cfd229-fcf4-4d7c-939d-a124580ec292)

![image](https://github.com/user-attachments/assets/419c14b0-4c7b-4d14-9ddb-42530f64474d)


This completes enabling of remote desktop connection, Host name update, and changing the servers' IP address from Dynamic to Static.
