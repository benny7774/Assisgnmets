# DHCP	

What is DHCP?

	Dynamic host configuration protocol simplifies and improves the accuracy of IP addressing but can raise security concerns. DHCP is a network server that automatically provides and assigns IP addresses, default gateways and other network parameters to client devices. It relies on the standard protocol known as Dynamic Host Configuration Protocol or DHCP to respond to broadcast queries by clients.

Components of DHCP

	When working with DHCP, it’s important to understand all of the components.  Below is a list of them and what they do:

		DHCP server: A networked device running the DCHP service that holds IP addresses and related configuration information. This is most typically a server or a router but could be anything that acts as a host, such as an SD-WAN appliance.

		DHCP client: The endpoint that receives configuration information from a DHCP server. This can be a computer, mobile device, IoT endpoint or anything else that requires connectivity to the network.  Most are configured to receive DHCP information by default.

		IP address pool: The range of addresses that are available to DHCP clients. Addresses are typically handed out sequentially from lowest to highest.

		Subnet: IP networks can be partitioned into segments known as subnets. Subnets help keep networks manageable.

		Lease: The length of time for which a DHCP client holds the IP address information. When a lease expires, the client must renew it.

		DHCP relay: A router or host that listens for client messages being broadcast on that network and then forwards them to a configured server. The server then sends responses back to the relay agent that passes them along to the client. This can be used to centralize DHCP servers instead of having a server on each subnet.

Benefits of DHCP servers

	In addition to simplified management, the use of a DHCP server provides other benefits.  These include:

		Accurate IP configuration: The IP address configuration parameters must be exact and when dealing with inputs such as “192.168.159.3”, it’s easy to make a mistake. Typographical errors are typically very difficult to troubleshoot and the use of a DHCP server minimizes that risk.

		Reduced IP address conflicts: Each connected device must have an IP address. However, each address can only be used once and a duplicate address will result in a conflict where one or both of the devices cannot be connected. This can happen when addresses are assigned manually, particularly when there are a large number of endpoints that only connect periodically, such as mobile devices.  The use of DHCP ensures that each address is only used once.

		Automation of IP address administration: Without DHCP, network administrators would need to assign and revoke addresses manually.  Keeping track of which device has what address can be an exercise in futility as it’s nearly impossible to understand when devices require access to the network and when they leave.  DHCP allows this to be automated and centralized so network professionals can manage all locations from a single location.

		Efficient change management: The use of DHCP makes it very simple to change addresses, scopes or endpoints. For example, an organization may want to change its IP addressing scheme from one range to another. The DHCP server is configured with the new information and the information will be propagated to the new endpoints. Similarly, if a network device is upgraded and replaced, no network configuration is required.

How does DHCP protocol work?

	 1.  Host connecting to network (cable or wireless) sends DHCP discover message to all hosts in Layer 2 segment (destination address is FF:FF:FF:FF:FF:FF). Frame with this DISCOVER message hits the DHCP Server.

	 2. After the DHCP Server receives discover message it suggests the IP addressing offering to the client host by unicast. This OFFER message contains:

		* proposed IP address for client (here 192.168.1.10)

		* subnet mask to identify the subnet space (here 255.255.255.0)

		* IP of default gateway for subnet (here 192.168.1.1)

		* IP of DNS server for name translations (here 8.8.8.8)

		* Options (read full article)

	3. Now after the client receives the offer it requests the information officially sending REQUEST message to server this time by unicast.

	4. Server sends ACKNOWLEDGE message confirming the DHCP lease to client. Now client is allowed to use new IP settings.


