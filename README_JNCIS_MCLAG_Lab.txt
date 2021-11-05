******** README - JUNIPER JNCIS MCLAG/VRRP LAB & CONFIGS ********

This series of configurations were configured for the JUNIPER JNCIS-ENT examination topics. These configurations should help the student understanding of the topic and provide an option to adjust the configuration values to understand traffic patterns. 

//// HARDAWARE | SOFTWARE SPECIFICATIONS \\\\

Vendor:: Juniper
Model:: vMX
OS Version:: Junos: 19.1R3.9

Virtualization Platform::
	> Application: EVE-NG COMMUNITY
	> Version: 2.0.3-112, QEMU 2.4.0
		System:    	Host: 		EVE-NG Kernel: 4.20.17-eve-ng-ukms+ x86_64 (64 bit) Console: tty 2 Distro: Ubuntu 16.04 xenial
					Machine:   	System: LENOVO product: 30B5005XUS v: ThinkStation P510 serial: MJ05Q450
					Mobo: 		LENOVO model: 102F Bios: LENOVO v: S00KT40A date: 05/04/2017
					CPU:       	Hexa core Intel Xeon E5-1650 v4 (-HT-MCP-) speed/max: 1809/4000 MHz
					Graphics:  	Card: NVIDIA GP106GL [Quadro P2000]
								Display Server: N/A driver: N/A tty size: 160x46 Advanced Data: N/A for root out of X
					Network:   	Card: Intel Ethernet Connection (2) I218-LM driver: e1000e
					Drives:    	HDD Total Size: 1024.2GB (4.4% used)
					Info:      	Processes: 270 Uptime: 4 days Memory: 7941.4/32058.8MB Init: systemd runlevel: 5
								Client: Shell (bash) inxi: 2.2.35 
								
This lab is based on a bare metal install of the EVE-NG Community Edition. It may be run within VMWare Workstation and other hypervisors. Resource utilization, on above server specifications, for this lab/system:

	CPU: 		28%
	MEM: 		26%
	SWAP: 		21%
	DISK ON /: 	5%
	
//// CODE REQUIREMENTS \\\\

To obtain the JUNOS code, you will need to create an account at HTTPS://WWW.JUNIPER.NET. Virtual code contains certain restrictions and is regulated by the vendor.
	
//// LAB DESCRIPTION \\\\

This lab focuses on basic layer-2 and layer-3 switching within a standard data center or MDF deployment. Many company's set up their data centers with MC-LAG, VRRP/HSRP, and SVIs on the spine/core of the data center. If you're studying or deploying MC-LAG and VRRP on a JUNIPER JUNOS MX device, this lab will give you a base to begin a deployment. You will need to customize this configuraiton for your environment and business needs if you deploy for a production network. If you are studying for the JNCx certification, this lab will provide a "standard" deployment where you may customize, destroy, and then spin up. It's good to get familiar with all the options.

Lab Requirements/Objectives:
	> Create active/passive MCLAG
	> Create active/active MCLAG
	> Create layer-2 segmentation
	> Create layer-3 segmentaiton
	> Create layer-3 redundancy for LAN connectivity
	> Verify configuration status of MCLAG and NHRP configurations
	> Test status by disabling interfaces
	

//// VENDOR GUIDES \\\\

https://support.juniper.net
https://https://learningportal.juniper.net
https://www.eve-ng.net/index.php/documentation/