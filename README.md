# Networking Project - DHCP Server on Cisco Router

This Project demonstrates how to configure a Cisco router to as a DHCP server that automatically assigns IP addresses to devies on the local network.

-- 


## Topology

  - 1 Cisco router (Acting as DHCP server)
  - 1 Cisco switch
  - 2 PCs

# Technology Used 
  - Cisco Packet Tracer
  - Cisco IOS CLI
  - DHCP (Dynamic Host Configuration Protocol)
  - IPv4 addressing
  - Default gateway setup

## Configuration Summary

  - Network Subnet: 192.168.50.0/24
  - Router IP (Default gateway): 192.168.50.1
  - DHCP Pool: 192.168.50.100 - 192.168.50.200
  - DNS Server: 8.8.8.8


Router DHCP Configuration

int g0/0
  ip address 192.168.50.1 255.255.255.0
  no shutdown

ip dhcp excluded-address 192.168.50.1

ip dhcp pool LAN
  network 192.168.50.0 255.255.255.0
  default-router 192.168.50.1
  dns-server 8.8.8.8





