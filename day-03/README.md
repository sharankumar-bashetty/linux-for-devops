### Networking concepts and networking related commands:

# Networking Concepts for DevOps and Cloud Engineers

## What is Networking?

Networking is the process of connecting computers, servers, devices, and cloud resources so they can communicate and share data securely and efficiently.

---

# OSI Model (7 Layers)

| Layer | Name         | Purpose                        | Examples            |
| ----- | ------------ | ------------------------------ | ------------------- |
| 7     | Application  | User interaction               | HTTP, HTTPS, DNS    |
| 6     | Presentation | Data formatting and encryption | SSL/TLS             |
| 5     | Session      | Maintains sessions             | NetBIOS             |
| 4     | Transport    | Reliable communication         | TCP, UDP            |
| 3     | Network      | Routing packets                | IP, ICMP            |
| 2     | Data Link    | MAC addressing                 | Ethernet            |
| 1     | Physical     | Cables and signals             | Fiber, Switch Ports |

---

# TCP vs UDP

| TCP                      | UDP                            |
| ------------------------ | ------------------------------ |
| Connection-oriented      | Connectionless                 |
| Reliable                 | Faster                         |
| Error checking           | No delivery guarantee          |
| Used in HTTP, HTTPS, SSH | Used in Streaming, DNS, Gaming |

---

# IP Address

An IP address identifies a device on a network.

## Types

* IPv4 → `192.168.1.1`
* IPv6 → `2001:db8::1`

## Public IP

Accessible over the internet.

## Private IP

Used inside internal networks.

### Private IP Ranges

```text
10.0.0.0/8
172.16.0.0 – 172.31.255.255
192.168.0.0/16
```

---

# Subnetting

Subnetting divides a large network into smaller networks.

## Example

```text
Network: 192.168.1.0/24
Subnet Mask: 255.255.255.0
Total IPs: 256
Usable IPs: 254
```

---

# CIDR Notation

| CIDR | Subnet Mask     | Usable Hosts |
| ---- | --------------- | ------------ |
| /8   | 255.0.0.0       | 16 Million   |
| /16  | 255.255.0.0     | 65K          |
| /24  | 255.255.255.0   | 254          |
| /32  | 255.255.255.255 | 1            |

---

# DNS (Domain Name System)

DNS converts domain names into IP addresses.

## Example

```text
google.com → 142.250.x.x
```

## Common DNS Records

* A Record → IPv4 Mapping
* AAAA Record → IPv6 Mapping
* CNAME → Alias
* MX Record → Mail Server
* TXT Record → Verification Records

---

# DHCP

Dynamic Host Configuration Protocol automatically assigns IP addresses to devices.

---

# MAC Address

A MAC address is a unique hardware address of a device.

## Example

```text
00:1A:2B:3C:4D:5E
```

---

# NAT (Network Address Translation)

NAT converts private IPs into public IPs for internet access.

## Types

* Static NAT
* Dynamic NAT
* PAT (Port Address Translation)

---

# Ports and Protocols

| Port  | Protocol   | Service              |
| ----- | ---------- | -------------------- |
| 20/21 | FTP        | File Transfer        |
| 22    | SSH        | Secure Remote Access |
| 23    | Telnet     | Remote Access        |
| 25    | SMTP       | Mail Sending         |
| 53    | DNS        | Name Resolution      |
| 80    | HTTP       | Web Traffic          |
| 443   | HTTPS      | Secure Web           |
| 3306  | MySQL      | Database             |
| 5432  | PostgreSQL | Database             |
| 6379  | Redis      | Cache                |
| 27017 | MongoDB    | NoSQL Database       |

---

# Routing

Routing decides the best path for data packets.

## Types

* Static Routing
* Dynamic Routing

## Routing Protocols

* RIP
* OSPF
* BGP

---

# Firewall

A firewall filters incoming and outgoing traffic based on rules.

## Types

* Network Firewall
* Application Firewall
* Cloud Firewall

---

# VPN (Virtual Private Network)

A VPN creates a secure encrypted tunnel between the user and the network.

---

# Load Balancer

A load balancer distributes traffic across multiple servers.

## Types

* Layer 4 Load Balancer
* Layer 7 Load Balancer

## Benefits

* High Availability
* Scalability
* Fault Tolerance

---

# HTTP vs HTTPS

| HTTP          | HTTPS              |
| ------------- | ------------------ |
| Not Secure    | Secure             |
| Port 80       | Port 443           |
| No Encryption | SSL/TLS Encryption |

---

# SSL/TLS

SSL/TLS is used to encrypt communication between client and server.

---

# Proxy Server

A proxy server acts as an intermediary between client and internet.

## Types

* Forward Proxy
* Reverse Proxy

## Examples

* Nginx
* HAProxy

---

# CDN (Content Delivery Network)

A CDN distributes content closer to users for faster delivery.

## Examples

* Cloudflare
* Akamai

---

# Networking Devices

| Device | Purpose                   |
| ------ | ------------------------- |
| Router | Connects Networks         |
| Switch | Connects Devices in LAN   |
| Hub    | Broadcasts Data           |
| Bridge | Connects Network Segments |
| Modem  | Internet Connectivity     |

---

# Cloud Networking Concepts

## VPC (Virtual Private Cloud)

A VPC is an isolated virtual network in the cloud.

### Components

* Subnets
* Route Tables
* Internet Gateway
* NAT Gateway
* Security Groups
* NACLs

---

# Security Group vs NACL

| Security Group   | NACL                 |
| ---------------- | -------------------- |
| Stateful         | Stateless            |
| Instance Level   | Subnet Level         |
| Allow Rules Only | Allow and Deny Rules |

---


# Important Networking Commands

```bash
ping google.com
traceroute google.com
nslookup google.com
dig google.com
netstat -tulnp
ss -tulnp
ip addr
ifconfig
curl https://google.com
telnet hostname port
ssh user@host
```

---

# What Happens When You Open google.com?

1. DNS lookup happens
2. Browser gets the IP address
3. TCP handshake starts
4. SSL/TLS negotiation happens
5. HTTP request is sent
6. Server responds
7. Browser renders the webpage

---

# TCP 3-Way Handshake

```text
Client  → SYN
Server  → SYN-ACK
Client  → ACK
```

---

# Important DevOps Networking Topics

* Reverse Proxy
* API Gateway
* Service Mesh
* Zero Trust Networking
* Ingress Controller
* Network Policies
* VPC Peering
* Transit Gateway
* Hybrid Networking
* VPN and Direct Connect

---

# Real-Time DevOps Networking Usage

* SSH into servers
* Configure Load Balancers
* Secure applications using HTTPS
* Setup DNS records
* Troubleshoot connectivity
* Configure Kubernetes Ingress
* Manage VPC and Subnets
* Configure Firewalls and Security Groups

---

# Final Notes

Networking is the backbone of:

* Cloud Computing
* DevOps
* Kubernetes
* Cyber Security
* Site Reliability Engineering (SRE)

As I continue learning and re-skilling in DevOps and Cloud, I realized that strong networking knowledge helps a lot in:


* Troubleshooting
* Cloud Architecture
* Production Support
* Kubernetes Management
* Security Hardening

---



Networking Commands:-

ping google.com – Checks connectivity to a remote server.
ifconfig – Displays network interfaces (deprecated, use ip).
ip a – Shows IP addresses of network interfaces.
netstat -tulnp – Displays open network connections.
curl https://example.com – Fetches a webpage's content.
wget https://example.com/file.zip – Downloads a file from the internet.


# Hashtags

```text
#DevOps
#Networking
#CloudComputing
#AWS
#Kubernetes
#Linux
#Docker
#Terraform
#Azure
#GCP
#SRE
#CyberSecurity
#Cloud
#Tech
#Learning
#Infrastructure
#NetworkingBasics
```
