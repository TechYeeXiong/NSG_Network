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
<img src="https://i.imgur.com/W094nVH.jpg" height="80%" width="80%" alt="Use Ping"/>
</p>
<p>
Use the ICMP protocol as the filter to observe the traffic. Open Windows Powershell and use "ping 10.0.0.5", "ping www.google.com", and "ping 10.0.0.5 -t". These commands will show how much data is being sent and received.
</p>
<br />

<p>
<img src="https://i.imgur.com/LNeqMT0.jpg" height="80%" width="80%" alt="Download ProtonVPN into Windows"/>
</p>
<p>
Choose the windows download.
</p>
<br />

<p>
<img src="https://i.imgur.com/P8plfWA.jpg" height="80%" width="80%" alt="Connect To An Open Free VPN Server"/>
</p>
<p>
Connect to Japan.
</p>
<br />

<p>
<img src="https://i.imgur.com/lFkECUi.jpg" height="80%" width="80%" alt="Go onto whatismyipaddress.com"/>
</p>
<p>
The IP Address is now located in Tokyo.
</p>
<br />

<p>
<img src="https://i.imgur.com/tPGCmMt.jpg" height="80%" width="80%" alt="Go to google and observe the changes"/>
</p>
<p>
Since VPN is used in a Japan server; Google changed.
</p>
<br />

<p>
<img src="https://i.imgur.com/QGIXapN.jpg" height="80%" width="80%" alt="Look at Netflix's URL"/>
</p>
<p>
The ending of the URL is now "jp-en/".
</p>
<br />
