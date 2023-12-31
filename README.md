<h1>Network Security Groups & Inspecting Network Protocols in Azure</h1>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark
- Powershell

<h2>Operating Systems Used </h2>

- Windows 10
- Ubuntu</b>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/kP1MMzN.png" height="80%" width="80%" alt="Topology"/>
</p>
<p>
Diagram of entire process
</p>
<br />

<p>
<img src="https://i.imgur.com/LvqwQAB.png" height="80%" width="80%" alt="2 vm"/>
</p>
<p>
Create 2 virtual machine inside the Resource Group; one is Windows and the other is Ubuntu
</p>
<br />

<p>
<img src="https://i.imgur.com/KgvLtCw.png" height="80%" width="80%" alt="rdc"/>
</p>
<p>
Remote Desktop Connection to the VM1 public IP Address
</p>
<br />

<p>
<img src="https://i.imgur.com/OHQ1B65.jpg" height="80%" width="80%" alt="Download Wireshark"/>
</p>
<p>
Download Wireshark inside the virtual machine
</p>
<br />

<p>
<img src="https://i.imgur.com/gjlwxEo.jpg" height="80%" width="80%" alt="Use Ping"/>
<img src="https://i.imgur.com/mdfsOYp.png" height="80%" width="80%" alt="Use Ping"/>
<img src="https://i.imgur.com/W094nVH.jpg" height="80%" width="80%" alt="Use Ping"/>
</p>
<p>
Use the ICMP protocol as the filter to observe the traffic. Open Windows Powershell then use "ping 10.0.0.5" and "ping www.google.com". Next go to VM2's network security group and create an inbound security rule to deny ICMP traffic. These commands will show how much data is being sent and received.
</p>
<br />

<p>
<img src="https://i.imgur.com/CyRmSTz.jpg" height="80%" width="80%" alt="SSH"/>
</p>
<p>
Use SSH to filter the traffic. In Powershell, use SSH to remotely connect to VM2 by typing "ssh labuser@10.0.0.5". Next type "pwd", "id", and "ls -lasth". Observe the traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/JF6RkKG.jpg" height="80%" width="80%" alt="DHCP"/>
</p>
<p>
Use DHCP to filter the traffic. In Powershell, type "ipconfig /renew" then observe the traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/f06KkBn.jpg" height="80%" width="80%" alt="DNS"/>
</p>
<p>
Use DNS to filter the traffic. In Powershell, type "nslookup www.google.com" and "nslookup www.disney.com" to find the IP Address for both website and observe the traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/KqAPmcB.jpg" height="80%" width="80%" alt="RDP"/>
</p>
<p>
In order to use RDP in the filter; you type in "tcp.port == 3389". Since RDP was selected as the protocol for VM1 when it was created; the rdp filter will spam nonstop. Every movement or words being typed inside the virtual machine will cause traffic to be sent.
</p>
<br />
