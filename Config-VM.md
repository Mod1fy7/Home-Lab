#  Setting Up the Virtual Machines
## You can make the specifics different, this is just a general guideline  


### 🪟 **Windows 10 (Client Machine)**

Used to simulate a domain-joined workstation for vulnerability scans, attacks, and log collection.

| Setting | Recommended Value |
| --- | --- |
| CPUs | 2 vCPUs |
| RAM | 4 GB |
| Disk Space | 50 GB (dynamic OK) |
| Network | Internal Network + NAT |
| Notes | Install VirtualBox Guest Additions for smooth UI |

---

### 🧱 **Windows Server 2022 (Domain Controller + DNS + DHCP)**

Used to create a realistic enterprise environment with Active Directory.

| Setting | Recommended Value |
| --- | --- |
| CPUs | 2 vCPUs |
| RAM | 4–6 GB |
| Disk Space | 60–80 GB |
| Network | Internal Network only |
| Notes | Promote to domain controller + set static IP |

---

### 🐧 **Ubuntu Server 22.04 LTS (SIEM / Log Collector / Web Server)**

Used for installing ELK Stack, Wazuh, or a mock website to attack.

| Setting | Recommended Value |
| --- | --- |
| CPUs | 2 vCPUs |
| RAM | 2–4 GB (4 GB if using ELK) |
| Disk Space | 40–60 GB |
| Network | Internal Network + NAT |
| Notes | Use OpenSSH for remote terminal access |

---

### 🔥 **Optional: Kali Linux (Attacker)**

Used to run Nmap scans, password attacks, exploit testing.

| Setting | Recommended Value |
| --- | --- |
| CPUs | 2 vCPUs |
| RAM | 2–4 GB |
| Disk Space | 40 GB (dynamic is fine) |
| Network | Internal Network only |
| Notes | Keep snapshots before tests |

---

### 🌐 **pfSense (Firewall/Router)**

Used to route traffic between NAT and Internal Network.

| Setting | Recommended Value |
| --- | --- |
| CPUs | 1–2 vCPUs |
| RAM | 512 MB – 1 GB |
| Disk Space | 10 GB |
| Network | 2 adapters: |
