Router-on-a-Stick VLAN Network Project
This project demonstrates a **Router-on-a-Stick** configuration using VLANs to segment traffic across multiple departments in a simulated enterprise network environment.
The setup was tested using Cisco IOS devices in a packet tracer or GNS3 simulation.

Project Overview
- **Topology:**
  - 1 Router (with subinterfaces configured for inter-VLAN routing)
  - 2 Switches (trunked and with access ports assigned to specific VLANs)
  - Multiple PCs grouped by department (Admin, HR, Finance, IT)

- **VLANs Used:**
  - VLAN 10 – Admin
  - VLAN 20 – HR
  - VLAN 30 – Finance
  - VLAN 40 – IT

Configuration
- **Router Subinterfaces:**
  - `Gig0/1.10` – `192.168.10.1/24`
  - `Gig0/1.20` – `192.168.20.1/24`
  - `Gig0/1.30` – `192.168.30.1/24`
  - `Gig0/1.40` – `192.168.40.1/24`

- **Trunk Links:**
  - Between Router and Switch1: `Gig0/1`
  - Between Switch1 and Switch2: `Gig0/1`

- **Access Ports**
  - Each PC is connected to a FastEthernet port on either Switch1 or Switch2 and assigned to the corresponding VLAN.
  - Both switches are connected to the router via GigabitEthernet

Features
- Inter-VLAN routing using router subinterfaces
- Full communication between PCs in different VLANs via the router
- VLAN segmentation for better network security and efficiency
- Tested successful ICMP connectivity using `ping`

Files Included
- `.pkt` (Packet Tracer file) & 2 network configuration .txt (text)files
- This `README.md`

Skills Practiced
- VLAN creation and assignment
- Trunk port configuration
- Subinterface configuration on a router
- Basic troubleshooting with `ping`, `show`, and `interface` commands

side notes
- Make sure trunk ports are properly configured on switches.
- Use `show vlan brief`, `show interfaces trunk`, and `show ip interface brief` to verify setup.
- Subnet IPs must match the VLAN and device configuration.
