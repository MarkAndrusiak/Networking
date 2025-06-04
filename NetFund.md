# Fundamentals of Networking

## Network Org
Quiz is on Day 6 (the 11th) Test is on the 18th - <br>

Network - Group of two or more nodes that are linked together to exchange data, share resources, and enable communication. <br>
Node - Any device on a network that deals in data communication (Handling, creating, storing or providing data) <br>
Physical - Physical connections on a network <br>
Logical - Data path followed on the network - Logical flow <br>

## Network Sizes / categories
2 general categories/ 3 subcategories: <br>

## PAN
Personal Area Network (PAN) - The smallest and most basic networks, typically confined to a home, office, or barracks room. <br>
- Primarily focused on flexibility (print from anywhere, stream or cast movies on a tv, etc) <br>
- Typically consist of PCs, printers, consoles, TVs, and peripheral devices. <br>
## LAN
Local Area Networks (LAN) - connect groups of devices within a building, or between 2-3 buildings in close proximity to share policies information and resources <br>
- Size can range from a few nodes to thousands
- Wired connections offer speed and security.
- Can have wireless connections but consist of **mostly wired connections** <br>
## WLAN
Wireless Area Networks (WLAN) a LAN primarily consisting of wireless network technology <br>
- Typically seen in the same applications as LANs (schools, libraries, coffee shops, airports, and laboratories) <br>
WLAN Technologies: <br>
- Wi-Fi
- Bluetooth
- Hot-spots <br>
## MAN
Metropolitan Area Networks (MAN) are a subset of Wide Area Networks (WAN), and incorporate Multiple LANs to span a medium-sized geographic area. <br>
## WAN
Wide Area Networks (WAN) connect multiple LANs or MANs over varying distances. Can span regions, countries, or the entire world. <br>
- WANs are used to relay data regardless of physical proximity. <br>
## Network Architecture
Network Architecture is another way we describe networks, but with a focus on how nodes in the network (LAN/WAN/etc) communicate and distribute resources. <br>
TWO TYPES:
- Client-to-Server -> Clients request and servers provide services/resources
- Clients initiate the communication, and servers are constantly listening for incoming requests
- in Client-to-Server, the computing power, memory, and storage requirements of the server must scale to match the needs of the clients <br>
- Peer-to-Peer -> has no distinct roles. <br>
Computers simply connect with each other in a chosen arrangement or workgroup to share files, printers, internet access, etc. <br>
- Tasks are allocated among all members of the network. <br>
- Every device on the network acts as a client and/or server depending on task <br>
Unlike client-server, computing power, memory, and storage requirements depend on the individuals in the network <br>
## Review
Quick review: Network org = Geographic size of network <br>
- Lan (1-3 bldgs, mostly wired) <br>
- WLAN (same as LAN, mostly wireless) 
- PAN (home/office space, "flexibility", game console/streaming)
- WAN (Large area, state/country world)
- MAN (Medium area, Multiple LANs)
Network Architecture = How devices in a network share resources: <br>
- Client to server = client requests and server provides
- Peer-Peer = everyone provides for everyone <br>
## Department of Defense Information Network
DODIN - thhe collection of networks owned and managed by the DoD <br>
3 subnetworks: NIPRNet, SIPRNet, JWICS <br>
**Non-Classified Internet Protocol Router Network (NIPRNet)** used by the DoD for exchanging sensitive but unclassified info. <br>
It allows users access to the public Internet via Gateways. <br>
**Secret Internet Protocol Router Network (SIPRNet)** - used to transmit classified info (up to including SECRET info) over a secure environment <br>
- SIPRNet is the DoD's SECRET classified version of the civilian internet. <br>
- Travels through NIPRNet (tunneling), but does not connect to the public internet. <br>

**Joint Worldwide Intelligence Communication Systems (JWICS)**
- Secure intranet system used by the DoD and the Intelligence Community (IC) <br>
- can transfer data up to the Top Secret classification level, including Sensitive Compartmentalized Information (SCI)
- Information is hosted and accessed within SCIF environments
- JWICS is an 'air-gapped' network, which is a network that is completely separate from the internet and can only be accessed physically <br>
## Network Topologies 
Point-Point -> contain exactly 2 directly connected nodes <br>
Every 1-1 connection is point-point, most networks in use today utilize these in a portion of their network. <br>
- Mostly seen when connecting two networks together, or used to send confidential info between two directly connected nodes. <br>
ADVANTAGES: <br>
- Highest bandwidth and Speed
- Simple connectivity, and easy to maintain <br>
DISADVANTAGES <br>
- Entire network depends on up-time of either node or transmission method (physical/wireless connection) <br>
## Bus Topology
**Bus** - All nodes are connected through a central copper cable (Daisy chained) <br>
- Any traffic sent is sent in both directions, along the central cable, in order to find its intended destination
- All hosts that receive the information, but those that it isn't meant for, simply disregard the info and drop it
- As soon as the signal reaches the end of the cable, a 'terminator' dissipates the signal, removing the data from the line so it does not bounce back
This topology is among the oldest, and not seen in modern infrastructure <br>
ADVANTAGES: <br>
- Repairs/replacement of a node does not affect other nodes
- Inexpensive to install and maintain
DISADVANTAGES:
- All devices are able to speak and listen, but must take turns to avoid a traffic collision
- Collision: Two signals being sent down a cable crash into each other, so both signals "drop" and are not properly sent
- ineffective for large networks
## Ring Topology
Ring: Each node (device) is connected to its two neighboring nodes. Traffic flows in a unidirectional manner from node to node. <br>
- Old topology that isn't seen often anymore due to resource issues and lack of redundancy
- Other topologies function better, but rings are still seen due to how cheap and fast they are to set up
ADVANTAGES:
- Reduces chance of collisions
- Connectivity between nodes is autonomous
DISADVANTAGES:
- If a cable or node breaks, the entire network goes down
- Data travels through every node to reach its destination
## Star Topology
Star - Every node is connected to a central device individually. <br>
- The most widely seen basic topology in modern networking

ADVANTAGES:
- Centralized network management
- Expansive, allowing additions to network without impacting others
- "Node redundant"
DISADVANTAGES:
- Can be expensive compared to previous topologies, due to central management devices and extra cabling <br>
- Not completely redundant (central management device)
- Central devices determine the network performance

## Mesh Topology
Mesh - defining characteristic of a mesh topology is that every node is connected to MORE THAN 1 other node to provide redundancy, and there is no central connection point <br>
Two types: <br>
Full mesh: Every node connected to every other node (max redundancy) <br>
- Typically used for network backbones (key infrastructure of a network) to protect the network from outages <br>
Partial mesh: <br>
- Nodes typically have connections to multiple nodes but not all <br>
ADVANTAGES: <br>
- Can manage high amounts of traffic
- redundant
- adaptive routing if a node breaks
DISADVANTAGES: <br>
- Most expensive option - redundancy costs resources
- Building and maintaining is difficult - requires specialized personnel
- Requires a LOT of cabling and ports on devices for comms
- Ports on devices are the physical docking points for cables, such as Ethernet port on back of workstations
## Hybrid Topology
Hybrid - Interconnection of multiple basic network topologies in a logical way that fits the needs of the organization <br>
- The resulting interconnection allows the nodes in a given basic topology to communicate with nodes that exist in other topologies. <br>


Generally, the advantages and disadvantages of hybrid technology depend solely on the topologies used to build the network. <br>
- Includes aspects such as scalability, reliability, and redundancy <br>
General Advantages/Disadvantage: <br>
- Configure network based on individual needs
- Maintenance and setup require extensive knowledge of all involved topologies <br>

## Network Connections
Cable Connections: <br>
- Ethernet (Twisted Pair and Coaxial)
- Fiber Optic <br>
Wireless Connections <br>
- Wi-Fi <br>
Signaling standards for Fiber Optic, Bluetooth, 802.11 (Wi-Fi), and 802.3 Ethernet were developed by the IEEE. <br>
## Copper Cabling
Two types: <br>
- Coaxial -> Almost obsolete for new LAN installations, however, network installations for cable TV and residential internet still use coaxial.
  - Consists of a single copper conductor shielded by plastic cladding and a braided metal conductor to reduce:
  - Induction (static/magnetism), Electromagnetic interference (EMI) Radio Frequency (RF) interference <br>
  
- Twisted Pair -> Consists of multiple cables twisted into pairs
  - Reduces interference from outside sources
  Unshielded Twisted Pair -> basic twisted cable standard mostly seen in home/office
Shielded Twisted Pair -> Uses a foil shield to further reduce interference, seen in modern infrastructure and static environments with equipment that is stationary <br>

## Twisted Pair
Defined in categories from 1 to 8 depending on performance and range. Most common is cat 5 <br>
- Connects using an RJ-45
## Straight Through (Or patch cables)
- Used to connect two different devices (PC -> switch)
- The wires are in the same order at both ends <br>
![image](https://github.com/user-attachments/assets/a483cb7c-3e5c-4f70-aa2a-55f9df78d1fa)

## Crossover
- Used to connect two similar devices (PC -> PC)
- Because both devices transmit on pins 1 and 2 and receive on 3 and 6, the cables must be swapped at one end to avoid data collision <br>
![image](https://github.com/user-attachments/assets/b187410d-dcbf-434d-8f7c-847031ba93f9)
## Fiber Optic
Fiber-optic cabling transmits pulses of light rather than electrical signals, eliminating EMI RF interference and induction static. <br>
Because fiber-optic cabling communicates at the speed of light, it is high-bandwidth high-speed, and can communicate across long distances. <br>
The center core is made of a glass or plastic fiber surrounded by a cushioning plastic coating, a layer of Kevlar, and an outer insulating jacket made of Teflon or PVC. <br>

## Wireless
Wireless Networking <br>
- Also known as Wi-Fi or Wireless Ethernet
- Replaces cable interface with an antenna to provide access to wireless media
- Antenna communicates with a wireless access point (WAP) transceiver
- Each network is identified by a Service Set Identifier (SSID)
- Wireless devices must be on the same SSID to interface with each other
- common radio frequencies used are 2.4GHz, 5GHz, and recently, 6GHz






