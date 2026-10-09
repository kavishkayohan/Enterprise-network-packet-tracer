# Enterprise Network - Packet Tracer Project

3-Tier VLAN based network with Inter-VLAN Routing.

### Topology
- Core Switch: Cisco 3560 (L3)
- Access Switches: Cisco 2960 x2 (HR-IT & Finance)
- VLANs: 10 (HR-IT), 20 (Finance), 100 (Servers)

### IP Scheme
- VLAN 10: 10.10.10.0/24 - Gateway 10.10.10.1
- VLAN 20: 10.10.20.0/24 - Gateway 10.10.20.1
- VLAN 100: 10.10.100.0/24 - Gateway 10.10.100.1 / Server 10.10.100.10

### Configuration
- Core: `ip routing`, SVI interfaces, `switchport trunk encapsulation dot1q`, DHCP Pools
- Access: VLAN creation, Access ports, Trunk ports (Gi0/1)

### Testing
- HR PC (10.10.10.x) -> ping 10.10.20.1 : 0% loss - Success
- HR PC -> ping 10.10.100.10 : Success (Inter-VLAN Routing Working)




