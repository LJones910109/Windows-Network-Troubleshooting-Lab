# 🖥️ Windows Network Troubleshooting Lab

## Objective
Document and demonstrate common Windows networking commands used in 
real IT support scenarios to diagnose and resolve connectivity issues.

---

## 🛠️ Tools Used
- Windows 11
- Command Prompt (cmd)
- PowerShell
- VMware Fusion

---

## 📋 Commands & Scenarios

### 1. ipconfig
Displays the full network configuration of a Windows machine.

Command used:
ipconfig /all

Common use cases:
- Verify IP address assignment
- Check subnet mask and default gateway
- Confirm DNS server addresses
- Identify MAC address

Sample output fields:
- IPv4 Address: 192.168.1.x
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1
- DNS Servers: 8.8.8.8

---

### 2. ping
Tests connectivity between two hosts on a network.

Commands used:
- ping 192.168.1.1 (test gateway)
- ping google.com (test internet connectivity)
- ping -t 192.168.1.1 (continuous ping)

Common use cases:
- Verify host is reachable
- Test internet connectivity
- Measure latency and packet loss
- Isolate where a connection is failing

---

### 3
