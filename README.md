# CCNA Networking Labs & Configuration Portfolio

Welcome to my Cisco Certified Network Associate (CCNA) hands-on lab repository. This repository documents my practical experience building, configuring, and troubleshooting network topologies using Cisco Packet Tracer and Cisco IOS syntax.

## 🎯 Project Objectives
- Demonstrate proficiency in Cisco IOS CLI syntax and core networking concepts.
- Document step-by-step configurations for switching, routing, and network security.
- Maintain a clean codebase of baseline device configurations for quick deployment.

## 📂 Laboratory Breakdown

### Phase 1: Fundamental Device Setup
| Lab Topic | Key Technologies / Commands | Configuration Files |
| :--- | :--- | :--- |
| **Switch Initial Setup** | Hostname, BANNER, Enable Secret, SSH v2 | [View Config](./01-basic-fundamentals/01-switch-initial-config/) |
| **Router Interface Setup** | IPv4/IPv6 addressing, `no shutdown`, descriptions | [View Config](./01-basic-fundamentals/02-router-interface-setup/) |
| **SSH Management** | `crypto key generate rsa`, line vty, local AAA | [View Config](./01-basic-fundamentals/03-ssh-security-hardening/) |

### Phase 2: Switching & Core Routing
| Lab Topic | Key Technologies / Commands | Configuration Files |
| :--- | :--- | :--- |
| **VLANs & Trunking** | 802.1Q, Trunking, Native VLAN | [View Config](./02-intermediate-switching-routing/01-vlan-and-trunking/) |
| **Inter-VLAN Routing** | Router-on-a-Stick, Subinterfaces, SVI | [View Config](./02-intermediate-switching-routing/02-inter-vlan-routing-router-on-a-stick/) |
| **Static Routing** | Default routes (`0.0.0.0/0`), Floating static routes | [View Config](./02-intermediate-switching-routing/04-static-routing-and-default-routes/) |

### Phase 3: Dynamic Routing & Security
| Lab Topic | Key Technologies / Commands | Configuration Files |
| :--- | :--- | :--- |
| **Single-Area OSPFv2** | Router ID, Passive Interfaces, Network Statements | [View Config](./03-advanced-networking-security/01-single-area-ospfv2/) |
| **Access Control Lists** | Standard & Extended ACLs, Interface Binding | [View Config](./03-advanced-networking-security/02-standard-extended-acls/) |
| **NAT & PAT** | Inside/Outside interfaces, `ip nat inside source` | [View Config](./03-advanced-networking-security/03-nat-pat-configuration/) |
| **Port Security** | Switchport security, Sticky MACs, Err-disabled | [View Config](./03-advanced-networking-security/04-port-security-dhcp-snooping/) |

## 🛠️ Tools & Environments Used
- **Cisco Packet Tracer** (Topology simulation & packet analysis)
- **Cisco IOS Software** (Router & Switch CLI)
- **Git / GitHub** (Version control & documentation)
