
**ifconfig** 
*Network & Subnets Data*

"IP Address, MAC Address (ether, hwaddress), Netmask, Broadcast Address, Loopback Address (localhost), MTU (Maximum Transmission Unit)." 

IP Address: 

32-bits unique number which represent the host in the network or subnet.


Netmask:

32-bit binary mask that divides an IP address into subnets. It is also used to determine the class (A, B & C) and range of IP addresses.


MAC Address: 

48-bits unique number which serve as identifier assigned to each Network Interface Controller (NIC) & Network Devices. It's also called 'physical address'. 


Broadcast Address: 

Special IP Address reserved for a multipoint connection reaching all the hosts in the network without knowing the recipient addresses. 


Loopback: 

Virtual network interface that the host uses to communicate with 'itself'. It is used for diagnostics and troubleshooting, and using the servers running on the local machine.

MTU: 

Maximum Transmission Unit defines the maximum size in bytes of the 'largest' data packet which is transmitted or received through the network.

>> Permite modificar manualmente IP, MAC, Netmask, Broadcast Address

-IP / Netmask / Broadcast Address-
> ifconfig eth0 'newIpNumber' netmask 'newNetAddress' broadcast 'newBroadcastAddress'

-MAC (HWaddress) Spoofing- 
> ifconfig eth0 down
> ifconfig eth0 hw ether 'newMAC'
> ifconfig eth0 up 


DHCP (Dynamic Host Configuration Protocol)

> Runs a 'daemon' (proccess running on background) called 'dhcpd' (DHCP Daemon)
Encargado de asignar direcciones IP para cada sistema en la red y subred. Manteniendo un LOG File de que direccion (IP) fue asignada cada dispositivo especificamente. 
En conexion LAN, es necesaria la asignacion de DHCP

-Solicitud al servidor DHCP para NUEVA asignacion IP- 
> dhclient eth0 



DNS (Domain Name System)
> Traductor de nombre del dominio (google.com) a direccion IP (192.x.x.1).

-Manipulando DNS: dig - (IP DNS Server, Server Name, Email Server, Subdomains)
> dig google.com 
> dig google.com ns
> dig google.com mx


In Linux the DNS is called BIND too.


-Cambiar servidor DNS- 

> leafpad /etc/resolv.conf (nameserver 8.8.8.8)
> echo "nameserver 8.8.8.8"> /etc/resolv.conf



Managing my own IP Addresses 
>> En el sistema linux existe un archivo llamado 'hosts' (/etc/hosts), hosts actua como DNS local. Mapeando el hostname (google.com) a una direccion IP asignada por DHCP o Manual (192.168.181.131)

-Cambiar archivo hosts y manipular ip-

> leafpad /etc/hosts (IP    hostname)
    127.0.0.1	localhost
    127.0.1.1	kali
    192.168.181.131	bankofamerica.com



