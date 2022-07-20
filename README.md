# Campus-network

In this repo I will explain how we can build a campus network design and also how to implement it.

## Requirements
* Scalable
* Redundant
* Fast

## Design
First we need to think for how many people we will design the network. In this case it's arround 600.
Important to know is that for our private address range we will use a lot more IP addresses than are needed due to the fact that it's than easier to manage if we have a sudden growth in network users.

### Subnet
A subnet is required for any network design.
We will be using VLAN's because it is easier to manage, improves security...
If you don't want to create the subnet by hand you can always use a calculator: https://www.subnet-calculator.com/


Our subnet:
* VLAN4: LEERLINGEN (700 hosts) /22 = 192.168.0.1 - 192.168.3.254
* VLAN3: LEERKRACHTEN (100 hosts) /25 = 192.168.4.1 - 192.168.4.126
* VLAN2: GUEST (100 hosts) /25 = 192.168.4.129 - 192.168.4.254
* VLAN1: MANAGEMENT (30 hosts) /27 = 192.168.5.1 - 192.168.5.30
* VLAN5: SERVERS (30 hosts) /27 = 192.168.5.33 - 192.168.5.62
