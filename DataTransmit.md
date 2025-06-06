# Data Transmission Methods & Signaling
## Baseband Vs Broadband
Baseband - Uses only a single fixed digital frequency to send a signal that occupies the cable's entire carrying capacity or bandwidth. <br>
- Only one device can transmit at a time <br>
Broadband - Carries multiple analog channels on a single cable, where one channel is required to send and another channel to receive <br>
- Allows multiple devices to transmit and receive simultaneously <br>
Digital: Carries data in digital form using on/off (Binary) values of electrical voltage, current, or light. <br>
Analog: Uses a continuously varying waveform to carry data. Radio frequencies (RF), sound & music are all analog signals. <br>
## Digital Telecom Convergence
Digital telecom convergence is the combination, integration, and evolution of voice, data, video, pictures, music, and other content of features. <br>
As technology evolves, legacy systems are either integrated into hybrid systems or phased out entirely. <br>
## Public Switched Telephone Network (PSTN)
PSTN - The world's collection of voice-oriented public telephone networks. <br>
The fixed-line analog telephone system, originally called Plain Old Telephone Service (POTS), is now almost entirely digital and integrates mobile phones with landlines. <br>
- Composed of telephone exchanges networked together to form a worldwide communications system where calls are switched through a network of copper and fiber optic cabling <br>
The internet shares the same infrastructure as the PSTN for intercontinental communication. During the expansion of the internet <br>
an architecture was needed for long distance comms. Instead of creating an entirely new infrastructure, the PSTN was adapted to handle internet traffic. <br>
Data rates for early PSTN modems topped out around 56 kbps. <br>
## Network Carrier Standards
![image](https://github.com/user-attachments/assets/130e5f46-904b-4b4e-89a1-832866f90a69)
Signal level DS-0 (Standard PSTN phone line) can carry exactly one phone call or voice channel. <br>
## Digital Subscriber Line
Digital Subscriber Line (DSL) - Is a modulation scheme to pack data onto copper lines or existing infrastructure (PSTN). <br>
DSL is a subscription service designed to bring the internet to homes and businesses and is offered in three types of service configurations <br>
- Asymmetrical DSL (ADSL) -> Residential Consumer version of DSL & Allows for faster downstream data rates than upstream rates (8Mbps Download, 800 Kbps Upload)
- Symmetric DSL (SDSL) -> Business oriented version (more expensive) & Supports same data rates for upstream and downstream transfers (10Mbps Download, 10Mbps Upload)
- Very High Bitrate DSL (VDSL) - Today's replacement for ADSL and SDSL. Runs fiber lines to neighborhoods for faster data. <br>
Can provide speeds between 100 Mbps (Symmetric) and 300 Mbps (Asymmetric) <br>
## Asynchronous Transfer Mode
ATM is a high speed network technology designed for use on both LANs and WANs <br>
- Primary choice as a WAN backbone for long-haul, high-bandwidth needs over the PSTN.
- Allows multiple types of traffic (voice, video, and data) to transmit between networks.
- ATM Bandwidth is measured and rated in terms of an OC level
- ATM connected networks together, while DSL handled each network's individual Voice/Data connections.
- ATM is connection-oriented and uses a dedicated circuit between switches. ATM circuits can either be Permanent or Switched <br>
  - Permanent -> Dedicated connections preconfigured by your ISP
  - Switched -> Per-call basis that disconnects when the call is terminated. <br>
## Synchronous Optical Network (SONET)
Synchronous Optical Network (SONET) is a high-speed digital networking standard that specifies data rates over fiber-optic connections. SONET uses baseband <br>
providing for synchronous comms. The signaling rates for both SONET and ATM are identical, and measured in terms of OC <br>
1) A multiplexer converts multiple signals into one multiplexed optical signal -> it is then sent over Fiber Optic cables.
2) The re-generator boosts the strength, allowing it to transmit further.
3) At the other end, the demultiplexer converts the multiplexed optical signal back into the individual signals. <br>
Because of the bandwidth capacity of SONET, it is partnered with ATM where ATM is the underlying signal technology and SONET is the overlying comms standard. <br>
Together, ATM and SONET provide for a high-bandwidth means of transferring a mix of info at near real-time. <br>

## Satellite Comms
Any object in an orbit is called a satellite. A satellite can be natural, like the moon, or artificial. <br>
Comm satellites receive, amplify and transmit voice, music, television, telephone, and data signals from one point on Earth to another. <br.
The area of earth a satellite signal strikes is called its "footprint" <br>
Ground stations can only communicate with a satellite when within the satellite's footprint. <br>
A satellite's orbital pattern, altitude and velocity determine its footprint <br>

## Satellite Orbits
There are five basic orbits for satellites:
- Low Earth Orbit (LEO) - Most common and smallest footprint
- Medium Earth Orbit (MEO) - Used for GPS & moderate footprint
- Highly Elliptical Orbit (HEO) - Elongated orbit, oriented for high dwell time on a large specific footprint & require 2+ satellites for consistent coverage. <br>
- Geosynchronous Orbit (GSO) - Second most common, 24 hour orbit designed to maintain a consistent footprint on the Earth, 22k mile altitude & used for comms and broadcasting <br>
- Geostationary Orbit, or Geosynchronous Equatorial Orbit (GEO) - Specific type of GSO & Occupies a fixed location above the equator. <br>
## VSAT
Very Small Aperture Terminal (VSAT) - Networking services such as data, voice, video, and fax transmissions are delivered using geostationary satellites. <br>
VSAT units can be integrated as one unit for portable applications and operate in two basic topologies: <br>
- Mesh Topology -> Comms go from the VSAT to the satellite and then directly to the destination VSAT & require one satellite hop
- Star Topology -> Satellite connection goes through a comm center or hub, then is transmitted to the destination & requires two satellite hops
VSAT operates in 3 configs: <br>
Point-point <br>
- Comms occur between 2+ ground stations and uses mesh topology
Point-multipoint <br>
- One transmitter and multiple receivers, utilizes star topology since only one ground station (usually transmits) used for TV and Radio broadcasts.
Multipoint-to-point: Multiple transmitters and one receiver acting as a hub. Star topology which tactical satellite architectures use. <br>




