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

### 3. tracert
Traces the route packets take to reach a destination.

Command used:
tracert google.com

Common use cases:
- Identify where network traffic is being dropped
- Diagnose slow connections
- Map the path between two hosts
- Identify routing issues

---

### 4. netstat
Displays active network connections and listening ports.

Commands used:
- netstat -an (show all connections)
- netstat -b (show process using each connection)

Common use cases:
- Identify open ports on a machine
- Detect suspicious connections
- Verify services are listening on correct ports
- Troubleshoot connection refused errors

---

### 5. nslookup
Queries DNS records to resolve domain names.

Commands used:
- nslookup google.com
- nslookup 8.8.8.8 (reverse lookup)

Common use cases:
- Verify DNS resolution is working
- Troubleshoot website not loading issues
- Check which DNS server is being used
- Resolve domain to IP address

---

### 6. arp -a
Displays the ARP cache showing IP to MAC address mappings.

Command used:
arp -a

Common use cases:
- Identify devices on local network
- Troubleshoot layer 2 connectivity issues
- Detect ARP spoofing attempts
- Verify network device communication

---

### 7. netsh
Advanced network configuration and troubleshooting tool.

Commands used:
- netsh interface ip show config (show IP config)
- netsh wlan show profiles (show saved WiFi networks)
- netsh int ip reset (reset TCP/IP stack)

Common use cases:
- Reset network settings when other fixes fail
- View and manage wireless profiles
- Configure network interfaces
- Diagnose advanced connectivity issues

---

## 🔧 Common IT Support Scenarios

### Scenario 1 — User Cannot Connect to Internet
Troubleshooting steps:
1. ipconfig /all — verify IP address is assigned
2. ping 192.168.1.1 — test gateway connectivity
3. ping 8.8.8.8 — test internet connectivity by IP
4. ping google.com — test DNS resolution
5. nslookup google.com — verify DNS is working
6. tracert google.com — identify where connection fails

---

### Scenario 2 — User Cannot Reach Network Share
Troubleshooting steps:
1. ping [server IP] — verify server is reachable
2. netstat -an — check if port 445 is open
3. arp -a — verify server MAC is in ARP cache
4. nslookup [server name] — verify DNS resolves server

---

### Scenario 3 — Slow Network Performance
Troubleshooting steps:
1. ping -t [gateway] — check for packet loss
2. tracert [destination] — identify slow hops
3. netstat -an — check for excessive connections
4. ipconfig /all — verify correct DNS servers

---

## 🧠 What I Learned
- How to systematically diagnose network connectivity issues
- The difference between Layer 3 (IP) and Layer 7 (DNS) problems
- How to use built-in Windows tools without third party software
- Real IT support troubleshooting methodology

---

## ⚠️ Disclaimer
All commands were run in a controlled lab environment using VMware Fusion 
with Windows 11. Screenshots of actual command output will be added as 
labs are completed.
