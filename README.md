<h1>******** README ********<br>
******** JUNIPER JNCIS MCLAG/VRRP LAB &amp; CONFIGS ********</h1>

This series of configurations were configured for the JUNIPER JNCIS-ENT examination topics. These configurations should help the student understanding of the topic and provide an option to adjust the configuration values to understand traffic patterns. 

<b>//// HARDWARE | SOFTWARE SPECIFICATIONS \\\\</b><p>
<i>Virtualized Network Devices:</i>
<blockquote>
Vendor:: Juniper<br>
Model:: vMX<br>
OS Version:: Junos: 19.1R3.9<br>
Virtualization Platform::<br>
Application: EVE-NG COMMUNITY<br>
Version: 2.0.3-112, QEMU 2.4.0<br>
</blockquote>
<p>
<i>System Hardware/Environment:</i>
<blockquote>
Host:	EVE-NG Kernel: 4.20.17-eve-ng-ukms+ x86_64 (64 bit) Console: tty 2 Distro: Ubuntu 16.04 xenial<br>
<b>Machine Details:</b><br>
System: 	LENOVO product: 30B5005XUS v: ThinkStation P510<br>
Mobo: 		LENOVO model: 102F Bios: LENOVO v: S00KT40A date: 05/04/2017<br>
CPU:       	Hexa core Intel Xeon E5-1650 v4 (-HT-MCP-) speed/max: 1809/4000 MHz<br>
Graphics:  	Card: NVIDIA GP106GL [Quadro P2000], Display Server: N/A driver: N/A tty size: 160x46 Advanced Data: N/A for root out of X<br>
Network:   	Card: Intel Ethernet Connection (2) I218-LM driver: e1000e<br>
Drives:    	HDD Total Size: 1024.2GB<br>
</blockquote>
<p>								
This lab is based on a bare metal install of the EVE-NG Community Edition. It may be run within VMWare Workstation and other hypervisors. Resource utilization, on above server specifications, for this lab/system:<p>
<blockquote>
	CPU: 		28%
	MEM: 		26%
	SWAP: 		21%
	DISK ON /: 	5%
</blockquote>
<p>
<b>//// CODE REQUIREMENTS \\\\</b>

To obtain the JUNOS code, you will need to create an account at HTTPS://WWW.JUNIPER.NET. Virtual code contains certain restrictions and is regulated by the vendor.
<p>
<b>//// LAB DESCRIPTION \\\\</b><p>
This lab focuses on basic layer-2 and layer-3 switching within a standard data center or MDF deployment. Many company's set up their data centers with MC-LAG, VRRP/HSRP, and SVIs on the spine/core of the data center. If you're studying or deploying MC-LAG and VRRP on a JUNIPER JUNOS MX device, this lab will give you a base to begin a deployment. You will need to customize this configuraiton for your environment and business needs if you deploy for a production network. If you are studying for the JNCx certification, this lab will provide a "standard" deployment where you may customize, destroy, and then spin up. It's good to get familiar with all the options.
<p>
<i>Lab Requirements/Objectives:</i>
<ul>
	<li>Create active/passive MCLAG</li>
	<li>Create active/active MCLAG</li>
	<li>Create layer-2 segmentation</li>
	<li>Create layer-3 segmentaiton</li>
	<li>Create layer-3 redundancy for LAN connectivity</li>
	<li>Verify configuration status of MCLAG and NHRP configurations</li>
	<li>Test status by disabling interfaces</li>
</ul>
<p>
<i>Lab Details:</i>
<p>
<b><i>Management interfaces:</b></i>
<blockquote>
<ul>
	<li>CSR1/VCP1: 192.168.21.101</li>
	<li>CSR2/VCP2: 192.168.21.102</li>
	<li>CSR3/VCP3: 192.168.21.103</li>
	<li>CSR4/VCP4: 192.168.21.104</li>
</ul>
</blockquote><p>
<b><i>Lab User Accounts (username / password)</b></i>
  <ul>
    <li>root / abc123</li>
    <li>admin / abc123</li>
  </ul><p>

<b>//// VENDOR GUIDES \\\\</b><br>
https://support.juniper.net<br>
https://learningportal.juniper.net<br>
https://www.eve-ng.net/index.php/documentation/<br>

<b>//// LAB IMAGE \\\\</b>

![image](https://user-images.githubusercontent.com/40407552/140561994-156b3bb4-d6ed-457b-986f-395d2a2225af.png)

