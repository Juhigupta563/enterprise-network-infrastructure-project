# Enterprise Network Infrastructure Design, Configuration & Monitoring

**A practical enterprise networking project using Cisco Packet Tracer and Wireshark.**

## Project Overview

Designed, implemented, secured, and tested a multi-department enterprise network connecting Human Resources (HR), Information Technology (IT), and Finance through a centralized network architecture.

The project demonstrates VLAN-based segmentation, inter-VLAN routing, network services, access control, NAT/PAT, secure device management, and packet-level protocol analysis.

## Network Architecture

The enterprise network consists of:

- R1-ENTERPRISE – Main enterprise router
- SW1-CORE – Central Layer 2 switch
- R2-ISP – ISP router
- SW2-ISP – External network switch
- HR, IT, and Finance departmental computers
- Internal DNS and web server
- External web server

## Technologies & Tools

| Technology          | Application                          |
|---------------------|--------------------------------------|
| Cisco Packet Tracer | Network design and simulation        |
| Cisco IOS CLI       | Router and switch configuration      |
| VLAN                | Departmental network segmentation    |
| IEEE 802.1Q         | VLAN trunking                        |
| DHCP                | Dynamic IP allocation                |
| DNS                 | Internal hostname resolution         |
| Static Routing      | Enterprise-to-ISP connectivity       |
| NAT/PAT             | External network access              |
| Extended ACLs       | Traffic filtering                    |
| SSH v2              | Secure remote administration         |
| Port Security       | MAC-based access control             |
| Wireshark           | Packet capture and protocol analysis |

## VLAN and IP Addressing

| VLAN | Department   | Network         | Gateway      |
|------|--------------|-----------------|--------------|
| 10   | HR           | 192.168.10.0/24 | 192.168.10.1 |
| 20   | IT           | 192.168.20.0/24 | 192.168.20.1 |
| 30   | Finance      | 192.168.30.0/24 | 192.168.30.1 |
| 40   | Servers      | 192.168.40.0/24 | 192.168.40.1 |
| 999  | Unused Ports | No IP subnet    | N/A          |

## Key Implementations

- Router-on-a-stick inter-VLAN routing.
- DHCP services for departmental computers.
- Internal DNS resolution using `www.enterprise.local`.
- Static routing between enterprise and ISP routers.
- NAT/PAT overload for external connectivity.
- Extended ACLs for HR and Finance traffic restrictions.
- SSH version 2 with local authentication.
- Sticky MAC port security with shutdown violation mode.
- VLAN 999 isolation and shutdown of unused switch ports.

## Testing and Validation

The following tests were performed:

- VLAN and default gateway connectivity.
- Inter-VLAN communication.
- ACL-based traffic restriction.
- DHCP and DNS verification.
- Internal and external web connectivity.
- NAT translation verification.
- SSH remote access.
- Switch port-security violation testing.
- WAN failure and recovery testing.
- Wireshark protocol analysis.

## Wireshark Analysis

Captured and analyzed:

- ICMP – Echo request and reply.
- TCP – Transport-layer communication.
- DNS – Query and response packets.
- HTTP – GET request and HTTP response.
- HTTPS – TLS 1.3 encrypted application data.

**Note:** Wireshark captures were collected from the host laptop's Wi-Fi interface, separately from the Packet Tracer simulation.

## Project Structure

```text
enterprise-network-infrastructure-project/
│
├── 01_Packet_Tracer/
├── 02_Network_Diagrams/
├── 03_Device_Configurations/
├── 04_Wireshark_Analysis/
├── 05_Testing_Results/
├── 06_Documentation/
└── README.md
```

## Learning Outcomes

- Enterprise network architecture and topology design.
- Cisco router and switch configuration.
- IPv4 addressing and subnetting.
- Network segmentation and security.
- Routing, NAT/PAT, and network services.
- Network troubleshooting and validation.
- Packet inspection using Wireshark.

## Future Enhancements

- OSPF dynamic routing.
- Network redundancy and high availability.
- Centralized monitoring and logging.
- Dedicated management VLAN.
- More granular least-privilege ACL policies.

---

**Project Domain:** Computer Networking | Network Engineering | Network Security

**Tools:** Cisco Packet Tracer | Cisco IOS | Wireshark

\- Strengthen least-privilege ACL policies.

\- Add a dedicated firewall and DMZ architecture.

