<h1>Failed RDP to IP Geolocation Information</h1>

<h2>Description</h2>
<b>The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third party API to collect geographic information about the attackers location.
</b>
<br />
<br />
The script is used in this demo where I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to
look up the attackers Geolocation information and plot it on an Azure Sentinel Map!
<br />
<br />

<h4> Logical Diagram: 
<br/>
<br/>
<p align="center">
<img src="https://github.com/dgftjr/Sentinel_Lab/blob/main/Honeypot_LogicalDiagram_treco.jpg" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>

<h4> Geolocate the Failed Log-In Attempts: 
<br/>
<br/>
<p align="center">
<img src="https://github.com/dgftjr/Sentinel_Lab/blob/main/FailedLogIn_geolocate.jpg" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>
- <b>Microsoft Azure Sentinel, Azure Virtual Machine:</b> To Initiate Honeypot for Attacks </br>
- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from Russia coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://github.com/dgftjr/Sentinel_Lab/blob/main/FailedLogins_fromRussia_Treco.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://github.com/dgftjr/Sentinel_Lab/blob/main/AttackMap_24hr.jpg" height="75%" width="75%" alt="Image Analysis Dataflow"/>
</p>
