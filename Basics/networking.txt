# 🖥️ Types of IP Address

## IPv4 and IPv6

- **IPv4 Range:** `0.0.0.0 to 255.255.255.255`

### Four Types of Class in IPv4:
- **Class A:** `1.0.0.0 to 126.255.255.255`  
  🧾 *Example:* `10.1.25.5` belongs to Class A  
- **Class B:** `128.0.0.0 to 191.255.255.255`  
  🧾 *Example:* `172.20.10.5` belongs to Class B  
- **Class C:** `192.0.0.0 to 223.255.255.255`  
  🧾 *Example:* `192.168.1.1` belongs to Class C  
- **Class D:** (Reserved for multicast)
- **Class E:** (Reserved for experimental use)

> 🔁 **127.x.x.x** is a **loopback address**, mainly used to test network interfaces.
>
> 🧪 *Example:* `127.0.0.1` is commonly called `localhost` and used to test applications on the same machine.

---

## Public and Private IPs

### 🔒 Private IPs:
Used within private networks (not accessible directly from the internet).

- `10.0.0.0 - 10.255.255.255` (**10/8 prefix**)  
  🧾 *Example:* `10.0.1.2` used in enterprise networks  
- `172.16.0.0 - 172.31.255.255` (**172.16/12 prefix**)  
  🧾 *Example:* `172.20.5.10` used in large organizations  
- `192.168.0.0 - 192.168.255.255` (**192.168/16 prefix**)  
  🧾 *Example:* `192.168.1.1` commonly used in home routers

### 🌐 Public IPs:
Used to access the internet directly. These are assigned by ISPs.

🧾 *Example:* `8.8.8.8` is a public IP provided by Google for DNS services.

---