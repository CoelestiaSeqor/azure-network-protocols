<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

1. Design and Planning
2. Azure Virtual Network (VNet) Setup
3. Azure Virtual Machine Deployment
4. AD DS Installation and Configuration
5. Additional Domain Controllers
6. Networking and DNS Configuration
7. Connectivity between On-Premises and Azure
8. Security and Access Control
9. Monitoring and Maintenance

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Part 1: Create our Resources
---------------------------
1. Create a Resource Group.
2. Create a Windows 10 Virtual Machine (VM) in the previously created Resource Group, allowing it to create a new Virtual Network (Vnet) and Subnet.
3. Create a Linux (Ubuntu) VM in the same Resource Group and Vnet as the Windows 10 VM.
4. Observe your Virtual Network within Network Watcher.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Part 2: Observe ICMP Traffic
---------------------------
1. Use Remote Desktop to connect to your Windows 10 VM.
2. Install Wireshark within your Windows 10 VM.
3. Open Wireshark and filter for ICMP traffic only.
4. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM.
5. Observe ping requests and replies within Wireshark.
6. From the Windows 10 VM, open the command line or PowerShell and attempt to ping a public website (e.g., www.google.com) and observe the traffic in Wireshark.
7. Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM.
8. Open the Network Security Group of your Ubuntu VM and disable incoming (inbound) ICMP traffic.
9. Observe the ICMP traffic in Wireshark and the command line Ping activity from the Windows 10 VM.
10. Re-enable ICMP traffic for the Network Security Group of your Ubuntu VM.
11. Observe the ICMP traffic in Wireshark and the command line Ping activity (should start working).
12. Stop the ping activity.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


Part 3: Observe SSH Traffic
---------------------------
1. Filter Wireshark for SSH traffic only.
2. From your Windows 10 VM, "SSH into" your Ubuntu VM using its private IP address.
3. Type commands (username, password, etc.) into the SSH connection and observe the SSH traffic in Wireshark.
4. Exit the SSH connection by typing 'exit' and pressing [Enter].

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Part 4: Observe DHCP Traffic
---------------------------
1. Filter Wireshark for DHCP traffic only.
2. From your Windows 10 VM, attempt to issue a new IP address to the VM from the command line (e.g., ipconfig /renew).
3. Observe the DHCP traffic appearing in Wireshark.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Part 5: Observe DNS Traffic
---------------------------
1. Filter Wireshark for DNS traffic only.
2. From your Windows 10 VM's command line, use nslookup to see the IP addresses of www.google.com and disney.com.
3. Observe the DNS traffic shown in Wireshark.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Part 6: Observe RDP Traffic
---------------------------
1. Filter Wireshark for RDP traffic only (tcp.port == 3389).
2. Observe the constant stream of traffic. The RDP protocol continuously transmits data between the computers, resulting in non-stop traffic.
