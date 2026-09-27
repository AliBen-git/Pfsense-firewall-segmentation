# pfSense Firewall Segmentation

## Project Overview

This project documents the design and implementation of a pfSense-based firewall lab environment.

The purpose of the project is to demonstrate practical skills in network security, firewall configuration, IP addressing, network policy design, aliases, and connectivity testing.

The lab was implemented using virtual machines and includes pfSense as the firewall and Ubuntu as a connected client system.

## Objectives

- Deploy pfSense as a virtual firewall.
- Configure network interfaces and IP addressing.
- Connect an Ubuntu virtual machine through pfSense.
- Design structured firewall policies.
- Configure IP aliases for reusable firewall objects.
- Test network connectivity and firewall behavior.
- Document the implementation and security considerations.

## Lab Environment

| Component | Technology |
|---|---|
| Firewall | pfSense Community Edition |
| Virtualization | VMware |
| Client | Ubuntu Linux |
| Network | IPv4 |
| Firewall Management | pfSense Web GUI |
| Testing | Linux networking tools |

## Network Architecture

The lab consists of a pfSense virtual firewall and an Ubuntu virtual machine connected through the configured network.

```text
Internet
   |
   |
+----------------+
|    pfSense     |
|    Firewall    |
+-------+--------+
        |
        |
+-------v--------+
|   Ubuntu VM    |
| 192.168.2.102  |
+----------------+
