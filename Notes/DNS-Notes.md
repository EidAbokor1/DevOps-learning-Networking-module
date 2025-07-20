# 🧠 DNS (Domain Name System) Cheat Sheet

## 🌍 Introduction to DNS
DNS translates **human-friendly domain names** (like `example.com`) into **IP addresses** (`93.184.216.34`) so computers can communicate over the internet.

---

## ❓ What is DNS?
- Think of DNS as the **internet's phonebook**.
- Users type domain names → DNS resolves them to IP addresses.

---

## 🧩 DNS Components: Nameservers & Zone Files

### 📌 Nameservers
- Servers responsible for handling DNS queries for a domain.
- Types:
  - **Root** (.)
  - **TLD** (.com, .net)
  - **Authoritative** (holds zone files)

### 🗂️ Zone Files
- Contain **DNS records** for a domain.
- Managed by authoritative nameservers.

---

## 🧾 DNS Records

| Record Type | Purpose                           |
|-------------|------------------------------------|
| A           | Maps domain to IPv4 address        |
| AAAA        | Maps domain to IPv6 address        |
| CNAME       | Alias to another domain            |
| MX          | Mail exchange server               |
| TXT         | Human-readable notes (e.g., SPF)   |
| NS          | Delegates to nameservers           |
| SOA         | Start of authority (domain config) |

---

## 🔄 How DNS Works (Query Flow)

1. User enters `example.com`
2. Resolver asks **root server** → Who handles `.com`?
3. Asks **TLD server** → Who handles `example.com`?
4. Gets answer from **authoritative nameserver**
5. IP is returned to user & **cached** for future use

---

## 🧪 Tools for DNS Debugging

### 🔍 `nslookup`
Quick lookup of DNS records
```bash
nslookup example.com
```

## 🔬 dig

More detailed DNS diagnostics

```bash
dig example.com
dig +trace example.com
```

## 🧾 /etc/hosts File

- Local file that maps hostnames to IPs.
- Used before DNS is queried.

```bash
127.0.0.1   localhost
192.168.1.10  test.local
```

📌 Tip: Use /etc/hosts for testing or overriding DNS locally.