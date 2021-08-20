# Networking Overview

	A network enables two computers to communicate with each other. There is array of topologies (mesh/tree/star), mediums (ethernet/fiber/coax/wireless) and protocols (TCP/UDP/IPX) that can be used to facilitate the network.

# Network Types

	Each network is structured differently and can be set up individually. For this reason so called types and topologies have been developed that can be used to categories these networks. 


#Common Terminology

Network type 				Definition

Wide Area Network (WAN)			Internet

Local Area Network (LAN) 		Internal Networks (Eg: Home or Office)

Wireless Local Area Network (WLAN)	Internal Networks accessible over Wi-Fi

Virtual Private Network (VPN)		Connects multiple network network sites to one LAN

WAN

	The WAN is commonly referred to as The Internet. A WAN is just a large number of LANs joined together. Many large companies or government agencies will have an "Internal WAN" ( also called Intranet, Airgap Network, etc.,).

LAN/WLAN

	LANs and  WLANs will typically assign IP Addresses designated for local use. There's nothing difference between a LAN or WLAN, other than WLAN's introduce the ability to transmit data without cables. It is mainly a security designation.

VPN

	There are three main types Virtual Private Networks (VPN), but all three have the same goal of making the user feel as if they were plugged into a different network.

		* Site-To-Site VPN - Both the client and server are Network Devices, typically either Routers or Firewalls and share entire neytwork ranges

		* Remote Access VPN - The involves the client's computer creating a virtual interface that behaves as if it is on a client's network.

		* SSL VPN - This is essentially a VPN that is done within our web browser and is becoming increasingly common as web browsers are becoming capable of doing anything.

Book Terms

Network Type 				Definition

Global Area Network (GAN)		Global network (the internet)

Metropolitan Area Network (MAN) 	Regional network (multiple LANs)

Wireless Personal Area Network (WPAN)   Personal network (Bluetooth)


Networking Topologies 

	A network topology is a typical arrangement and physical or logical connection of device in a network. Computers are hosts such as client and servers, that actively use the network. They also include network components such as switches, bridges and routers.

1. Connections

Wired Connections					Wireless connections

Coaxial Cabling						Wi-Fi

Glass fiber cabling					Cellular

Twisted-pair cabling					Satellite

2. Nodes - Network Interface Controller (NICs)

Repeaters		Hubs		Bridges			Switches

Router/Modem		Gateways	Firewalls

3. Classification

We can imagine a topology as a virtual form or structure of a network. This form does not necessarily correspond to the actual physical arrangement of the devices in the network. Therefore these topologies can be either physical or logical.

Point to Point					Bus

Star						Ring

Mesh						Tree

Hybrid						Daisy Chain

# Proxies

Many people have different opinions on what a proxy is

* Security Professionals jump to HTTP Proxies ( BurpSuite) or pivotingwith a SOCKS/SSH Proxy( Chisel, ptunnel, sshuttle).

* Web Developers use proxies like Cloudflare or ModSecurity to block malicious traffic.

* Sysadmins probably think web application filters to prevent users from going to malicious or inappropriate websities.

* Average people may think a proxy is used to obfuscate your location and access another country's Netflix catalog.

* Law Enforcement often attributes proxies to illegal activity.

Proxies will almost always operate at Layer 7 of the OSI Model.There are many types of proxy services

	* Dedicated Proxy/ Forward Proxy

	* Reverse Proxy

	* Transparent Proxy

# Networking Models

	Two networking models describe the communication and transfer of data from one host to another called ISO/OSI model and the TCP/IP model.


The OSI Model							The TCP/IP Model

Application FTP,HTTP						Application

Presentation JPG,PNG,SSL,TLS

Session NetBIOS

Transport TCP, UDP						Transport

Network Router, L3 Switch					Internet

Data-Link Switch, Bridge					Link

Physical Network Card 

OSI Model

	The OSI model, often referred to as ISO/OSI layer models, is areference model that can be used to describe and define the communication between systems. The reference model has seven individual layers, each with clearly separated tasks.

TCP/IP Model

	TCP/IP is a generic term for many network protocols. The protocols are responsible for the switching and transport of data packets on the internet.

ISO/OSI vs TCP/IP

	TCP/IP is a communication protocol that allows hosts to connect to the internet. It refers to the Transmission Control Protocol used in and by application on the internety.

	OSI, on the other hand, is a communication gateway between the network and end-users.

Packet Transfers

	In layered system, devices in a layer exchange data in a different format called a protocol data unit (PDU).


		OSI Layer				TCP/IP				PDU

		Application FTP, HTTP  			Application			DATA

		Presentation JPG, PNG, SSL, TLS		Application			DATA

		Session NetBIOS				Application			DATA

		Transport TCP, UDP			Transport			Segment/Datagram

		Network Router, L3 Switch		Internet			Packet

		Data-Link Switch, Bridge		Link				Frame

		Physical Network Card			Link				Bit

# Network Layer

	The Network layer ( Layer 3) of OSI controls the exchange of data packets, as these cannot be directly routed to the receiver and therefore have to be provided with routing nodes. Tne data packets are then transferred from node to node until they reach their target.

	* Logical Addressing

	* Routing

	Protocols are defined in each layer of OSI, and these protocols represent a collection of rules for communication in the respective layer. They are transparent to the protocols of the layers above or below. Some protocols fulfill tasks of several layers and extend over two or more layers. The most used protocols on this layer are:

		* IPv4 / IPv6
		
		* IPsec
		
		* ICMP
	
		* IGMP
		
		* RIP
		
		* OSPF

# IP Addresses
	Each host in the network located can be identified by the so-called Media Access Control address (MAC). This would allow data exchange within this one network. If the remote host is located in another network, knowledge of the MAC address is not enough to establish a connection. Addressing on the Internet is done via the IPv4 and/or IPv6 address, which is made up of the network address and the host address.

		* IPv4 / IPv6 - describes the unique postal address and district of the receiver's building.
		
		* MAC - describes the exact floor and apartment of the receiver.

# Subnetting
	The division of an address range of IPv4 addresses into several smaller address ranges is called subnetting.

	A subnet is a logical segment of a network that uses IP addresses with the same network address. We can think of a subnet as a labeled entrance on a large building corridor. For example, this could be a glass door that separates various departments of a company building. With the help of subnetting, we can create a specific subnet by ourselves or find out the following outline of the respective network:

		* Network address

		* Broadcast address

		* First host

		* Last host

		* Number of hosts

# MAC Addresses

	Each host in a network has its own 48-bit (6 octets) Media Access Control (MAC) address, represented in hexadecimal format. MAC is the physical address for our network interfaces. There are several different standards for the MAC address:

		* Ethernet (IEEE 802.3)

		* Bluetooth (IEEE 802.15)

		* WLAN (IEEE 802.11)

	MAC address:

		DE:AD:BE:EF:13:37
		DE-AD-BE-EF-13-37
		DEAD.BEEF.1337

# IPv6 Addresses
	IPv6 is the successor of IPv4. In contrast to IPv4, the IPv6 address is 128 bit long. The so-called prefix is used to identify the host and network parts. The Internet Assigned Numbers Authority (IANA) is responsible for assigning IPv4 and IPv6 addresses and their associated network portions. In the long term, IPv6 is expected to completely replace IPv4, which is currently still predominantly used on the Internet. In principle, however, IPv4 and IPv6 can be made available simultaneously (Dual Stack).

		* Larger address space
		* Adress self-configuration (SLAAC)
		* Multiple IPv6 addresses per interface
		* Faster routing
		* End-to-end encryption (IPsec)
		* Data packages up to 4 GByte

There are four different types of IPv6 addresses:

		Type					Description
		Unicast				Addresses for a single interface.
		Anycast				Addresses for multiple interfaces, where only one of them receives the packet.
		Multicast			Addresses for multiple interfaces, where all of them receive the same packet.
		Broadcast			Do not exist and is realized with multicast addresses.


	

