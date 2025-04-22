# 🌐 Networking Concepts – Quick Reference

---

## 📌 IPv4 vs IPv6

| **Feature**         | **IPv4**                            | **IPv6**                              |
|---------------------|-------------------------------------|----------------------------------------|
| Address Length      | 32-bit                              | 128-bit                                |
| Format              | Decimal (e.g., 192.168.1.1)         | Hexadecimal (e.g., 2001:db8::1)        |
| No. of Addresses    | 4.3 billion                         | 340 undecillion+                       |
| Security            | Less secure (optional IPSec)        | Built-in security (IPSec)              |
| Speed & Routing     | Slower                              | Faster & efficient                     |
| Address Shortage    | Yes                                 | No shortage – future-ready             |

---

## 🏗️ 2-Tier vs 3-Tier Architecture

| **Feature**        | **2-Tier**                            | **3-Tier**                                        |
|--------------------|----------------------------------------|---------------------------------------------------|
| Layers             | Client + DB                            | Client + App Server + DB                          |
| Business Logic     | In client                              | In application server                             |
| Performance        | Fast but less scalable                 | Little slower but more scalable                   |
| Security           | Less secure                            | More secure                                       |
| Example            | MS Access                              | Flipkart, Gmail, Online Banking apps              |

---

## 🔁 CIDR – Classless Inter-Domain Routing

### ✅ CIDR Format

<Network Address>/<CIDR Notation>


### 🧠 IP Address Range Formula

Total IPs = 2^(32 - CIDR Range)

### 📊 CIDR Table Examples

| **CIDR**        | **Range**                     | **Total IPs** |
|------------------|-------------------------------|----------------|
| 10.0.0.0/32      | 10.0.0.0                       | 1              |
| 10.0.0.0/31      | 10.0.0.0 - 10.0.0.1            | 2              |
| 10.0.0.0/30      | 10.0.0.0 - 10.0.0.3            | 4              |
| 10.0.0.0/29      | 10.0.0.0 - 10.0.0.7            | 8              |
| 10.0.0.0/28      | 10.0.0.0 - 10.0.0.15           | 16             |
| 10.0.0.0/27      | 10.0.0.0 - 10.0.0.31           | 32             |
| 10.0.0.0/26      | 10.0.0.0 - 10.0.0.63           | 64             |
| 10.0.0.0/25      | 10.0.0.0 - 10.0.0.127          | 128            |
| 10.0.0.0/24      | 10.0.0.0 - 10.0.0.255          | 256            |
| 10.0.0.0/22      | 10.0.0.0 - 10.0.3.255          | 1024           |
| 10.0.0.0/16      | 10.0.0.0 - 10.0.255.255        | 65,536         |
| 10.0.0.0/8       | 10.0.0.0 - 10.255.255.255      | 16,777,216     |

---

## 🌍 Public vs Private IP Address

| **Type**         | **Description**                                                             |
|------------------|------------------------------------------------------------------------------|
| Public IP        | Used for global communication (e.g., email, websites).                      |
| Private IP       | Used within internal networks (e.g., company tools, LAN communication).      |

---

## 🖥️ Architecture Diagram (Text Representation)

## 🧱 Architecture

### 🧩 2-Tier Architecture

text
🧑‍💻 Browser
   │
   ▼
🌐 DNS (Route 53)
   │
   ▼
🧰 Load Balancer (ELB)
   │
   ▼
🖥 Web Server (EC2 - Apache)
   │
   ▼
🗄 Database (EC2/RDS/DynamoDB)


- Static files can be served from: 🗂 *S3 Bucket*

---

### 🧩 3-Tier Architecture

text
🧑‍💻 Client (Browser)
   │
   ▼
🌐 DNS (Route 53)
   │
   ▼
🧰 Load Balancer (ELB)
   │
   ▼
⚙ Application Tier (EC2 - Node.js, Spring Boot, etc.)
   │
   ▼
🖥 Web Server Tier (EC2 - Apache/Nginx for static + dynamic content)
   │
   ▼
🗄 Database Tier (RDS / DynamoDB / EC2-DB Server)


🎯 S3 can be connected at the *Web Server Tier* to store and serve static content efficiently.

---

✅ Use *VPC* to structure networking securely and scalably in AWS.


