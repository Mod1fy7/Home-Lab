---

# 🌐 General Guide: Setting IPs & VLANs

---

## 1️⃣ Decide Your Networks

* Pick a subnet for each group (VLAN). Example:

  * VLAN 10 → `192.168.10.0/24`
  * VLAN 20 → `192.168.20.0/24`

Each VLAN needs its own range of IPs.

---

## 2️⃣ Assign Gateways

* Every subnet has a **gateway** (usually the router/firewall). Example:

  * VLAN 10 gateway = `192.168.10.1`
  * VLAN 20 gateway = `192.168.20.1`

---

## 3️⃣ Give Devices IPs

* Each device in a VLAN must:

  1. Have a **unique IP** in that subnet.
  2. Use the subnet’s **gateway**.

Examples:

* Device A in VLAN 10 → IP `192.168.10.11`, gateway `192.168.10.1`
* Device B in VLAN 10 → IP `192.168.10.12`, gateway `192.168.10.1`
* Device C in VLAN 20 → IP `192.168.20.21`, gateway `192.168.20.1`

---

## 4️⃣ Connectivity Rules

* Devices in the **same subnet** (same VLAN) can talk to each other directly.
* Devices in **different subnets** (different VLANs) need a router/firewall to talk across.

---

✅ That’s it — the general recipe:

1. Pick subnets.
2. Assign gateways.
3. Give devices IPs in the right range.
4. Same subnet = direct talk, different subnets = router needed.

---

