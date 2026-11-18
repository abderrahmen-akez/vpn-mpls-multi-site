# 🌐 Redundant Multi-Site VPN-MPLS Architecture

**Academic project — Master SSIR, TEK-UP University**

Design and implementation of a **secure multi-site enterprise network** under GNS3:
redundant gateways, link aggregation, inter-VLAN routing, MPLS VPN tunnels,
centralized AAA authentication and SNMPv3 supervision.

> ⚠️ Lab project built entirely in GNS3. No production equipment involved.

## 🖼️ Topology

*(add `topology/topology.png` — full GNS3 topology export)*

- **3 sites** interconnected via an MPLS core (ISP)
- Cisco 7200 routers as PE/P routers, IOU L2/L3 switches at each site
- VLANs **210, 215, 220, 300** with inter-VLAN routing

## ✨ What was implemented

- 🔁 **First-hop redundancy** — HSRP/VRRP on site gateways
- 🔗 **Link aggregation** — EtherChannel between distribution and access layers
- 🚇 **WAN** — VPN tunnels over an **MPLS** backbone (site-to-site connectivity)
- 🔐 **Security** — AAA/RADIUS centralized authentication, ACLs, segmentation
- 📡 **Supervision** — SNMPv3 polling + traps, IP SLA tracking

## 🧰 Requirements

- GNS3 (recommended ≥ 2.2)
- Cisco IOS images: c7200 (PE), IOU L2/L3 images for switching
- ~4 GB RAM allocated to the lab

## 📁 Repository structure

```
vpn-mpls-multi-site/
├── configs/       # running-config of each router/switch (.cfg, named per device)
├── topology/      # GNS3 project export + topology diagram
├── screenshots/   # proof: ping tests, HSRP failover, VPN tunnels up, AAA logs
└── README.md
```

## ✅ Validation performed

*(add screenshots for each test)*

- [ ] Inter-VLAN routing across all VLANs
- [ ] HSRP/VRRP failover (gateway shutdown → traffic keeps flowing)
- [ ] EtherChannel up (LACP/PAgP)
- [ ] MPLS VPN tunnels established between all sites
- [ ] AAA authentication via RADIUS server
- [ ] SNMPv3 polling/traps received by the monitoring station

## 👤 Author

**Abderrahmen Akkez** — engineering student, Information Systems & Network Security (SSIR)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abderrahmen-akkez)
