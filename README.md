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
<img width="775" height="598" alt="Screenshot 2026-05-31 at 2 01 42 PM" src="https://github.com/user-attachments/assets/c44f3540-d0fe-4c20-88be-0c15309ff8da" />

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
<img width="579" height="478" alt="Screenshot 2026-05-31 at 2 02 23 PM" src="https://github.com/user-attachments/assets/75d695b0-23b8-4037-8e86-a42d8d1d7e60" />

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
<img width="571" height="615" alt="Screenshot 2026-05-31 at 2 02 44 PM" src="https://github.com/user-attachments/assets/7ab4b4c2-87c1-48a9-89e9-691278e97bc2" />
  
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
<img width="449" height="182" alt="Screenshot 2026-05-31 at 2 03 02 PM" src="https://github.com/user-attachments/assets/ced21011-7e1c-4500-ae37-8fc9d9159ddb" />


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
<img width="582" height="220" alt="Screenshot 2026-05-31 at 2 03 23 PM" src="https://github.com/user-attachments/assets/e156d60c-bac6-4293-a286-ff78a3ef19bd" />

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
<img width="677" height="354" alt="Screenshot 2026-05-31 at 2 08 27 PM" src="https://github.com/user-attachments/assets/00c56bf6-bd93-47ad-b4c6-df1bdafc0c0b" />

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
