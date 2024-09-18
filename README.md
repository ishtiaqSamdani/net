# net


### 1. **IP Addressing**

IP Addressing refers to the assignment of unique numerical labels to devices in a network to allow for communication. There are two major versions of IP addresses:

- **IPv4**: 
  - 32-bit address (e.g., `192.168.1.1`).
  - Limited to approximately 4.3 billion unique addresses.
  - Written in dot-decimal notation: four numbers (0-255) separated by dots.

- **IPv6**:
  - 128-bit address (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
  - Provides a much larger address space to meet the growing demand for IP addresses.
  - Written in hexadecimal and colon-separated.

**Classes of IP Addresses (IPv4)**:
- **Class A** (1.0.0.0 to 126.255.255.255): Large networks with millions of devices.
- **Class B** (128.0.0.0 to 191.255.255.255): Medium-sized networks.
- **Class C** (192.0.0.0 to 223.255.255.255): Small networks.
- **Class D** (224.0.0.0 to 239.255.255.255): Reserved for multicast.
- **Class E** (240.0.0.0 to 255.255.255.255): Reserved for experimental purposes.

**Private IP Addresses**:
- Used within private networks (not routable on the internet).
- **Private Ranges**:
  - Class A: `10.0.0.0/8`
  - Class B: `172.16.0.0/12`
  - Class C: `192.168.0.0/16`

---

### 2. **Routes**

**Routing** is the process of selecting paths in a network along which to send network traffic. Routers use routing tables to determine the best path for data packets to reach their destination.

- **Routing Table**: A data table stored in a router that lists the routes to particular network destinations.
- **Static Routing**: Routes are manually configured and do not change unless manually updated.
- **Dynamic Routing**: Routes are automatically learned and updated using routing protocols (e.g., OSPF, BGP).

**Key Concepts**:
- **Default Gateway**: The device (usually a router) that a device uses to send packets outside of its local network.
- **Default Route (0.0.0.0/0)**: A catch-all route that directs all traffic that doesn’t match specific routes.
- **CIDR Notation**: IP addresses are often specified using Classless Inter-Domain Routing (CIDR), e.g., `192.168.1.0/24`, where `/24` denotes the subnet mask (`255.255.255.0`).

---

### 3. **Interface, DNS, TCP, HTTPS**

#### **Network Interfaces**
A network interface connects devices to a network. It could be physical (like an Ethernet port) or virtual (in the case of VMs or containers).

- **Physical Interface**: A hardware component, such as a network card.
- **Virtual Interface**: Used in virtualized environments or containers to enable network communication.

#### **DNS (Domain Name System)**
DNS translates domain names (like `example.com`) into IP addresses that computers use to communicate. It's a hierarchical system:
1. **Root DNS Servers**: Directs the query to the appropriate top-level domain (TLD) server.
2. **TLD DNS Servers**: Handles the top-level domains (e.g., `.com`, `.org`).
3. **Authoritative DNS Servers**: Contains the actual IP addresses for a domain.

**DNS Records**:
- **A Record**: Maps a domain to an IPv4 address.
- **AAAA Record**: Maps a domain to an IPv6 address.
- **CNAME**: An alias for another domain.
- **MX Record**: Specifies mail servers for a domain.

#### **TCP (Transmission Control Protocol)**
TCP is a connection-oriented protocol that ensures reliable communication between devices. It establishes a connection, guarantees data integrity, and ensures data is delivered in the correct order.

**TCP Handshake**:
1. **SYN**: The client sends a synchronization request to the server.
2. **SYN-ACK**: The server acknowledges the request.
3. **ACK**: The client sends an acknowledgment, establishing the connection.

**Use Case**: TCP is used by most major protocols such as HTTP/HTTPS, SSH, and FTP.

#### **HTTPS (HyperText Transfer Protocol Secure)**
HTTPS is the secure version of HTTP, used to encrypt communication between a client (e.g., a browser) and a server. It uses **TLS (Transport Layer Security)** to secure the data, ensuring privacy and integrity.

**Key Features of HTTPS**:
- **Encryption**: Data is encrypted to prevent eavesdropping.
- **Authentication**: The server's identity is verified using certificates.
- **Integrity**: Ensures that data hasn’t been tampered with during transit.

