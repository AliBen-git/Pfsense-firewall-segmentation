# pfSense Firewall & Network Security Lab

## Project Overview

This project documents a hands-on pfSense firewall lab implemented in a virtualized VMware environment.

The project focuses on practical network security and firewall administration, including firewall rule processing, LAN/WAN traffic control, aliases, NAT, traffic analysis, logging, troubleshooting, and connectivity testing.

The lab was completed using pfSense Community Edition and Ubuntu Linux virtual machines.

---

## Objectives

The main objectives of the project were to:

- Deploy pfSense as a virtual firewall.
- Configure and validate network connectivity.
- Understand how the pfSense firewall rule engine processes traffic.
- Create and test LAN and WAN firewall rules.
- Use aliases to structure firewall policies.
- Configure NAT and port forwarding.
- Analyze firewall logs and network traffic.
- Troubleshoot allowed and blocked traffic.
- Validate the final configuration through practical testing.

---

## Lab Environment

| Component | Technology |
|---|---|
| Firewall | pfSense Community Edition |
| Virtualization | VMware Workstation |
| Client | Ubuntu Linux |
| Network | IPv4 |
| Firewall Management | pfSense Web GUI |
| Testing | Linux networking tools |

---

## Network Architecture

The lab uses pfSense as the central firewall between the external network and internal virtual machines.


                    Internet
                       |
                       |
                +------+------+
                |   pfSense   |
                |   Firewall  |
                +------+------+
                       |
                  Internal LAN
                       |
              +--------+--------+
              |                 |
        +-----+-----+     +-----+-----+
        | Ubuntu VM |     | Internal  |
        |   Client  |     |  Server   |
        +-----------+     +-----------+
