# OSI Model
## The OSI Model
The Open System Interconnection (OSI) Reference Model provides a standardization for network comms<br>
and encompasses everything from how different services and applications perform in a GUI down to the individual bits moving across a wire or out through an antenna. <br>
Standardizing this process ensures long-term compatibility of nodes/hardware from multiple manufacturers across the information technology environment. <br>
This model is also commonly used for troubleshooting, as it identifies where different services, hardware, and capabilities are situated in a given line of communication. <br>
![image](https://github.com/user-attachments/assets/74c71434-8760-43bf-a20e-9521ca14ee77) <br>
The OSI model breaks data transmission into 7 layers: <br>
1-7 P D N T S P A <br>
7-1 A P S T N D P <br> 
## Encapsulation
Data Encapsulation - The process of taking a piece of network traffic, and adding more info to the beginning (or sometimes end) to form a new piece of data. <br>
- Similar to putting a letter (data) inside an envelope (header/trailer). <br>
When information flows from one layer to the next, network traffic takes on a different name, called a PDU (Protocol Data Unit), depending on where it is in the encapsulation process. <br>
- The Protocol Data Units you will need to know are: Data, Segment, Packet, Frame, and bit. <br>
## Encapsulation and Decapsulation
Encapsulation - When info is going down the stack (layer 7 to 1), relevant node is adding a header to the data. <br>
Decapsulation - When info is going up the stack (layer 1 to 7), relevant node is removing a header from the data. <br>
## Layers 5-7 Session, Presentation, and Application
These layers control the interactions and usage with application programs, user display, and allowing access to network resources for end users. <br>
- There are distinct duties and characteristics of each of these layers in the OSI model, but some services/protocols apply to more than one of them
- The Protocol Data Unit (PDU) for all 3 of these layers is "data". <br>
## Application Layer
The Application Layer (Layer 7) is the "visual layer" <br>
- Receives input from the user and displays data in a way they can understand
- Provides an interface for the end user's device across a network
- It is not an application - it represents the components in the application, which control comms with other nodes <br>
Layer 7 is responsible for: <br>
- Displaying received information to the user (via an interface)
- Controls the interface methods used in communications across the network <br>
## App Layer PROTOCOLS
Layer 7 Protocols: <br>
- HTTP & HTTPS (Web Browsing)
- Telnet & SSH (Remote Access)
- FTP & TFTP (File Sharing)
- DHCP & DNS (Networking Support)
- POP3, IMAP, & SMTP (Email)
- SNMP & LDAP (Host/Network management) <br>
## App Layer Encapsulation
This is where your raw user data begins in transmission. It is not yet encoded, translated or encapsulatedd in any way yet. <br>
When data is ready to transmit -> handed off to Presentation Layer for encoding and formatting. <br>
## Presentation Layer
The Presentation Layer (Layer 6) establishes context for the application layer syntax/semantics, <br>
taking the information from the application layer of one system and reformatting it to be readable by the application layer of another system. <br>

Layer 6 is responsible for:
- Data Compression
- Coding (ASCII, EBCDIC, UTF-8)
- Encryption/Decryption
  - Encryption is primarily done at layer 6, but can be done at other layers, each having its own advantages and disadvantages
## Presentation Layer - Services/Protocols
Layer 6 Services: <br>
- ASCII
- JPEG
Layer 6 Protocols: <br>
- TLS/SSL (Security Protocols)
## Presentation Layer - Encapsulation
When your data from the application layer comes down to the presentation layer (save as...) the data is encoded and compresses into a standard format to be transmitted.
- Optionally, as discussed, encryption happens at this stage
Once in a standard format, the data is handed down to the Session Layer. <br>
## Session Layer
The Session Layer (Layer 5) controls the connections between computers, and establishes request/response communication. <br>
It also receives service requests from Layer 6 and issues requests to Layer 4 through application programming interfaces (APIs, or in today's world "Apps") <br>
- Inputs from the user, regarding the session, make requests (Authentication, closing sessions, restoring sessions, etc)
- The first layer discussed that uses a client/server concept <br>
Layer 5 is responsible for <br>
- Establishing and managing connections between local and remote applications (clients and servers)
- Establishing procedures for check-pointing, suspending, restarting, and terminating a session
  - This is done because Layer 5 organizes and synchronizes all data exchanges, allowing for it to be check-pointed
- Closing or re-opening connections that have become inactive
  - This concept is referred to as Layer 5 having a 'semi-permanent dialogue'
## Session Layer - Services
Layer 5 Services: <br>
- Authentication
- Authorization
## Session Layer - Encapsulation
When data is handed to the session layer, a Session ID is tagged to the data. <br>
This is used for managing the connection, the session layer's primary role. <br>
Your data is then handed off to the transport layer <br>

## Transport Layer
The transport layer (Layer 4) manages reliability and quality of traffic <br>
- Layer 4 PDU is a "segment" <br>
Layer 4 is responsible for: <br>
- Segmentation/Desegmentation of the data stream
  - Segmentation is when a layer 4 segment is too big to send, so it is split into several pieces. At the destination, these pieces are put back together in order <br>
  and the traffic is processed normally <br>
- Flow control & congestion avoidance
- Security functionalities (such as firewalls)
## Transport Layer Hardware/services/protocols
Layer 4 Hardware: <br>
- Firewalls
Layer 4 Protocols: <br>
- TCP
- UDP
## Transport Layer - Encapsulation
When data is handed to the transport layer, it is broken into smaller blocks of data. At this point, a layer 4 header is added to the beginning of the "data" from the above layers. <br>
This makes an entirely new data package called a "segment"
- A header is simply a section of the traffic that contains info specific to that protocol/layer
- The layer 4 header contains info pertaining to TCP/UDP, and flow control
This segment is then handed down to the Network Layer. <br>
## Network Layer
The network layer (Layer 3) provides the means of transferrign packets from a source to a destination via one or more networks. <br>
- Layer 3's PDU is "packet"
Layer 3 is responsible for: <br>
- Forwarding and routing packets
- Inter-network addressing (IP Addresses)
- Fragmentation of data Packets
  - Fragmentation is the Layer 3 process of segmentation (layer 4), and functions similarly
## Network Layer - Hardware/Services/Protocols
Level 3 hardware: <br>
- Routers
Layer 3 Protocols: <br>
- Ipv4 & IPv6
- ICMP
- IGMP
- IPSec
- Nat
## Network Layer - Encapsulation
The layer 3 header is now added, which contains forwarding information for layer 3 hardware/services. <br>
Once the layer 3 header is added, it is no longer a "segment" it is now a "packet" <br>
This packet is then handed down to the Data Link Layer. <br>

## Data Link Layer
The data link layer (layer 2) transfers data between adjacent network nodes in a WAN or between nodes on the same LAN segment. <br>
- Layer 2's PDU is "frame"
Layer 2 is responsible for: <br>
- Detecting and (sometimes) correcting errors that may occur at the physical layer
- Defining the protocol to establish and terminate a connection between two connected devices <br>
- Defining the protocol for flow control between devices
  - Flow control makes it possible for a recipient of data to tell you how fast/slow you should send data, and vice versa <br>

## Data Link Layer - Hardware/Services/Protocols
Layer 2 Hardware: <br>
- Network Interface Cards (NIC)
- Switches <br>
Layer 2 Protocols: <br>
- MAC Addresses
- IEEE 802.3 (Ethernet)
- IEEE 802.11 (Wi-Fi)
- ATM
- ARP
- HDLC / Frame Relay / MPLS / PPP (WAN Protocols)
Wired Connections: <br>
- Copper Cables (Coaxial and Twisted Pair)
- Fiber Optic
    - Large amounts of data over large distances -- Connects servers and main infrastructure
Wireless Connections <br>
- Wi-Fi
    - 2 Ghz, 5GHz, and 6 GHz -- uses Wireless Access Points
- Cellular
  - 'Pair of radio frequencies' -- uses cell towers
- Satellite
  - Global communication -- Geosynchronouus (GEO) & geostationary vs Low Earth Orbit (LEO)
  - Topologies -- Mesh vs Star
Ethernet: IEEE project 802.3 <br>
- Communications modes:
    - Simplex, Half-Duplex, Full-duplex
- Standards
    - 100 BASE-T - UTP/STP - Half/Full Duplex - Up to 100m
    - 1000 BASE-T - UTP/STP - Half/Full Duplex - Up to 100m
    - 10GBase-T - STP - Full Duplex Only - Up to 100m
    - 40GBase-T - STP - Full Duplex only - Up to 30m
- PoE - Provides DC power over Ethernet
    - Requires PoE Hardware that can provide DC current
        - Ex. PoE phones, WAP, IP Cameras <br>
## Data Link Layer Hardware/Services/Protocols
"Fiber Optic Cabling" - Uses light pulses - Simplex communications <br>
- Types of Fiber
  - Single-mode: One transmission path, expensive, faster and further distances
  - Multi-mode: Multiple Transmission paths in one cable, cheap, slower and shorter distances
PSTN - "analog" phone system - Converts voice to electronic signals <br>
- Allowed for voice and data, replacing POTS (old system)
- In the process of phasing out - being replaced by VoIP <br>
VoIP - "digital" phone system - Converts voice to digital signals
- Uses RTP and H.323
  - Real Time Protocol (Delivery)
  - H.323 (Call Management) <br>
## Data Link Layer - Encapsulation
Once the packet is handed to the Data Link Layer, a Layer 2 header and trailer is added to the packet <br>
- Headers are added to the beginning of the packet, and trailers are added to the end of it, making it a "frame"
  - This frame is in charge of error checking, and communication between layer 2 protocols/hardware/services
The frame is then sent to the physical layer <br>
## Physical Layer
The physical layer (layer 1) specifies the physical and electrical components, including cables, cards, and any other physical aspects. <br>
This layer is where data is moved across the network.
- Layer 1 PDU "bit" <br>
Layer 1 is responsible for: <br>
- Bit rate control to define transmission mode (Simplex [fm radio], half-duplex [walkie-talkie], and full-duplex [phone call])
- Converts the binary data into electrical, optical signals, or EM waves <br>
## Physical Layer - Hardware/Services/Protocols
Hardware Examples: <br>
- Amplifiers
- Repeaters
- Hubs
- Wires/Antennas
Layer 1 Technologies: <br>
- DSL
- Signals
  - Voltages, radio frequencies, optical signals, etc.
## Physical Layer - Encapsulation
Once the frame is handed to the Physical Layer, it is translated into a signal and sent along its transmission medium in binary. <br>
Once the signal reaches the destination address, it begins the process of going back up the layers (decapsulation) <br>
## TCP/IP Model
The TCP/IP Model was developed by DARPA and the DoD, and predates the worldwide global internet and the OSI model. <br>
- As internet grew, model released to public
- Also referred to as the DoD model, or "internet model" <br>
The TCP/IP model defines a suite of protocols that had an end goal of ensuring a connection between a source and destination. <br>
- The TCP/IP model is the model that organizations follow today when discussing networking in practical applications <br>
The TCP/IP model is a 4 layer variation of the OSI model <br>
The TCP/IP layers are as follows from top to bottom: <br>
- Application layer
- transport layer
- internet layer
- network access layer <br>
All layers maintain the same functionality and PDUs <br>
- TCP/IP Layer1: Culmination of OSI layers 1-2 (data link, physical) PDU - both bit and frame
- TCP/IP Layer2: OSI Network Layer 3 becomes TCP/IP Internet Layer 2 with the same PDU - packet
- TCP/IP Layer3: The exact same as OSI Model (protocol, function PDU, etc)
- TCP/IP Layer4: Culmination of OSI layers 5-7 (Application, Presentation, Session) PDU - Data <br>

Today the TCP/IP model is the standard for practical use by network engineers and analysts when building, maintaining, and analyzing network connections. <br>
- The TCP/IP model represents the "implementation" of the theoretical OSI Model, as our jobs do not rely on separating Layer 1 and Layer 2 or Layer 5, Layer 6, and Layer 7 concepts.
- The OSI Model is more widely used in academics, therefore it is important to know both, as you will likely hear the OSI Model referenced often in your career. <br>

## OSI Model Protocols

L1 - Topologies / Cables / DSL <br>
L2 - ATM / 802.3 / 802.11 <br>
![image](https://github.com/user-attachments/assets/976db1bc-ae6f-4b3a-a550-240b78dc507a)





