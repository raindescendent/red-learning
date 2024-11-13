Cyver Kill Chain or Lockheed Martin Cyber Kill Chain

***Discovering Cyberattacks Chain***

   - Reconnaissance
   - Weaponization
   - Delivery
   - Exploitation
   - Installation
   - Command & Control
   - Actions on Objectives 


**Recon**

Discovering and collecting information on the system and the victim.

Starting point:

- OSINT (Open-Source Intelligence) 

Refers to the practice of collecting data from free sources that are available to the general public. 



***Weaponization** 

In this phase we can choose or develop our 'arsenal' to perform the different stages of the attack. Some of them are: 

- Malware: Designed software to damage, disrupt or gain unauthorized access 
- Exploit: Code that takes advantage of vulnerabilities or flaws in the system
- Payload: Malicious code



***Delivery***

Delivery phase consist in decide the technique for transmitting the payload or malware to the target. Some popular options are

- Phishing Email
- Infected USB Drives
- Watering Hole (Compromise a frequented group-used resource, i.e. websites., to infect and propague the malware.)



***Exploitation***

This phase is for gain unauthorized access and eventually perform privilege escalation or lateral movements through vulnerabilities exploit. 

- OWASP Top 10: Server-based or web-based vulnerabilities
- Zero-day exploit: Unknown exploit that exposes vulnerabilities on software/hardware. Leaving NO opportunity for detections. 



***Installation (persistence)***

As attacker/pentester we want to keep the access to the system that we was attacked before. That is when we need to install a 'persistent backdoor'. Some examples are: 

- Web shell: malicious script written in web development programming languages used by an attacker to maintain access to the compromised system.
- Create or Modify System Process: Windows Services
- Masquerading
- Registry Run Keys (Startup Folder Persistence)


***Command & Control (C2)***

At this stage we need to establish a channel through the malware to control them remotely. 

- C&C or C2 Beaconing: The infected host will consistently communicate with the attacker 'C2 server'. 

- C2 Server: A set of programs and rules to remotely control the installed malware on the victim host machine

Most common C2 Channels: 

- HTTP/HTTPS: Blending the malicious traffic with the legit traffic to avoid detection. (80, 443)
- DNS Tunneling



***Actions on Objectives (Exfiltration)***

After the performed 'kill-chain' we need to take action on the original objectives/motivation previously defined to execute the penetration test. 

- Collect and exfiltrate any sensitive data (user-credentials, etc.)
- Privilege Escalation
- Internal Recon
- Pivoting
- Deleting backups
