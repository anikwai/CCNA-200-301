# Explain the roles and functions of a layer 2 and 3 switch?

In a network, L2 Switch makes forwarding decisions based on the destination MAC address in the layer 2 header. 

Ethernet network devices learn the layer 2 addresses of other devices on the same network.  
Hosts and endpoints (such as clients and servers) need to learn the layer 2 addresses of other local devices to send frames to those devices. 
A layer 2 switch learns about layer 2 addresses to build a MAC address table. 
The MAC address table on the switch allows that switch to correctly perform layer 2 forwarding of frames between devices in the same network.

Clients, servers, and other endpoints on an IPv4 network can dynamically learn the layer 2 address of other devices on the same network by using Address Resolution Protocol (ARP).

A Cisco IOS router also uses ARP to discover the layer 2 addresses of other devices on the same network. However, the commands to see the arp cache are slightly different than on a Windows or Linux computer.

