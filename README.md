# Small Business Network Lab for "Prestridge Woodworking HQ"

## 1. Project Objective
The goal of this project is to design and configure a secure and segmented network for a hypothetical small business. This lab demonstrates fundamental networking concepts including VLANs, inter-VLAN routing, DHCP services, and security using Access Control Lists (ACLs).

## 2. Network Topology
*A screenshot of the final Packet Tracer topology will be inserted here.*

## 3. IP Addressing Scheme & VLAN Table
The network uses the `192.168.0.0` block, segmented into the following VLANs:

| VLAN ID | Name        | Network Address     | Gateway             | Purpose                                  |
|---------|-------------|---------------------|---------------------|------------------------------------------|
| 10      | Management  | `192.168.10.0/24`   | `192.168.10.1`      | PCs for managers, access to all areas.   |
| 20      | Sales       | `192.168.20.0/24`   | `192.168.20.1`      | PCs for sales staff.                     |
| 30      | Guest WiFi  | `192.168.30.0/24`   | `192.168.30.1`      | Laptops for guests, internet-only access.|
| 99      | Server Farm | `192.168.99.0/24`   | `192.168.99.1`      | Houses internal servers.                 |

## 4. Security Policies
The following rules will be enforced using Access Control Lists (ACLs):
- **Management (VLAN 10):** Can access all other VLANs.
- **Sales (VLAN 20):** Can access the Server Farm, but is **BLOCKED** from accessing the Management VLAN.
- **Guest WiFi (VLAN 30):** Is **BLOCKED** from accessing any internal VLAN (Management, Sales, Servers).

*Configuration details and lessons learned will be added below upon completion.*
