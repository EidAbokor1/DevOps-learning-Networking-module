# 🧰 Networking Troubleshooting Cheat Sheet

## 🧠 27. Troubleshoot Like a PRO!

🔁 **Follow the OSI Model** from bottom to top:

1. **Physical (L1)** – Check cables, Wi-Fi, adapter
2. **Data Link (L2)** – Verify MAC address, ARP, switches
3. **Network (L3)** – Check IP, ping gateway, traceroute
4. **Transport (L4)** – Confirm open ports (TCP/UDP)
5–7. **Session to App (L5–L7)** – Application behavior, DNS, firewalls

✅ Always ask:
- Is it plugged in?
- Can I reach the gateway?
- Is DNS resolving?
- Is the service responding?

---

## 📡 28. Tools: `ping`, `traceroute`, `nslookup`

### 📍 `ping`
- Test basic **connectivity** to a host  
```bash
ping 8.8.8.8
ping google.com
```

## 🌐 `traceroute` / `tracert` (Windows)
- Trace the path a packet takes through the network
```bash
traceroute google.com
```

## 🔎 `nslookup` / `dig`
- Diagnose DNS resolution
```bash
nslookup google.com
dig google.com
```

## 🛠 Bonus Tips
- Check IP config: ip a or ipconfig

- View routes: ip route or route print

- Flush DNS: sudo systemd-resolve --flush-caches or ipconfig /flushdns

- Restart network: sudo systemctl restart NetworkManager

📌 Use these tools in sequence to pinpoint where the issue is — connectivity, DNS, routing, or app level.