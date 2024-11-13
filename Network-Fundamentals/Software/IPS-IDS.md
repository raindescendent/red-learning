All this Systems are based on **RULES**

**IDS** 
*Intrusion Detection System*

*NIDS* Network Intrusion Detection System
*HIDS* Host Intrusion Detection System (Computer Scope)

Perform actions reporting detections of not-regular patterns of packet traffic based on rules 

- Alert 
- Logs

**IDS** 
*Intrusion Prevention System*

*NIPS* Network Intrusion Prevention System
*HIPS* Host Intrusion Prevention System (Computer Scope)

Perform actions when detects not-regular patterns of packet traffic and "prevent" the traffic based on rules 

- Alert 
- Logs
- Drop packets
- Reject connections



**RULES**

*Signature-based detection* 
Set of rules which identify the specific pattern of the traffic comparing it against a list of known malicious indicators. 

*Behaviour-based detection* 
The technique allows to identify known threaths as a new uknown's threats. Training the IDS/IPS trading them with "normal traffic" indicating a specific time to analyze the packets establishing the "normal pattern" to do future comparisons. 

*Policy-based detection*
Similar to signature-based threat detection, but it uses a database of specific protocols defined by the manager/admin and blocks any activity violates those protocols.


------------------------------------


**Snort** IDS/IPS Software

It works with the detection and prevention systems and perform actions:

- Live Traffic Analysis (Alerts, Logs, Drops, Rejects)
- Log Packets (Not-live Analysis)
- Sniffing (Monitoring and Capturing data packets)


Config File contains: 

- Path to rules
- Plugins 
- Source net (analyzed network)
- External net (any other network)


The software works on 3 modes: 

- Sniffer 
- Packet logger
- NIDS/NIPS

*Snort Network Placement*

- IPS: Works in network between router and switch.
- IDS: Works inside the switch.