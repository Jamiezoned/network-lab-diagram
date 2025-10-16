# Addressing Plan

VLAN 10 — Clients  
- Subnet: 192.168.10.0/24  
- Gateway: 192.168.10.1  
- DHCP Scope: 192.168.10.50–192.168.10.200  
- DNS: 192.168.20.10

VLAN 20 — Servers  
- Subnet: 192.168.20.0/24  
- Gateway: 192.168.20.1  
- DC/DNS: 192.168.20.10 (SRV-DC01)

Switch Ports  
- Gi1/1 (Trunk 10,20) → Router  
- Gi1/2 (Access 20) → SRV-DC01  
- Gi1/3–4 (Access 10) → PC1, PC2
