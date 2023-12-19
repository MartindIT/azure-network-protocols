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

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/d217e1c7-de41-4e4f-91cb-763d0ec6cdb4)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/3d66730f-749b-42d4-a910-b6925c42d5d7)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/3831973c-d4ae-41c3-99c6-4002f32e8b79)

**3.) Once all your VM's are ready go to VM1 and copy and paste the Public IP address to Remote Desktop and connect with the username and password that you created. From there go to microsoft edge and download Wireshark**

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/c7875bd7-a1ff-47d6-a4ae-44f7be352d87)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/de678919-2887-4e79-973a-d33d2836ea0e)

**4.) After installation click finish and load wireshark and click on ethernet and then click on the shark fin where it says start capturing packets.**

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/e06c88e9-d1a4-4be7-af3f-c0a46966443c)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/9e7b083a-5c14-4e20-9fe6-c524ed2a2d5f)

**5.) Now this should show our actual live traffic thats happening in our VM, then to filter this traffic we can go on top and type "ICMP" where nothing shows beacuse this is the protocol that "Ping" which just test connectivity to different host on the network. So now that we see its empty we will try to ping VM2 and bring live traffic to ICMP.

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/2d5574d3-8e98-4953-a6a7-46337d111777)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/d54349fa-9121-401c-b4cc-4a7bdd3ea2ab)
![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/757830e6-7ca8-421e-833c-76e4b98a316c)

**6.) In order to ping VM2 we have to go back to Azure and figure out VM2s Private IP Address is and go back into VM1 Remote Desktop and load up Powershell and ping VM2 Private IP Address.**

***As soon as I hit enter ICMP traffic started to pop up beacuse ping was being used and ICMP reads Ping traffic.***

![image](https://github.com/MartindIT/azure-network-protocols/assets/151476834/a3b17a51-0607-457b-a206-2102e1657ba5)

**7.) Now that we know we have a connection between VM's I will make a Perpetual Ping to VM2 and have a never ending amount of ICMP traffic just so I can go into VM2 Firewall and Block ICMP traffic.** 







