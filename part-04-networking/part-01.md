# Networking Notes for DevOps

## 1. Introduction to Networking in DevOps
- Networking is crucial in DevOps for ensuring seamless communication between applications, services, and infrastructure.
- It includes configuring and managing network components such as DNS, load balancers, firewalls, and cloud networking services.

## 2. Key Networking Concepts
### **IP Addressing**
- **IPv4** (e.g., 192.168.1.1) and **IPv6** (e.g., fe80::1)
- **Private vs Public IPs**: Private IPs are used within internal networks, whereas public IPs are used for internet communication.

### **DNS (Domain Name System)**
- Resolves domain names to IP addresses.
- Common DNS record types:
  - **A Record**: Maps domain to IPv4.
  - **AAAA Record**: Maps domain to IPv6.
  - **CNAME Record**: Alias of another domain.
  - **MX Record**: Mail exchange record for email routing.

### **Subnets and CIDR**
- Used for efficient IP allocation.
- Example: `192.168.1.0/24` (256 addresses)

### **NAT (Network Address Translation)**
- Allows private IPs to access the internet using a public IP.
- Used in cloud environments for outbound traffic.

### **Firewall and Security Groups**
- Control inbound and outbound traffic.
- Rules define allowed IP ranges and ports.

## 3. Networking in DevOps Tools
### **Docker Networking**
- **Bridge Network** (Default): Containers in the same network can communicate.
- **Host Network**: Containers share the host network.
- **Overlay Network**: Used in Docker Swarm for cross-node communication.
- **Macvlan Network**: Assigns a MAC address to a container.

### **Kubernetes Networking**
- Uses **CNI (Container Network Interface)** plugins.
- **Pod-to-Pod Communication**: All pods can communicate within the cluster.
- **Services**:
  - **ClusterIP**: Internal service.
  - **NodePort**: Exposes service on a node’s IP and port.
  - **LoadBalancer**: Uses cloud provider’s load balancer.

### **CI/CD and Networking**
- Tools like Jenkins, GitLab CI/CD require proper network access for repository and artifact management.
- VPNs or Bastion Hosts are used to secure connections.

## 4. Cloud Networking in DevOps
### **AWS Networking**
- **VPC (Virtual Private Cloud)**: Isolated network in AWS.
- **Subnets**: Public and private network segmentation.
- **Security Groups and NACLs**: Define inbound/outbound rules.
- **Route Tables**: Direct traffic within VPC.

### **Azure Networking**
- **Azure Virtual Network (VNet)**: Isolated cloud network.
- **NSGs (Network Security Groups)**: Traffic filtering.
- **Load Balancers**: Distribute traffic.

### **GCP Networking**
- **VPC and Subnets**: Global virtual network with regional subnets.
- **Firewall Rules**: Define traffic control.
- **Cloud Load Balancers**: Global traffic management.

## 5. Load Balancing
- Ensures high availability and fault tolerance.
- **Types of Load Balancers**:
  - **Layer 4 (Transport Layer)**: TCP/UDP based.
  - **Layer 7 (Application Layer)**: HTTP/HTTPS based.
- Common Load Balancers:
  - AWS ELB (Elastic Load Balancer)
  - Nginx, HAProxy
  - Azure Load Balancer

## 6. VPNs and Secure Communication
- **SSH Tunneling**: Secure remote connections.
- **VPN (Virtual Private Network)**: Secure connection between on-premises and cloud.
- **Bastion Host**: A jump server for secure remote access.

## 7. Observability and Monitoring
- **Network Monitoring Tools**:
  - Prometheus & Grafana
  - AWS CloudWatch
  - Netdata
  - Wireshark (Packet Analysis)
- **Logging**:
  - Fluentd, ELK Stack (Elasticsearch, Logstash, Kibana)

## 8. Conclusion
- Understanding networking is vital for DevOps to ensure secure, scalable, and efficient infrastructure.
- Mastering cloud networking, security, and observability improves system reliability and performance.

