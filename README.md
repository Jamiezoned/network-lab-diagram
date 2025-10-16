# 🌐 Network Lab – VLAN & AD Environment

**Goal:** Demonstrate a basic two-VLAN topology with Windows AD, routing, and client separation.  
Built as a visual reference for IT infrastructure and field deployment understanding.

---

## 🧩 Overview
A small, controlled lab showing:
- Two VLANs (clients + servers)
- Router performing inter-VLAN routing
- AD/DC server providing authentication and DNS
- Clients joined to the `lab.local` domain
- DHCP scopes per VLAN

---

## 🗺️ Topology Diagram
[Router]
│ (Trunk, VLAN 10+20)
[Switch]
├─ VLAN 10 → [PC1] [PC2]
└─ VLAN 20 → [SRV-DC01]

Router:
• VLAN10 GW: 192.168.10.1
• VLAN20 GW: 192.168.20.1

SRV-DC01:
• IP: 192.168.20.10
• Role: AD/DC + DNS
• Domain: lab.local

PC1 / PC2:
• DHCP from VLAN10 scope
• DNS → 192.168.20.10
• Joined to lab.local

yaml
Kopiera kod

---

## 💾 Addressing Plan
| VLAN | Purpose | Subnet | Gateway | DNS | Notes |
|------|----------|---------|----------|------|-------|
| 10 | Clients | 192.168.10.0/24 | 192.168.10.1 | 192.168.20.10 | PC1, PC2 |
| 20 | Servers | 192.168.20.0/24 | 192.168.20.1 | self | SRV-DC01 |

---

## 🧠 Key Learning Points
- Understands VLAN tagging (802.1Q) and trunk/access ports  
- Demonstrates DNS/AD integration between VLANs  
- Shows routing fundamentals for small business or field IT setups  
- Visualizes AD/DC role in multi-subnet networks  

---

## 🧰 Recommended Tools
- **Draw.io / Excalidraw** – diagram creation  
- **Packet Tracer / GNS3** – optional lab simulation  
- **Wireshark** – for verifying tagged traffic  

---

## 📸 Files (suggested)
network-lab-diagram/
├─ diagrams/
│ ├─ network-lab-v1.drawio
│ └─ network-lab-v1.png
└─ notes/
└─ addressing-plan.md

yaml
Kopiera kod

Add your `.drawio` file or exported PNG here once created.


## 🗓️ Project Timeline & History

- **Lab design & experiments** — Mar 2025 – Sep 2025  
  Built VLAN variants, tested inter-VLAN routing, and AD/DNS across subnets.

- **Diagram & addressing plan** — Oct 2025  
  Created draw.io topology and documented port/VLAN mapping for reproducible builds.

- **Current state** — Ongoing  
  Exporting PNGs, adding port-level notes and sample configs for interview walk-throughs.


---

## 🪪 License
MIT License – open for educational and portfolio use.
