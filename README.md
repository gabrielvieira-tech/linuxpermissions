<p align="center">
  
![Image](https://github.com/user-attachments/assets/676e6021-54a3-4c02-9ac2-e338466ee5ba)

<h1>VPN - Homelab Tutorial</h1>
This toturial uses an Azure VM, Proton VPN, and WhatIsMyIPAddress.com to compare IP and geolocation across a personal machine, a remote VM, and a VPN inside the VM.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: VPN HOMELAB TUTORIAL ](https://youtu.be/BR5-kqFuU-k)

<h2>Environments and Technologies Used</h2>


- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Proton VPN Program and an account

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Computer/laptop
- 4gb RAM
- DUO CORE CPU
- Internet access
- Azure account


<h2> STEPS</h2>

<h2> Set Up a Virtual Machine in a Different Country</h2>

![Image](https://github.com/user-attachments/assets/6507cad6-e1b5-4d80-902c-724d3d53ac03)

<p>

To set up a virtual machine in another country using Azure, first log into the Azure Portal and create a new Windows 10 22h2 Virtual Machine, selecting a region in a different country (e.g., Germany or Japan). Create a resource group, choose a username and password during setup (make sure to save it in your notes). Once the VM is deployed, go to its overview page, copy the Public IP, and then go to the search bar at the bottom of your screen. Write 'RDP' or 'Remote Desktop Connection', paste the IP, and log in with the user details created in Azure. This provides you with access to a virtual Windows machine located in a different country.
<br />

<h2> Compare IP Addresses</h2>

![Image](https://github.com/user-attachments/assets/058fcd4e-1865-4422-8ea5-28aa2157f260)

<p>
To compare IP addresses and test a VPN, start by going to whatismyipaddress.com on your own computer and save the IP address and other details to a text file. Then, log into your Virtual Machine (VM) and do the same to record the VM’s details. Next, on the VM, download and install the ProtonVPN client, log in, and connect to a server in a third country (e.g., Japan). After connecting, visit whatismyipaddress.com again from the VM and save the new IP address and geolocation details.
</p>
<br />

<h2> Test a VPN on the VM</h2>

![Image](https://github.com/user-attachments/assets/43a42d7a-f470-4297-9c1e-87275bc42eb2)

<p>
Then visit sites like Google or Amazon to see if the language, URL, or content changes based on your new virtual location.
</p>
<br />
