---
title: VPN Configuration
weight: 5
---

This section covers how VPN access is configured in the ProxHome homelab using Tailscale. Tailscale provides secure, encrypted, and authenticated remote access to internal services across the LAN and DMZ without the complexity of traditional VPNs.

### Why Tailscale?

Tailscale is a mesh VPN built on **WireGuard**, designed to simplify secure networking across devices and networks. It is ideal for homelabs because:

- **Zero-config** networking over the internet  
- **Device-level access control (ACLs)**  
- **Works through NAT/firewalls** works like a magic. No need to configure NATs to allow access, it can travel through NAT to allow access to machines
- **Supports full-tunnel VPN routing**

### ProxHome VPN Topology

- Tailscale is installed on the **Ubuntu-server VM**.
- A subnet is advertised, this enables tailscale to integrate the advertised subnet into its network. The routes advertised are **LAN** (`10.10.1.1/24`) and **DMZ** (`10.10.200.1/24`)
- After advertising the routes, enable **Exit Node**. Enable exit node so that the traffic can be proxied through the network via the Ubuntu Server with tailscale installed on it.

### Note:

- Why not install Tailscale directly on pfsense?
    - While installing Tailscale directly on pfSense may seem like an efficient approach, it poses significant security risks. In the event of a zero-day remote code execution (RCE) vulnerability in Tailscale, an attacker could potentially gain elevated privileges, modify routing tables, block network traffic, and even lock out administrative access. Avoiding direct installation helps minimize the impact of a potential supply chain compromise and protects the integrity of the entire network.