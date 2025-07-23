

# Firewall and VPN Implementation Lab

## 📌 Objective  
Design and implement a secure, enterprise-grade network topology for Corporation Techs. The project includes separating network segments for departments, setting up a DMZ for public web access, selecting and placing firewalls, and creating a VPN plan to support secure remote access.

---

## 🧠 Skills Gained  
- Network topology design and segmentation (VLANs for Accounting and Sales)  
- Implementing DMZ for secure public web server hosting  
- Firewall selection and placement (Perimeter, internal, server, and workstation firewalls)  
- Configuring Next-Generation Firewall (NGFW) features  
- Planning and deploying VPNs (IPSec and SSL/TLS) for site-to-site and remote access  
- Enhancing network authentication with MFA and Active Directory  

---

## 🛠️ Tools & Technologies Used  
- Cisco Packet Tracer (Network Design)  
- pfSense (Firewall appliance)  
- Fortinet FortiGate (Internal network firewall)  
- Windows Defender Firewall (Workstations)  
- VPN protocols: IPSec, SSL/TLS  
- Active Directory & Multi-Factor Authentication (MFA)  

---

## 🖥️ Network Design Overview  

| Component               | Details                                              |
|------------------------|------------------------------------------------------|
| Servers                | 1 Web server (Linux/Apache), 2 Application servers, 2 Database servers, 2 File/Print servers (Windows Server)  |
| Workstations           | 50 Windows machines, separated into VLANs for Accounting and Sales |
| Network Segmentation   | DMZ for web server, LAN segmented with VLANs         |
| Firewalls              | Perimeter NGFW, Internal FortiGate firewalls, Host-based firewalls |
| Network Protocol       | IPv4 (planned gradual transition to IPv6)            |
| Redundancy             | Redundant links and power backups (UPS), RAID storage on servers |



---

## 🔍 Firewall Selection and Placement  

- **Perimeter Firewall:** Next-Generation Firewall (NGFW) with intrusion prevention and deep packet inspection placed between internet and internal network.  
- **Internal Firewalls:** Fortinet FortiGate to segment internal traffic between departments and protect servers.  
- **Server Firewalls:** Windows Firewall (or iptables on Linux) to restrict access on individual servers.  
- **Workstation Firewalls:** Windows Defender Firewall enabled on all workstations for local protection.  



---

## 🔒 VPN and Remote Access Plan  

- **VPN Technologies:**  
   - IPSec VPN for secure site-to-site tunnels between offices.  
   - SSL/TLS VPN for secure remote access via web browsers without special clients.  
- **Remote Desktop Services (RDS):** Recommended for remote access to internal desktops and servers.  
- **Authentication:** Multi-Factor Authentication (MFA) combined with Active Directory ensures only authorized users can access resources.  

---

## 📄 Executive Summary  

This design modernizes Corporation Techs’ network by introducing layered security, segmentation, and remote access capabilities. Using dual firewalls and a DMZ isolates public web services from internal resources, reducing attack surface. Department VLANs improve security and fault isolation. The VPN plan enables secure remote connectivity for users, supported by strong authentication mechanisms. Together, these upgrades improve network resilience, security posture, and readiness for future growth.



