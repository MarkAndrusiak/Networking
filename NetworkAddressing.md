# Network Addressing Characteristics
## Physical / Hardware Addressing
A Media Access Control address (MAC Address) is the layer 2 (data link) identifier for any physical device. <br>
- MAC addresses are tied to a specific device, and do not change
- When devices first connect to a LAN, they use their MAC address to locate each other and begin learning what is also on the network. <br>
MAC Addresses format: 48-bits, or 12 digits of hexadecimal, or 6 Bytes <br>
Mac Addresses are known as "Physical" addresses, but they reside at the Data Link Layer of the OSI model.
- Organizational Unique Identifier (OUI) - The first 24 bits, or 6 hexadecimal digits, contain the ID number of the manufacturer of the network adapter. <br>
Larger vendors can have multiple OUIs assigned to them. (OUIs are open-source information and can be looked up on the internet)
- The last 24 bits contain the serial number assigned to the specific device, and are not shared with any other device with the same OUI. <br>
![image](https://github.com/user-attachments/assets/1cc42846-ff47-4d0a-a5a9-297e7e749a1c) <br>
The MAC address does not give any indication as to where your device is located, geographically or within a network <br>
unlike other addresses we learn about next. <br>
- No two devices on a network can share the same MAC Address <br>
MAC Addresses, as a layer 2 address, help other devices communicate and perform layer 2 functions such as <br>
Address Resolution Protocol (ARP) (discussed later) <br>
## Logical Addressing - IPv4
Logical Addressing (IPv4) - IPv4 contains 32 bit integers, or 4 bytes (octets) of binary. <br>
Dotted Decimal Notation (DDN) is the standard format for writing an IPv4 address. (0.0.0.0-255.255.255.255) <br>
IPv4 address can also be written in hexadecimal or binary notation. <br>
32 bits of binary allows for up to 4.3 billion possible addresses. <br>
- Dotted-Decimal Notation: 172.16.254.1
- Binary Notation: 10101100.00010000.11111110.00000001
- Hexadecimal Notation: AC.10.FE.01 <br>
![image](https://github.com/user-attachments/assets/f2916bf5-c2ef-4c3c-8a4b-73c37044fe35) <br>
## Logical Addressing Ipv4 Address Types
Broadcast: <br>
Represents every interface in the broadcast domain ("one-to-all"). <br>
Packets using this address type are delivered to every host on the device's network. <br>
Broadcast Domains are a group of devices that will receive broadcast traffic from any other host in the group <br>
Broadcast traffic is forwarded by switches, but not by routers <br>
All devices connected via one or more switches are in the same broadcast domain <br>
Anycast: ("One-to-nearest") <br>
Anycast traffic is unique, in the sense that it is only used when a group of devices, typically servers, share an IP. <br>
Anycast is used to identify the closest node out of these servers, and route it there. <br>
The decision on which server is the closest to the sender is not determined by the packet, but by the routers in charge of the servers' network. <br>
IPs are used as dynamic logical addresses and can be easily changed if needed. <br>
While we initially had 4.3 billion Ipv4 addresses available, the popularity of the internet quickly used them all. IPv4 addresses are still very common, but no more can be allocated <br>
The rapid depletion of IPv4 addresses led to the creation of private address space, network address translation (NAT), classless inter-domain routing (CIDR), and eventually IPv6 <br>
## ARP (Address Resolution Protocol)
Address Resolution Protocol - ARP is a layer 2 protocol that correlates an ever-changing IP address to a fixed MAC address within the LAN. <br>
Each host on your network has an IP address assigned to it, and a MAC address given by the manufacturer. IPs may change over time, but a MAC address will not. <br>
When IPs change, or when a new node is added to your network, ARP matches the node's physical address to its new logical address.

## Example
PC3 is trying to find the 192.168.1.5 address in order to send some information. <br>
It will send a layer 2 MAC broadcast message (ff:ff:ff:ff:ff:ff:ff) saying "Who is 192.168.1.5?" to every computer on your network <br>
The computers that do not have this IP will drop the traffic <br>
PC4 the 192.168.1.5 host, will receive this info and reply with its MAC address. <br>
When this communication occurs, the router, switch, and PC will log, "B4:40:AE:EF:A1:3B has IP address 192.168.1.5" in their ARP tables. <br>
The addresses are then resolved <br>
![image](https://github.com/user-attachments/assets/b9e0df8d-e39d-443a-ace0-aef93f600a73) <br>
Now, when data destined for you arrives, the network compares the IP on the data to the MAC addresses in the ARP cache, and forwards the data to you. <br>
The ARP cache is simply the storage of MAC-to-IP resolutions that have recently occured. Due to its small size, the ARP cache is purged regularly to free space. <br>
When traffic passes through your network and a resolution is not in your ARP cache, or if the info in the cache is outdated <br>
the ARP process is performed again to find the correct host. <br>

## IP Address Classes
The 32 bit IP address from IPv4 is broken up into five classes (A, B, C, D, E) to form what is known as "Classful" Networking, a legacy system that is no longer in use. <br>
A classful "range" is determined by the first octet of the address. <br>
**Class A (0-127) and Class B (128-191)** <br>
- Used for large enterprise networks and ISPs <br>
**Class C (192-223)** <br>
- Used by residential homes and small businesses
**Class D (224-239)** <br>
- Reserved for multicast addressing (not assignable to networks or nodes)
**Class E (240-255)** <br>
- Reserved for experimental use - not seen naturally in network traffic <br>
Classful Networking wasted vast amounts of IPv4 address space. <br>
The smallest available network, class C, provided the average consumer with 254 assignable IP addresses, far more than most people need. <br>
These advancements in networking began to conserve IPv4 addresses: <br>
- Private address ranges
- Subnetting/Classless inter-domain routing (CIDR)
- Variable Length Subnet Masking (VLSM) <br>
## Private IP Addresses
Private IP addresses only work within their own private network - they are not routable on the public internet <br>
The introduction of Private IPs separated the internet into 'Public' networks and 'Private' networks. <br>
Because private IP ranges are not used on the public internet, they are reusable worldwide. <br>
This advent helped curb the exhaustion of IPv4 address space. <br>
You should be immediately suspicious of a private IP address on a public network. Security engineers block private IP ranges coming into their network from public networks. <br>
Private IPv4 ranges: <br>
Class A: 10.0.0.0 - 10.255.255.255 <br>
Class B: 172.16.0.0 - 172.31.255.255 <br>
Class C: 192.168.0.0 - 192.168.255.255 <br>
Special Purpose IPv4 ranges: <br>
Loopback (Network Diagnostic Tool) <br>
127.0.0.0 - 127.255.255.255 <br>
APIPA (Automatic Private IP Addressing) <br>
169.254.0.0 - 169.254.255.255 <br>
CGN or CGNAT (Carrier-grade NAT) <br>
100.64.0.0 - 100.127.255.255 <br>
## Subnet Masks
Subnet mask - Identifies how many of the 32 bits in an IPv4 address belong to the network <br>
Network ID: <br>
- Portion that stays static for all nodes in the same network
- Portion of the IP that is unique to that network <br>
Host ID: <br>
- Portion that changes from node-node
- Portion of the IP that is unique to the host <br>
Logical AND Method - Boolean AND process (ref: logic gates) used by the coputer to turn off 'host bits' and identify the Network ID for an IPv4 address. <br>
Subnet masks are used in conjunction with IP addresses to help devices define: <br>
- The networks in which an IPv4 address belongs
- The range of IPv4 addresses that are assignable to devices within that network
- The IPv4 broadcast address for that network
Subnet Masks accomplish this by identifying the "Network ID" and the "Host ID" <br>
- An example of this is the IP 192.168.1.34 paired with subnet mask "255.255.255.0" <br>
- The network portion of the address is 192.168.1 the host portion is .34 <br>
Subnet masks can also be expressed with a forward slash followed by the number of bits being used for the network. <br>
This is known as CIDR Notation (Classless Inter-domain Routing) <br>
## Logical & Method
The logical "AND" method uses the Boolean logic function, "AND" to compare an IP address with a subnet mask (both in binary form) <br>
to turn off host bits and produce the network ID. <br>
In order to compare each bit of the IP address to the subnet masks, here is a refresher on logical "AND" gates: <br>
- Input 1 | 1 = 1
Compare each bit vertically and run the AND function against the entire binary line, the output is your network ID. <br>

## Logical Addressing IPv6
Ipv6 addresses are represented by 8 groups of 4 hex digits: <br>
While IPv4 offered 32 bits, IPv6 are 128 bits, allowing for **340 undecillion addresses**  <br>
If IPv4 were the size of a golf ball, IPv6 would be the size of the sun. <br>
IPv6 has a fixed header size and removed checksums, two structure decisions which enabled superior speed and efficiency <br>
- A static packet header size means packets don't have to defragment like in IPv4.
- A lack of a checksum in the header means that routers do not need to check at every hop whether or not the packet has been tampered with. <br>
![image](https://github.com/user-attachments/assets/80ed273f-e92f-4615-a87c-e9a4af4648f7) <br>
3 address Types: Unicast, multicast, anycast: <br>
IPv6 Unicast Addresses fall into 6 categories:
- Link-local address -> designed for use on a local network
- Globe address -> designed for use on any network
- Loopback address -> designed for use in troubleshooting network connections
- Unspecified address -> indicate the absence of a valid address
- Site local -> used for Private IPs
- IPv4 Compatible addresses -> Used for devices that support IPv6 and IPv4, 96 zeroes followed by 32 bit IPv4 address <br>
Multicast: One-to-many address type. All IPv6 multicast addresses share the prefix of FF00::/8 <br>
Anycast: One-to-nearest address type. Appears the same as an IPv6 global address. <br>

## IPv6 Transition Methods
IPv4 is still widely in use. while the world transitions to IPv6, methods have been developed to allow traffic to communicate with both protocols. <br>
The following transition methods are in use today to allow for these protocols to coexist: <br>
- Dual Stacking
- Tunneling
- Translation
## Dual Stacking
Dual Stacking: requires infrastructure that supports IPv4 and Ipv6 to run both protocols at once. Most modern infrastructure today has this capability. <br>
## Tunneling
Tunneling: IPv6 packets are encapsulated inside IPv4 packets. <br>
When IPv6 packets begin to travel out of your network, they are encapsulated with an IPv4 header, allowing the packet to traverse across IPv4 infrastructure, and can be translated back to IPv6 at dest. <br>
This tunneling is traditionally done at the router. A commonly used tunneling tech for IPv4 to IPv6 is Teredo. <br>
## Translation
Translation: Method where dual stack devices are configured to translate between IPv4 and IPv6. <br>
When packets pass through the router, they are translated from IPv6 to IPv4, travel along IPv4 networks, and are translated back at destination. <br>
## Address Verification
Address Verification is the process of identifying IP addresses through the Windows or Linux command-line/terminal.
- Windows "ipconfig"
- Linux "ifconfig" or "ip addr" <br>
Windows Address Verification - Go to your command prompt and type "ipconfig" <br>
From this command you can see MAC addr. IP addr. Subnet Mask. <br>
## Linux Address verification
Go to your VM and type "ip addr" or "ifconfig" <br>
Can see: Mac addr. IP addr. Loopback addr. Subnet Mask. <br>

## OSI MODEL REVISIT
L3 IPv4 IPv6 <br>
L2 ATM 802.3 802.11 MAC ARP <br>
L1 Topologies Cable DSL <br>
![image](https://github.com/user-attachments/assets/308b0fc5-2a96-4418-8cb9-b2bb53606079) <br>






