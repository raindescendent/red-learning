**Hardware**

*Devices*
- Firewall
- IDS
- IPS 
- NIDS
- HIDS

*Appliances & Tools on Routers, Hubs and Switches*
- ACL (access-list)



1.  *Firewall*
-    Device or Software which blocks the access into the network (outside too) through 'rules' or 'politics'. 
-    It compares all the traffic with the permission logic. 
-    Restrictive: Any not allowed traffic, it will be rejected.
-    Permissive: Any not blocked traffic, it will be accepted. 
-    *Dual-Homed*: Works with 2 interfaces, one for each type of networks (private, public)
-    *Multi-Homed*: Works with many devices allowing the possibility of 'modify' differents networks with differents rules and politics for each one.

-   *Firewall Services*
-    Packet Filtering
-    Application Layer (Layer's analysis)
-    Stateful (Session logging history)


2.  *DMZ* 
-    DMZ network (sometimes referred to as a “demilitarized zone”) functions as a subnetwork containing an organization's exposed, outward-facing services (generally Internet). (DNS, SMTP, etc.)


3. *IDS* (Intrusion Detection System)
-    It controls the network traffic through a packet analysis. Detects anomalys in them or signatures. 

-    Signature-based detection it works comparing the packet signature information with the already admin determineds offensive signatures.
-    Heuristic-based detection it works reading the "normals" values of activity in the network (used bandwith, protocols, devices, etc.) if detects some anomaly change it reports to the admin. It comes with a database of already know offensive signatures.


-    It re-setup a external security device (Packet filter or Firewall) through a command (N-IDS). When the device send the data also send the alert in the *header* packet. 

-    Establishes a SNMP trap for a external hipervisor (intruder) in a datagram format. 

-    Sends an email to the users or admins of the IDS alerting of a serious-intrude. 

-    Saves Attack logs in a db including:
-        Intruder IP
-        Destination IP
-        Used Protocol to attack
-        Payload

-    Saves the origin suspicious packets. 

-    Permits the openning of differents applications.

-    Notification of attack alert to the admins in console.


- *NIDS*: Hardware or software based, works on a delimited segment of the network. Warranting the entire network security.
- *HIDS*: Software based, works on the device to protect specifically on the O.S. Warranting the security of the host. 
-         Read registrys
-         Packet capture and detection: Trojans, Malicious Code, Buffer overflow, non-authorizeds access attempts. 


4. *IPS* (Intrusion Prevention System)

- It does the analisys for the entire in/out traffic. 
- Signature-based detection
- Rule-based detection 
- Anomaly-based detection: Profiles of "normally" traffic is defined by the admin. All the traffic which not match with the profile pattern it will be captured. 
-    Statistic-anomaly-based detection: The device analyzes dinamically the entire traffic of the network for a certain time creating the "normal" base line and sending an alarm when packets are too different. 


5. *Honeypots* 

A flexible system which is used to attract and analyze the behavior of a network intruder. This system is previously setup with specifics vulnerabilities by the administrator.  

- It can be executed on any O.S. 
- Divert and distract the intruder. 
- Get information about the intruder. 
- Reports Attack tendencies
- Zero-days

-    Types of *Honeypots* (defined by the implementation)
-    For Production: Infrastructure purposes. 
-    For Researchment

-    Types of *Honeypots* (defined by the interaction)
-    High: Hardware installed in production. 
-    Low: Software for the reasearchment by the organizations of malicious traffic purposes . The risk is almost null because is used in virtual simulated enviroments. 
