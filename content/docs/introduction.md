---
title: Introduction
weight: 1
next: /docs/installation
prev: /docs
---

Welcome to my Portato setup Documentation!

## What is Portato?

Many times, you may want to instantly access your machines from any internet-enabled device. However, to securely do so, you typically need to install a VPN client that is compatible with the VPN server running inside your personal network. This setup only grants network access, after which you still need to connect to a VNC server and log in remotely to access a user interactive GUI. But what if you could skip the VPN configuration and access the GUI directly and securely over the internet? Portato is my implementation for securely accessing machines in my homelab over the internet, without the need for a VPN.

## Network Topology
![Network](/images/Portado.png)

## Configuration
{{< cards >}}
  {{< card link="/docs/hardware/" title="Hardware Configuration" icon="AMD" subtitle="Overview of the hardware powering the Homelab." >}}
  {{< card link="/docs/network/" title="Network Configuration" icon="router" subtitle="Managing virtual networks within my homelab." >}}
  {{< card link="/docs/firewall/" title="Firewall Configuration" icon="shield-check" subtitle="Securing the network using OPNsense firewall rules." >}}
  {{< card link="/docs/proxy/" title="Apache Guacamole" icon="avacado" subtitle="Enabling secure GUI access to configured instances within the homelab" >}}
  {{< card link="/docs/cloudflare/" title="Cloudflare Tunnel" icon="cloudflare" subtitle="Creating a secure tunnel to cloudflare network enabling exposing virtual instance sercurely to cloudflare services." >}}
  {{< card link="/docs/vnc/" title="TightVNCServer" icon="vnc" subtitle="Enabling remote log in to desired machines." >}}
  {{< card link="/docs/proxy/" title="Nginx-Reverse-Proxy" icon="proxy" subtitle="Directing traffic securely to configured homelab instances" >}}
{{< /cards >}}

## Features

- **Clientless Access:** No need to install any client software, access is entirely browser-based.

- **Protocol Support:** Supports RDP, VNC, and SSH for remote desktop and terminal access.

- **Web-Based Interface:** Clean, responsive UI accessible from any modern browser.

- **Centralized Management:** Manage all remote connections and user permissions from a central server.

- **Multi-User Support:** Allow multiple users with individual access controls.

- **End-to-End Encryption:** Secure connections using HTTPS and SSH encryption.

- **LDAP & SSO Integration:** Integrates with LDAP, Active Directory, and single sign-on systems.

- **Two-Factor Authentication:** Supports 2FA via TOTP and extensions.

- **Session Recording:** Optional recording of user sessions for auditing or training.

- **Clipboard & File Transfer:** Copy-paste text and transfer files between client and remote system.

- **Custom Branding:** Modify the UI for organizational branding and themes.

- **Extensible via Plugins:** Add custom authentication methods and features through extensions.

## Questions or Feedback?

{{< callout type="warning" >}}
  Portado is still in **active** development. Questions/Suggestions: [open an issue](https://github.com/arbaaz29/Portado/issues)
{{< /callout >}}
