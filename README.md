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

        ---

## Testing & Validation

Network connectivity was tested from the Ubuntu virtual machine.

The Ubuntu network configuration showed the following:

- **IPv4 address:** `192.168.2.102/24`
- **Default gateway:** `192.168.2.1`
- **Network:** `192.168.2.0/24`

Connectivity was verified using ICMP ping tests.

```bash
ip a show ens33
ip route
ping -c 4 8.8.8.8
ping -c 4 google.com
```

Both ping tests completed successfully with 0% packet loss in the recorded test session. This verified IP connectivity and DNS name resolution from the Ubuntu virtual machine at the time of testing.

## Evidence and Screenshots

The following screenshots document the configuration and testing performed in this lab.

| Screenshot | Description |
|---|---|
| [pfSense Dashboard](screenshots/Dashboard-1.png) | pfSense system information and dashboard |
| [Additional Dashboard View](screenshots/Dashboard-2.png) | Additional view of the pfSense environment |
| [Firewall Aliases](screenshots/Firewall-Aliases-IP.png) | Configured host and network aliases |
| [LAN Firewall Rules](screenshots/Firewall-Rules-LAN.png) | LAN firewall rule configuration |
| [WAN Firewall Rules](screenshots/Firewall-Rules-WAN.png) | WAN firewall rule configuration |
| [NAT Configuration](screenshots/NAT-Configurations.png) | NAT configuration evidence |
| [Ubuntu Connectivity Tests](screenshots/Ubuntu-Connectivity.png) | Ubuntu IP configuration, routing, and connectivity tests |
