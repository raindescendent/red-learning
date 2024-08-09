***Open Systems Interconnection model***

Created by: International Organization For Standarization (**ISO**) in 1984.

Understanding and designing communication networks.
The communication between systems starts from High to Low Level and reverse.

**7 LAYERS**

- Physical Layer (Bits):  This layer deals with the physical transmission of data bits across a network cable or wireless connection. It ensures the ones and zeros representing information travel reliably.

Converting bits (binary data) into electric or electromagnetic singal. 


- Data Link Layer (Frame):  This layer packages data into manageable chunks and adds error-correction mechanisms to ensure the data arrives without errors. It's like putting the data bits into envelopes for delivery.

It brings identification for the devices of the layer 1 connected and eventually links them to the network. 
It defines: 

    - Adressing
    - Network Topology
    - Error notification
    - Frame sequencing
    - Data flow control

This layer is divided in 2 sub-layers: 
    - LLC (Logical Link Control)
    - MAC (Medium Access Control)


- Network Layer (Packet):  This layer handles routing the data packets across the network. It figures out the most efficient path to get the data to its destination, like a GPS for your data packets. It provides a local identification to the connected devices giving the warranty of sending/reveiving packages between them. 


- Transport Layer (TPDU):  This layer ensures reliable delivery of data between applications on different devices. It acknowledges receipt of data and re-sends packets if there are any errors. It works with TCP/UDP. 
Additionally this layer fragments the data packages into smaller size due to MTU. 
    - MTU (Maximum Transmission Unit): A measurement in bytes of the largest data packets that an Internet-connected device can accept.

    
- Session Layer (SPDU):  This layer establishes, manages, and terminates sessions between communicating applications. It sets up a connection for communication to take place.


- Presentation Layer (PPDU):  This layer deals with the format of the data being exchanged. It ensures both devices understand how to interpret the data. It transforms the data into other formats like sound, image, text, etc. 


- Application Layer (APDU):  This layer is the closest to the end user. It provides network services to applications like web browsing, email, and file transfer. This is the layer you interact with when you use any application that relies on the network. 
It describes how these applications read and work with the final information that is delivered to the user who is using the device. Some protocols are used by this applications like HTTP, SMTP, POP, IMAP, etc.







