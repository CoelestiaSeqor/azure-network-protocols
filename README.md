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

1. Set up an Azure subscription: If you don't already have an Azure subscription, sign up for one at https://azure.microsoft.com/ and create a new account.

2. Create Azure Virtual Machines (VMs): Deploy one or more Azure VMs that you'll use to observe network traffic. Ensure that the VMs are running and properly configured.

3. Install and configure Wireshark: Wireshark is a network protocol analyzer that allows you to capture and analyze network traffic. Install Wireshark on your local machine or on a separate VM.

4. Capture network traffic: Launch Wireshark on your local machine or the VM where it's installed. Select the network interface that is connected to the same network as your Azure VMs. Start capturing network traffic.

5. Filter traffic for Azure VMs: Apply filters in Wireshark to only capture traffic related to your Azure VMs. You can use filters based on IP addresses, ports, or other criteria to narrow down the captured traffic.

6. Analyze the captured traffic: Review the captured packets in Wireshark to observe the network traffic to and from your Azure VMs. You can analyze protocols, source and destination IP addresses, ports, and any other relevant information.

7. Experiment with Network Security Groups (NSGs): Network Security Groups are an Azure networking feature that allows you to control traffic flow and implement security rules. In the Azure portal, navigate to the NSG settings for your Azure VMs.

8. Create and modify NSG rules: Experiment with creating and modifying NSG rules to control inbound and outbound traffic to your Azure VMs. You can define rules based on source IP addresses, ports, protocols, and other parameters.

9. Observe the effects of NSG rules: After applying NSG rules, monitor the network traffic using Wireshark. Observe how the rules affect the flow of packets, which packets are allowed or blocked, and any other changes in the network behavior.

10. Evaluate network security: Analyze the effectiveness of the NSG rules in enhancing network security. Consider factors such as the ability to block unwanted traffic, protect sensitive services, and enforce access control.

11. Document your findings: Take notes during the tutorial and document your observations, configurations, and any insights gained from analyzing the network traffic and experimenting with NSG rules.

12. Conclusion and further learning: Conclude the tutorial by summarizing your findings and highlighting any areas for further exploration or learning related to network traffic analysis and network security in Azure.

Remember to refer to official Azure documentation or additional resources for detailed instructions on specific steps and concepts.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
