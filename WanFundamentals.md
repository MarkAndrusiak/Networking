# Wan Fundamentals
Multiplexing is the process of taking multiple signals and turning it into one signal <br>
Two types: <br>
- Digital
- Analog
Analog Falls into two types: <br>
- Frequency Division Multiplexing (FDM)
- Wavelength Division Multiplexing (WDM)
Digital multiplexers are often times seen as: <br>
- Time Division Multiplexing (TDM)
## Analog Multiplexing
Frequency Division Multiplexing (FDM) is the most common type of analog multiplexing <br>
This takes signals from all different frequencies and turns them into a single signal. <br>
- A TV would be an example -> You have one cable line running to the TV, but many different frequencies from separate channels. <br>
Wavelength Division Multiplexing (WDM)
- Much like its name implies, this type of analog multiplexing takes different wavelengthhs and combines them into a light spectrum
- Fiber optic uses this in SONET <br>
## Division Multiplexing
- Digital Multiplexing
- Divides the time frame into slots
  - A slot is given for each message or data to be sent
TDM has two main types that are employed
- Synchronous TDM -> incoming assigns a fixed time slot for every device that is connected, regardless of whether the device is sending any data or not. <br>
- Asynch. TDM -> The slots are not fixed, and the slots are only given out when the device connected is actually sending data. <br>
## Wan Circuits
Circuits are used to connect WANs together, or connect devices within a WAN <br>
- For example if a university has smaller campuses in other states they can all be connected through one WAN so they stay on the same network. <br>
The following are Types of WAN Circuits:
- Point-Point
- Point-Multipoint
- Multipoint-Multipoint
- Metro Ethernet
- Circuit Switching
- Packet Switching
## Point-Point
Point-Point: <br>
- As the name implies, you have two points that are directly connected (simplest type of WAN connection) <br>
- On the WAN side, point-point connections are typically router-router (bridging two networks) <br>
## Point-Multipoint
Point-Multipoint: <br>
- Each site has an individual link to the central hub
- Forwarding functions are similar to a Star Topology <br>
## Multipoint-Multipoint
No central Hub - Each site has a dedicated connection to each other <br>
- Functions similarly to a Full Mesh Topology <br>
## Metro Ethernet
- Widely seen in metropolitan areas <br>
- Usually seen connecting multiple sites within a MAN environment (such as a campus to an ISP)<br>
## Circuit Switching & Packet Switching
Circuit Switching <br>
- A circuit is established between the source and destination prior to the data transfer
- Once circuit established, all of the traffic transfers along the cleared route
- When comm is complete, circuit no longer exists <br>
Packet Switching <br>
- Fragmentation occurs for data transfer
- Defragmentation occurs at the destination (the layer 3 header for each packet has a sequence number, which makes sure all packets arrive in the correct order) <br>
## WAN Protocols
Wans are data comm networks that cover a relatively broad geographic area
