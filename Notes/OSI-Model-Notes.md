# OSI Model Overview

## 🌐 Introduction to the OSI Model
The **OSI Model (Open Systems Interconnection)** is a conceptual framework used to understand and standardize how data is transmitted across a network. It divides communication into **7 layers**, each with a specific function.

---

## 📚 The 7 Layers of the OSI Model

| Layer | Name               | Function Summary                                  |
|-------|--------------------|----------------------------------------------------|
| 7     | Application         | User-facing apps (e.g., HTTP, FTP, DNS)           |
| 6     | Presentation        | Data formatting, encryption, compression (e.g., SSL/TLS) |
| 5     | Session             | Session control between devices (start/stop/manage) |
| 4     | Transport           | Reliable delivery, segmentation (TCP/UDP, ports)  |
| 3     | Network             | Routing & addressing (IP, ICMP)                   |
| 2     | Data Link           | Frame delivery over physical link (MAC, ARP)      |
| 1     | Physical            | Actual transmission media (cables, bits)          |

---

## 📦 TCP/IP Model: A Practical Alternative

While the OSI model is conceptual, the **TCP/IP Model** is used in real networks (e.g., the internet). It has **4 layers**, mapped as follows:

| TCP/IP Layer   | OSI Equivalent Layers           |
|----------------|----------------------------------|
| Application    | Layers 5–7                      |
| Transport      | Layer 4                         |
| Internet       | Layer 3                         |
| Network Access | Layers 1–2                      |

---

## 🔄 Sender vs Receiver: OSI Layer Perspective

- **Sender**: Data is **encapsulated** as it moves **down** the OSI layers.
- **Receiver**: Data is **decapsulated** as it moves **up** the OSI layers.

🧠 Think:  
Sender → [App → Physical]  
Receiver → [Physical → App]

---

## 🎯 Ports & Protocols

**Ports** identify specific processes/services on a device.  
**Protocols** define how data is formatted and exchanged.

| Protocol | Port | Layer | Description            |
|----------|------|--------|------------------------|
| HTTP     | 80   | 7      | Web traffic (insecure) |
| HTTPS    | 443  | 7      | Secure web traffic     |
| FTP      | 21   | 7      | File Transfer Protocol |
| SSH      | 22   | 7      | Secure Shell           |
| DNS      | 53   | 7      | Domain name resolution |
| TCP/UDP  | —    | 4      | Transport protocols    |

---

## ✅ Quick Tip for Troubleshooting with OSI

Use the OSI model as a **top-down checklist**:
1. Is the application working? (Layer 7)
2. Is there a TLS or format issue? (6)
3. Is the session stable? (5)
4. Is the port open? (4)
5. Is the route valid? (3)
6. Is the local network fine? (2)
7. Is the device even connected? (1)

---

📌 *Memorization Tip:*  
**"All People Seem To Need Data Processing"** (Acronym from L7 to L1)

