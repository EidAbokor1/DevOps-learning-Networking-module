# 🛰️ Routing Cheat Sheet

## 🔄 What is Routing?
Routing is the process of **selecting a path** for traffic in a network.  
It determines how data packets travel from **source to destination** across networks.

Routers use **routing tables** to decide the best next hop for a packet based on its destination IP.

---

## 🛣️ Static vs. Dynamic Routing

### 📌 Static Routing
- Manually configured routes.
- Simple & predictable, but doesn't adapt to network changes.
- Best for small, stable networks.

✅ Pros:
- Easy to configure  
- Low CPU/memory usage  
- Secure (no advertisement)

❌ Cons:
- Doesn’t auto-update  
- Hard to manage in large networks

---

### 🔄 Dynamic Routing
- Routers **communicate with each other** to learn/update routes automatically.
- Uses routing protocols (e.g., OSPF, BGP, RIP).

✅ Pros:
- Auto-adjusts to changes  
- Scales well in large networks

❌ Cons:
- More complex  
- Uses more resources  
- Susceptible to route flapping/misconfigs

---

## 📡 Common Routing Protocols

| Protocol | Type       | Description                                 |
|----------|------------|---------------------------------------------|
| **RIP**  | Distance-vector | Old/simple, uses hop count as metric (max 15) |
| **OSPF** | Link-state     | Fast convergence, cost-based metric, used in enterprise LANs |
| **EIGRP**| Hybrid         | Cisco proprietary, combines vector + link-state |
| **BGP**  | Path-vector    | Core routing protocol of the internet (used between ISPs) |

---

📌 **Note**:  
- **IGP (Interior Gateway Protocol)**: RIP, OSPF, EIGRP (within an org)
- **EGP (Exterior Gateway Protocol)**: BGP (between organizations)

