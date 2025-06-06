# Network Devices
## Network Devices
Network devices are hardware and physical devices that are required for communication across a network. <br>
- Specifically, they control/allow data transmission in their network, or from one network to another. <br>
Aside from the OSI model, network devices are categorized by the Following functions: <br>
Core: (Interconnect other hardware) <br>
- Router
- Switch
- Hub
- Repeater
- Amplifier
- Wireless Access Point
- Cabling Structures (patch panels, cabling racks, etc) <br>
Border: Sits on the outside of one network that faces another. <br>
- Firewall
- Router <br>
End Stations: Establish networks and connections
- Network Interface Controller (NIC)
Core Routers vs Border (Edge) Routers: <br>
- Core: Connects subnets together and internal network devices
- Border: Connects the private network as a whole to the public network <br>
## NICs
A Network Interface Card (NIC) works as a device's interface to a network, allowing for you to communicate with the rest of the networks you belong to <br>
as well as other networks.  <br>
- Essentially works as a translator for your device, allowing it to speak the networking language. Without it, you are unable to connect. <br>
A network interface card is a network adapter that comes as either an expansion card that plugs into your motherboard or as a USB dongle. <br>
- Layer 2 of the OSI model <br>
Characteristics of a NIC: <br>
- Provide you a network interface, for either ethernet or wireless networks
 - If you have both Ethernet and Wi-Fi capabilities, then you have 1 individual NIC for each interface <br>
- Come as either simplex, half-duplex, or full-duplex
- Various designs exist, rated by speeds of megabits per second to gigabits per second
  - For cutting-edge technologies, speeds greather than a gigabit (tera - peta - zeta etc.) <br>
## Amplifiers & Repeaters - Attenuation
As signals travel across a medium (wired or wireless), they lose signal as they travel -> Attenuation <br>
- Transmission mediums have standardized maximum transmission lengths
  - These mark the limit a medium or device can transmit before attenuation causes it to become unreliable <br>
Amplifiers and repeaters are devices used to help transmit signals past their maximum transmission length <br>
## Amplifiers
Amplifiers are networking devices that exist to strengthen the signal (from the source) to allow it to transmit further than the maximum transmission length <br>
![image](https://github.com/user-attachments/assets/6aa1be70-228a-4cb3-97b1-62f668094cb2) <br>
In the diagram, the amplifiers on either side are only used when that side is the source of traffic. <br>
(Since green is source, blue does not impact communication for this side of the conversation) <br>
Amplifiers are seen in dynamic wireless networks, mobile technologies, and remote area networks <br>
- Used to increase the strength oof the signal, allowing it to take a weak signal, and transmit it loudly <br>
  - Referred to as 'taking a low input power, and outputting a high output power <br>
Repeaters sit in between transmission links to re-transmit signals (as if the signal came from them originally), and function bidirectionally, unlike an Amplifier. <br>
Repeaters are used in static, more stationary, environments <br>
- Wi-fi repeaters are common in homes to expand the reach of the Wi-Fi <br>
Both Repeaters and Amplifiers work at Layer 1 of the OSI model. <br>
## Hubs
Hubs are passive devices, simply connecting nodes. <br>
- Hubs receive input through a port and blindly broadcast that data to all other ports. <br>
  - Operate in half-duplex due to being unable to filter traffic <br>
- They don't have any configuration or software associated with them, making them non-customizable
These operate at layer 1 of the OSI model <br>
Hubs are also unable to filter data, and therefore operate with half-duplex comms only
- In the event that computers transmit packets simultaneously, collisions occur, and the traffic is dropped
Any nodes that are connected, and are subject to traffic collisions, are referred to as being in the same "Collision Domain" <br>
- Since these nodes also receive any broadcast frames sent on the LAN, they are in the same "broadcast domain" as well <br>
## Switches
Switches are able to connect various devices together (PCs, printers, routers, etc) via cabling. <br>
- Switches allow these to communicate with a specific node connected to that switch (rather than broadcast)
- Each device is connected to the switch via a Switch Port (most will have 4, 8, 12, 24, or 48 ports) <br>
Switches are faster than hubs, and allow for full-duplex traffic, eliminating issues with collisions that are prevalent in hub based networks. <br>
Traditional switches operate at layer 2 of the OSI model <br>
- This is due to their ability to work with MAC addresses (layer 2), and forward traffic through LAN environments
  - These MAC addresses are stored in MAC Address Tables (MATs) <br>
## Switches - Address Learning
Switches can identify the devices connected from MAC addresses, within the ethernet layer 2 frames being sent. <br>
- A switch's ability to forward traffic, based on MAC addresses, relies on its ability to perform Address Learning
Every port on a switch has its own MAC address. <br>
- Switch ports, unlike a computer's ethernet port, run in "Promiscuous Mode"
- Receive all frames it sees on the port
As traffic flows through the switch port, the switch logs the source port in its MAC Address Table and maps that source MAC to the port it received the data from for future reference <br>
Switches perform communication by copying incoming frames (from the data source) from one switch port and sending them out of another switch port (connected to the data destination) <br>
While switches don't automatically send broadcast frames, they do have the capability to send them in order to learn what devices are connected to them
- This means that they do not define broadcast domains
However, switches run full duplex -> issues with collisions are eliminated over ethernet networks (prevalent in hub networks) <br>
- Referred to as a switch's capability to "define collision domains" <br>
Switches are available in many forms, which all vary in size, the number of nodes that it can support, and their general purpose.
The two types of switches discussed are:
**Purpose**: <br>
- Stand-Alone Switch -> Typically intended for a home or office room next to your desktop
- Rack mounted Switch -> Switches that manage multiple office's devices <br>
**Configuration Type**:
- Managed
- Unmanaged <br>
## Switches Config Types
Unmanaged Switches<br>
- Hold no configuration interface or options
- Often used in a small office/home office environment
- Referred to as plug and play as they aren't configured for a specific environment <br>
Managed switches <br>
- These have a config table, giving you a way to modify the way it functions<br>
This allows for the following practices, among others: <br>
- Duplexing
- VLANs
- Port management
- Traffic Management
Config tables are accessed via CLI, Serial Console Connection, Telnet/SSH
