<h1>Geomapping Failed RDP Attacks</h1>


<h2>Description</h2>
<b>  We will be utilizing a Powershell script, which can be found in this repository, to parse out the Windows Event Log information for failed RDP attacks. We will also be utilizing a third-party API to collect the geographic data such as the latitude, longitide, and country of the attackers.  
</b>
<br />
<br />
 
A live virtual machine is set up to act as a honey pot and is connected to Azure Sentinel (SIEM) while the PowerShell script is being run. In this lab, we will be observing live attacks, such as RDP Brute Force, from all around the world. The PowerShell script will then provide us with the Geolocation information with the help of the API and map the coordinates on Azure Sentinel Map.  
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/b3WQTJ8.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from France coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/XXYqSTB.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 5 hours (built custom logs including geodata)</h2>

<h2>Description</h2>
<b>After leaving the lab running for around five hours, I realized there were a large number of attacks coming from one specific area. It appeared as though an RDP Brute Force Attack was coming from France. Unfortunately, the free API we were utilizing had a restriction of 1000 requests, which made it difficult for us to run the system for long periods of time while collecting data. If we left the honey pot running, countless more attacks from all over the world would undoubtedly be launched against it. This can definitely be a key takeaway from this lab, that no matter who you are or what information you own, your devices that are not completely protected will always be a target. 
</b>
<p align="center">
<img src="https://i.imgur.com/uTMrsKa.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
