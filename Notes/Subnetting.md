# 🧮 Subnetting & NAT Cheat Sheet

## 🧩 Subnetting & CIDR (Classless Inter-Domain Routing)

**Subnetting** breaks a network into smaller, manageable pieces (subnets).  
**CIDR** notation (e.g., `192.168.1.0/24`) specifies:
- IP address: `192.168.1.0`
- Prefix length: `/24` → first 24 bits = network portion

🔢 Example:
192.168.1.0/24 = 255.255.255.0

🧠 Formula:
- **IPs = 2^(32 - CIDR)** → Total IPs in the subnet

💡 Example:
- `/24` → 32 - 24 = 8 → `2^8 = 256 IPs` (254 usable)

---

## 💡 Binary: 1s and 0s

Understanding IPs and subnet masks in **binary** helps with calculations.

| Decimal | Binary            |
|---------|--------------------|
| 192     | 11000000           |
| 255     | 11111111           |
| 0       | 00000000           |

🧠 IP address: `192.168.1.1`  
🧠 Subnet mask `/24`: `255.255.255.0` → `11111111.11111111.11111111.00000000`

---

## 🔢 Calculating Subnets

To create **subnets**, borrow bits from the host portion of the IP.

| Subnet Bits | /CIDR | # of Subnets | Hosts per Subnet |
|-------------|--------|--------------|------------------|
| 1           | /25    | 2            | 126              |
| 2           | /26    | 4            | 62               |
| 3           | /27    | 8            | 30               |
| 4           | /28    | 16           | 14               |

📝 Formula:
- **Hosts/subnet** = 2^host_bits - 2  
- **Subnets** = 2^borrowed_bits

---

## 🌍 NAT (Network Address Translation)

**NAT** maps **private IPs ↔ public IPs**, allowing multiple internal devices to access the internet using one public IP.

### 🛠️ Types of NAT:
- **Static NAT** – one-to-one mapping
- **Dynamic NAT** – pool of public IPs
- **PAT (Port Address Translation)** – many-to-one (most common)

### 🔒 Common Private IP Ranges:
- `10.0.0.0/8`
- `172.16.0.0/12`
- `192.168.0.0/16`

NAT happens on your **router or firewall**, essential in cloud VPCs and home networks.

---

📌 Tip: Use tools like `ipcalc` or `subnet-calculator.com` to verify subnet ranges quickly.
