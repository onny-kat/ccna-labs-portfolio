# Lab: Basic Switch and End Device Configuration

## Lab Overview & Objectives
This lab focuses on performing initial administrative setup and IP connectivity configuration on Cisco Catalyst switches (`S1` and `S2`) and end-user host devices (`PC-A` and `PC-B`) using Cisco Packet Tracer.

### Core Learning Objectives:
- Perform initial switch configurations (Hostname, Banner, Passwords).
- Configure Switch Virtual Interfaces (SVI / VLAN 1) for IP connectivity.
- Configure IPv4 parameters on end-user PCs.
- Verify network layer connectivity across devices using ICMP (`ping`).
- Save active running configurations to non-volatile memory (NVRAM).

---

## Addressing Table

| Device | Interface | IP Address | Subnet Mask |
| :--- | :--- | :--- | :--- |
| **S1** | VLAN 1 | `192.168.1.1` | `255.255.255.0` |
| **S2** | VLAN 1 | `192.168.1.2` | `255.255.255.0` |
| **PC-A** | NIC | `192.168.1.10` | `255.255.255.0` |
| **PC-B** | NIC | `192.168.1.11` | `255.255.255.0` |

---

## Configuration Steps

### 1. Initial Device Identity & Hardening (S1 & S2)
Secured administrative access and configured device identification:

```cisco
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1
S1(config)# enable secret cisco
S1(config)# line console 0
S1(config-line)# password password
S1(config-line)# login
S1(config-line)# exit
S1(config)# banner motd # AUTHORIZED ACCESS ONLY #
