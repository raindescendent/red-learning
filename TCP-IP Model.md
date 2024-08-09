***TCP/IP Model overview from OSI Model***
**Also knows as DoD (Department of Defense) Model 4 Layers (high to low level)**

***TCP/IP Protocol Suite***
**Transmission Control Protocol**
**Internet Protocol***

It provides all the necessary services to connect all type of devices in a network.  

1.  Network Access Layer (2-on-1) 
[OSI: Physical Layer] 
"Function as interpreter of the Physical addressing where is translated to Logical Addressing"
        - Protocol Data Unit: Bits or Data Stream
        - Protocols: Electrons, Radio Frequency or Light.
2.    Network Access Layer (2-on-1)
[OSI: Data-Link Layer]
        - Protocol Data Unit: Frame 
        - Protocols: Ethernet, L2TP (Layer 2 Tunneling Protocol), NDP (Neighbor Discovery Protocol), PPP (Point-to-Point), Frame Relay, MAC Address, ARP.
3.  Internet Layer 
[OSI: Network Layer]
"Defines the Logical addressing scheme of each device connected to the network and the Physical addressing too. Also it provides a Routing service for the entire information of the communication between origin and destiny node"
        - PDU: Packets
        - Protocols: IP, IPSEC, ARP (Address Resolution Protocol), IGMP, ICMP
4.  Host-to-Host Layer
[OSI: Transport Layer]
"It provides the connnectivity through the entire network. Also it manages the roles of the sender and receiver dinamically"
-    PDU: Segments
-    Protocols
-        TCP
-        DCCP
-        μTP
-        UDP
-        ICMP
-        FCP

5.  Application Layer 
[OSI: Session, Presentation & Application Layers]
"This layer manage all the funcionalities required by the apps and services which have a directly relationship with the user"
-    PDU: Data
-    Protocols and Ports 
-        HTTP: 80 
-        HTTPS/TLS/SSL: 443
-        NNTP: 119 
-        FTP: 21, 20
-        Telnet: 23
-        SSH: 22
-        POP3: 110
-        IMAP4: 143
-        SMTP: 25 
-        DNS: 53
-        TFTP: 69
-        DHCP/BootP: 67, 68
-        SNMP: 162, 161
-        NTP: 123
-        Syslog: 514
-        RIP       