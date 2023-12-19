<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04


<h2>Actions and Observations</h2>

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/ea73b1f9-0191-423b-a238-d203f5fc10e2)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/54aa5489-7415-4102-8469-6e62a1c5d567)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/be4e4abd-9eab-41ef-b89f-60a8d2b4984a)

**1.) First we will make a resource group inside Microsoft Azure and make a Virtual Machine that runs on Windows 10 and take note on the VNET we will be using the same VNET for the other VM.**

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/4c776bed-f66a-4627-bc94-db896b9a15d7)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/4fb6b544-cd40-4f13-9c46-feb506ae5d75)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/f48edcaf-802b-48b5-844e-12db3a6fa8c7)


**2.) Then proceed to make another VM but this time make sure it is Obuntu Server and in the same resource group as the first VM we created.**

**Then scroll down and click password as Authentication type and type any username and password *(I just put the same username and password as my first VM)* and Once your ready go to Networking and make sure that the VNET is the same as VM1s VNet and hit review and create.**


Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.






