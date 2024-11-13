**IP - Internet Protocol**

*Non-connection oriented* protocol it transfers switched packets through differents linkeds physical networks in bidirectional direction on origin or destination. It works on Network Layer (OSI) or Layer 3 (TCP/IP). 

A protocol *Non-connection oriented* establishes a directly communication between 2 final points of the network where the message can be sent without previously permission or 'handshake'. 

The packets will be split through different routes an finally assembled at the destination. 

This protocol doesn't have contact with the destination before send the packet. 

- Header 
-    Contains the IP addresess of the origin/destination devices, Routers will use this information for trace the transfer section of the network for send the packets"
-    IP doesn't provide any tool or mechanism to check if the packet finally is on destination (or not). 
-    IP provide checksums only for the header of the packet, not for the data. Instead, TCP protocol provides reliability. TCP works on Layer 4 (TCP/IP) or Transport Layer (OSI). 

**Addressing**
Defined as a 'label' for each device or element in the network. 
Inside a network it's necessary identify all the devices for the communiaction between them or external resources.

*IP Addressing* 
A number which identifies (logical and hierarchical mode) a interface of a device inside a network which use Internet Protocol. 
Each assigned IP is unique for any device. It can't exist 2 same IP's. 

**Routing**
Defined as "learn" how to find a device or a "IP" inside the network. 

*Routing table*
A data structure that allows the storage and access of necessary data regarding routes leading to designated IP destinations. 
It contains all routed networks or "learned", this happens through different protocols (BGP, EIGRP, IGRP, RIP, static routes, etc.)

**Netmask**
A set of bits, useful for limit the ambit of a computers network. 
Used to divide an IP address into subnets and specify the network's available hosts. 

**Gateway**
Acting as a connection interface between 2 networks with different transmission protocols. Translates the data of the origin protocol for the final destination network and its protocol. 
It can be modified using a DHCP server. 

**Loopback**
Is the routing of electronic signals or digital data streams back to their source (origin) without intentional processing or modification.
A certain range of IP's are reserved for Loopback address from 127.0.0.0 to 127.255.255.255.


------------------------------------------------------------

- Private IP address is used to connect securely to other devices in a same network, there are not routed to the Internet. This range of addresses is here to be used in a LAN.


- Public IP address identifies a device to the wider Internet.

ICANN (Internet Corporation for Assigned Names and Numbers) provides to us a 3 differents 'classes' of public IP Addresses for organizations.
A, B & C.   

- Class: A 
- Public IP Range: 0.0.0.0 > 127.255.255.255 
- Networks: 128
- Hosts: 16.777.214
- Big Networks
- Reserved Addresses: 127.0.0.0
- Private IP Range: 10.0.0.0

- Class: B 
- Public IP Range: 128.0.0.0 > 191.255.255.255
- Networks: 16.384
- Hosts: 65.534
- Mid Networks
- Reserved Addresses: 128.0.0.0, 191.255.0.0
- Private IP Range: 172.16.0.0 > 172.31.0.0

- Class: C
- Public IP Range: 192.0.0.0 > 223.255.255.255
- Networks: 2.097.152
- Hosts: 254 
- Small Networks
- Reserved Addresses: 192.0.0.0
- Private IP Range: 192.168.0.0 > 192.168.255.0

- Class: D (Reserved)
- IP Range: 224.0.0.0 > 239.255.255.255
- Multicast (Send the same data at the same time to different devices in a network)
- Reserved Addresses: 224.0.0.0

- Class: E (Reserved)
- IP Range: 240.0.0.0 > 255.255.255.255
- Research (Individual testing purposes)


------------------------------------------------------------


**IPv4**

IPv4 Addresess are interpreted as a 32-bits number (integer). 
- Max. Addresess: 4.294.967.296

Each IP is expressed as decimal integer, dividing the 32-bits in 4 (fourth) octals (8 bits). 

[IPv4 Address]
172.16.254.1

[Same IPv4 in binary octals]
10101100.00010000.11111110.00000001
- Each (8 bits per octal) is equivalent to 1 byte. 

[Converting Binary Octal to Decimal]
IPv4: 10101100.00010000.11111110.00000001
- The octal has a decimal value between 0 > 255
- The higher number in 8-bits binary is 11111111
- Each bit has a sequenced value from right to left 
-    1, 2, 4, 8, 16, 32, 64, 128 (The sum of this numbers = 255)

"Each IP is expressed as decimal integer, dividing the 32-bits in 4 octals."

[IPv4 Address]
172.16.254.1

1.  1   0   1   0   1   1   0   0 (Binary)
    128 64  32  16  8   4   2   1 (Decimal - 128 + 32 + 8 + 4 = 172)

2.  0   0   0   1   0   0   0   0 (Binary)
    128 64  32  16  8   4   2   1 (Decimal = 16)

3.  1   1   1   1   1   1   1   0 (Binary)
    128 64  32  16  8   4   2   1 (Decimal - 128 + 64 + 32 + 16 + 8 + 4 + 2 = 254)

4.  0   0   0   0   0   0   0   1 (Binary)
    128 64  32  16  8   4   2   1 (Decimal = 1)
