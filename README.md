\# **Enterprise Network Infrastructure – Cisco Packet Tracer**



\## 1. Project Overview



Designed and implemented an enterprise network infrastructure using Cisco Packet Tracer to connect multiple departments through a centralized network architecture.



The network provides departmental segmentation, inter-VLAN routing, controlled communication using Access Control Lists (ACLs), DNS resolution, external web access and Network Address Translation (NAT/PAT).



\## 2. Technologies Used



\- Cisco Packet Tracer

\- Cisco IOS CLI

\- VLAN and IEEE 802.1Q

\- Router-on-a-Stick

\- Inter-VLAN Routing

\- DHCP and DNS

\- Extended Access Control Lists (ACLs)

\- NAT/PAT (Overload)

\- Port Security

\- Network Troubleshooting



\## 3. Network Architecture



The enterprise network consists of:



\- R1-ENTERPRISE: Enterprise gateway router

\- R2-ISP: ISP router

\- SW1-CORE: Central network switch

\- SW2-ISP: ISP-side switch

\- HR Department

\- IT Department

\- Finance Department

\- Internal DNS/Web server

\- External web server



\## 4. VLAN and IP Addressing Plan



| Department | VLAN | Network         | Gateway      |

|------------|-----:|-----------------|--------------|

| HR         | 10   | 192.168.10.0/24 | 192.168.10.1 |

| IT         | 20   | 192.168.20.0/24 | 192.168.20.1 |

| Finance    | 30   | 192.168.30.0/24 | 192.168.30.1 |

| Servers    | 40   | 192.168.40.0/24 | 192.168.40.1 |

|Unused Ports| 999  | Isolated VLAN   | N/A          |



\## 5. Routing and Connectivity



Implemented Router-on-a-Stick architecture using IEEE 802.1Q subinterfaces on the enterprise router.



Configured:

\- Inter-VLAN routing

\- Default route towards ISP

\- External network connectivity

\- Departmental gateway configuration



\## 6. Network Security



Implemented extended ACLs:



\- HR-SECURITY

\- IT-SECURITY

\- FINANCE-SECURITY



Security features include:

\- Departmental traffic restrictions

\- Controlled DNS and HTTP access

\- ICMP filtering

\- TCP established traffic handling

\- Unused switch port isolation

\- Port security with maximum MAC address limits



IT currently has unrestricted routing access according to its ACL policy.



\## 7. NAT/PAT Implementation



Configured dynamic NAT overload on the enterprise router.



\- Inside interfaces: Departmental VLAN subinterfaces

\- Outside interface: GigabitEthernet0/0

\- Public-facing enterprise address: 203.0.113.1



Verified translations using:



show ip nat translations



show ip nat statistics



\## 8. Testing and Validation



Performed the following tests:



| Test                              | Result                     |

|-----------------------------------|----------------------------|

| Departmental gateway connectivity | Successful                 |

| Inter-VLAN routing                | Successful where permitted |

| HR-to-Finance isolation           | Verified                   |

| Finance-to-HR isolation           | Verified                   |

| Finance-to-IT isolation           | Verified                   |

| DNS resolution                    | Successful                 |

| External server ping              | Successful                 |

| HTTP access                       | Successful                 |

| NAT/PAT translation               | Verified                   |

| Switch VLAN configuration         | Verified                   |

| Trunk configuration               | Verified                   |

| Port security                     | Verified                   |



\## 9. Project Outcome



Successfully implemented a segmented enterprise network with centralized routing, departmental access controls, internal DNS services and external web connectivity.



The project demonstrates practical knowledge of enterprise networking, Cisco IOS configuration, network security and troubleshooting.



\## 10. Future Enhancements



\- Implement redundant gateway architecture using HSRP.

\- Introduce dynamic routing using OSPF.

\- Implement centralized network monitoring.

\- Strengthen least-privilege ACL policies.

\- Add a dedicated firewall and DMZ architecture.

