# Vic Modern Hotel Network Project

## 📌 Project Overview
This project involves the design and implementation of a **computer network for Vic Modern Hotel**.  
The hotel has **three floors** with different departments, each segmented using VLANs for better security and management.  
The project is implemented using **Cisco Packet Tracer**.

---

## 🏢 Network Design

- **3 Routers** located in the IT department/server room.  
- Routers connected using **Serial DCE cables**.  
- **One switch per floor**.  
- **VLANs** assigned per department.  
- **DHCP** for automatic IP allocation.  
- **OSPF** for routing.  
- **SSH** for secure remote management.  
- **Port Security** on IT department switch for Test-PC.  

---

## 📊 VLAN & IP Addressing Plan

| Floor | Department  | VLAN ID | Network             |
|-------|-------------|---------|---------------------|
| 1st   | Reception   | 80      | 192.168.8.0/24      |
| 1st   | Store       | 70      | 192.168.7.0/24      |
| 1st   | Logistics   | 60      | 192.168.6.0/24      |
| 2nd   | Finance     | 50      | 192.168.5.0/24      |
| 2nd   | HR          | 40      | 192.168.4.0/24      |
| 2nd   | Sales       | 30      | 192.168.3.0/24      |
| 3rd   | Admin       | 20      | 192.168.2.0/24      |
| 3rd   | IT          | 10      | 192.168.1.0/24      |

**Router Interconnections (Serial Links):**
- R1 ↔ R2: `10.10.10.0/30`  
- R2 ↔ R3: `10.10.10.4/30`  
- R1 ↔ R3: `10.10.10.8/30`  

---

## ⚙️ Key Configurations

### VLANs & Trunks
Each switch is configured with **access VLANs** and **trunk links**.  

### Routing
- **OSPF** is used for dynamic routing.  
- Area 0 backbone configuration.  

### DHCP
- Each VLAN has its own **DHCP pool**.  
- Default gateway is the router’s VLAN interface.  

### Security
- **SSH** configured on all routers.  
- **Port Security** on IT switch (only Test-PC allowed).  

---

## 🧪 Testing
1. **Ping Test** between PCs in different VLANs.  
2. **DHCP Test** – PCs and printers receive IP addresses dynamically.  
3. **SSH Test** – Remote login to routers from Test-PC.  

---


## 🚀 How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Vic-Modern-Hotel-Network.git
