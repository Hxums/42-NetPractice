# NetPractice

*This project has been created as part of the 42 curriculum by hcissoko.*

## Description
NetPractice is a systemic networking project in the 42 curriculum designed to introduce students to the fundamentals of addressing, routing, and subnetting within IP networks. 

The primary goal of this project is to solve a series of interactive networking puzzles by configuring various network interfaces, IP addresses, subnet masks, and routing tables. Through these exercises, the project covers key internetworking principles, including:
- **IPv4 Addressing & Subnetting:** Understanding network and host portions of an IP address.
- **CIDR Notation:** Master classless inter-domain routing prefixes (e.g., `/24`, `/30`).
- **Routing Tables & Default Gateways:** Configuring proper next-hop routing so packets can travel seamlessly across multiple subnets.
- **Internet connectivity (NAT):** Learning how private networks communicate with the public internet through Network Address Translation gateways.

## Instructions

### Prerequisites
Since NetPractice is a web-based training simulation provided within the 42 school ecosystem, it requires no local compilation or external compilation tools. You just need a modern web browser to run the interface.

### How to Run
1. Connect to the 42 network interface or open the offline NetPractice interface provided in your assignment directory.
2. Load the configuration files or access the level selection dashboard.
3. For each level, inspect the network diagram showing hosts, switches, routers, and internet nodes.
4. Fill in the missing network parameters (`IP Address`, `Subnet Mask`, or `Routing Table` entries) based on the constraints of the level.
5. Click the **Check** / **Run** button to simulate packet transmission and validate your network configuration.

---

## Technical Overview & Rule Summary

To solve the configuration problems, keep the following core concepts in mind:

### 1. Subnet Mask Calculation
The subnet mask defines the boundary between the network ID and the host ID. 
- A standard `/24` prefix translates to `255.255.255.0`, offering 256 addresses (254 usable for hosts).
- A point-to-point router link often uses a `/30` prefix (`255.255.255.252`), leaving only 2 usable host addresses.

### 2. Host Verification Formula
For any given host IP $A$ and another host IP $B$ to be on the same local network without a router, their network addresses must match exactly:
$$\text{Network ID} = \text{IP Address} \ \& \ \text{Subnet Mask}$$
If the result matches, they can communicate directly via a Switch. If not, a Router interface must act as a gateway.

### 3. Routing Table Rules
- **Destination:** The target network block (e.g., `192.168.1.0/24`) or `default` (`0.0.0.0/0`) for any unknown external destination.
- **Next Hop:** The IP address of the specific router interface connected to your local subnet that will forward the traffic.

---

## Resources

### Documentation & Tutorials
- [Subnet Mask Cheat Sheet](https://www.netacad.com/) - Cisco Networking Academy introduction to subnetting.
- [IP Routing Basics Explained](https://www.computernetworkingnotes.com/) - Visual guide to understanding routers, default gateways, and routing tables.
- [CIDR to Subnet Mask Conversion Table](https://www.subnet-calculator.com/) - Quick reference guide for calculating network ranges and host capacities.

### Use of AI
In compliance with the project guidelines, Artificial Intelligence (Large Language Models) was utilized in the following capacities during the development of this project:
- **Conceptual Clarification:** Used to generate interactive examples of complex routing problems involving overlapping subnets and ambiguous default paths.
- **Documentation Structure:** Assisted in organizing and proofreading this `README.md` file to comply with the official 42 requirements and formatting constraints.
- *Note:* All final puzzle validations, subnet computations, and level configurations were analyzed, calculated, and executed manually.