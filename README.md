# University Campus Network Using Cisco Packet Tracer

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7.svg)](https://www.netacad.com/cisco-packet-tracer)
[![Course](https://img.shields.io/badge/Course-CSE405-green.svg)]()

## 📋 Project Overview

This project focuses on designing an **Enhanced University Network** using Cisco Packet Tracer. The objective is to create a secure and efficient network architecture that integrates dynamic IP allocation, VLAN segmentation, and robust routing protocols.

The simulation represents a university campus network comprising multiple departments and external connectivity to cloud-hosted servers. Advanced security configurations ensure protection against common threats, while protocols like **OSPF** and **DHCP** enhance network efficiency.

## 🎯 Objectives

1. To design a secure and scalable network for a university campus
2. To simulate the network using Cisco Packet Tracer
3. To integrate dynamic IP addressing and VLAN segmentation

## 🏗️ Network Architecture

### Departments Connected
- **Electrical Engineering**
- **Computer Science** 
- **Mathematics**
- **Admissions Office**

### Network Components

| Component | Model/Type |
|-----------|------------|
| Routers | Cisco 2911 |
| Core Switches | Layer 3 Switches |
| Access Switches | VLAN-enabled Layer 2 Switches |
| Servers | DHCP Servers |
| End Devices | PCs (one per department) |

## 🔧 Protocols Used

| Protocol | Purpose |
|----------|---------|
| **OSPF** (Open Shortest Path First) | Dynamic routing between networks |
| **DHCP** (Dynamic Host Configuration Protocol) | Automatic IP address allocation |
| **ACLs** (Access Control Lists) | Enhanced security and traffic filtering |
| **ICMP** (Internet Control Message Protocol) | Network connectivity testing (ping) |
| **VLAN** (Virtual Local Area Network) | Logical network segmentation |

## 📊 Network Topology

Each department operates on **separate VLANs**, ensuring logical segregation and enhanced security. The network is configured with unique subnets per VLAN, and routers are programmed for inter-VLAN routing.

### VLAN Configuration Example

| Department | VLAN ID | Subnet |
|------------|---------|---------|
| Computer Science | VLAN 10 | 192.168.10.0/24 |
| Electrical Engineering | VLAN 20 | 192.168.20.0/24 |
| Mathematics | VLAN 30 | 192.168.30.0/24 |
| Admissions Office | VLAN 40 | 192.168.40.0/24 |

## 🚀 Features

- ✅ **Dynamic IP Allocation** - DHCP servers automatically assign IP addresses
- ✅ **VLAN Segmentation** - Logical isolation between departments
- ✅ **Inter-VLAN Routing** - Layer 3 switches enable cross-department communication
- ✅ **Access Control Lists (ACLs)** - Security rules to filter traffic
- ✅ **Port Security** - Prevents unauthorized device connections
- ✅ **OSPF Dynamic Routing** - Efficient route advertisement and failover
- ✅ **Cloud Connectivity** - External access to hosted servers

## 🖥️ Testing & Verification

### Ping Testing

The `ping` command is used for troubleshooting device accessibility. It uses ICMP Echo messages to determine:

- Whether a remote host is active or inactive
- The round-trip delay in communicating with the host
- Packet loss percentage

#### Test Results

| Source | Destination | IP Address | Status |
|--------|-------------|------------|--------|
| PC2 (CS Dept) | PC8 (CS Dept) | 192.168.10.2/24 | ✅ Successful |
| PC2 (CS Dept) | PC6 (Admissions) | 192.168.7.2/24 | ✅ Successful |

### Performance Metrics

| Metric | Result |
|--------|--------|
| Packet Delivery Success Rate | Optimal |
| Packet Loss | Minimal |
| Latency | Within acceptable range |
| Bandwidth Utilization | Efficient |

## 📁 Project Structure

```
university-campus-network/
├── README.md                 # Project documentation
├── projectFile.pkt      # Cisco Packet Tracer file
```

## 🛠️ Prerequisites

- [Cisco Packet Tracer](https://www.netacad.com/cisco-packet-tracer) (version 8.0 or higher recommended)
- Basic understanding of networking concepts
- Knowledge of Cisco IOS commands

## 📥 Installation & Setup

### Step 1: Install Cisco Packet Tracer

Download and install Cisco Packet Tracer from the Cisco Networking Academy website.

### Step 2: Open the Project File

```bash
1. Launch Cisco Packet Tracer
2. File → Open
3. Select `projectFile.pkt`
```

### Step 3: Verify Configurations

Check that all devices are properly configured:
- Verify router interfaces are up
- Check VLAN assignments on switches
- Ensure DHCP services are running

### Step 4: Test Connectivity

```bash
# From any PC, ping devices in different VLANs
ping 192.168.10.2    # Ping CS department host
ping 192.168.7.2     # Ping Admissions department host
```

## 📊 Sample Configuration Snippets

### Router OSPF Configuration

```
router ospf 1
 network 192.168.10.0 0.0.0.255 area 0
 network 192.168.20.0 0.0.0.255 area 0
 network 192.168.30.0 0.0.0.255 area 0
 network 192.168.40.0 0.0.0.255 area 0
```

### VLAN Configuration on Switch

```
vlan 10
 name CS_Department
vlan 20
 name EE_Department
vlan 30
 name Math_Department
vlan 40
 name Admissions_Department
```

### DHCP Pool Configuration

```
ip dhcp pool CS_DEPT_POOL
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 8.8.8.8
```

## 📈 Results & Performance Analysis

The simulation successfully demonstrates:

1. ✅ **Successful Inter-VLAN Communication** - Devices in different VLANs can communicate via Layer 3 routing
2. ✅ **Dynamic IP Assignment** - DHCP servers successfully assign IP addresses to all end devices
3. ✅ **Reliable Connectivity** - Ping tests show 0% packet loss within the network
4. ✅ **Security Implementation** - ACLs effectively control traffic between departments

## 🔒 Security Features

- **Access Control Lists (ACLs)** - Restrict unauthorized access between departments
- **Port Security** - Limit MAC addresses per switch port
- **VLAN Isolation** - Prevent broadcast storms and enhance security
- **SSH Configuration** - Secure remote management (optional)

## 🚧 Future Work

| Area | Enhancement |
|------|-------------|
| **Physical Implementation** | Deploy the design in a real university environment |
| **Advanced Security** | Integrate firewalls and intrusion detection systems |
| **Wireless Connectivity** | Add Wi-Fi access points for mobility |
| **Redundancy** | Implement HSRP/VRRP for gateway redundancy |
| **IPv6 Support** | Extend the design to support IPv6 addressing |
| **Network Monitoring** | Add SNMP for centralized monitoring |

## 👥 Team Members

| Student Name | Student ID |
|--------------|------------|
| Md Ashik | 2020-3-60-032 |
| Md. Asifuzzaman | 2021-3-60-167 |
| Fatema Tahsin Anamika | 2021-3-60-170 |
| Md Rashedur Rahman Tanvir | 2022-1-60-187 |

## 📚 Course Information

| Field | Details |
|-------|---------|
| **Course Code** | CSE405 |
| **Course Title** | Computer Networks |
| **Section** | 04 |
| **Instructor** | Md. Khalid Mahbub Khan |
| **Department** | Computer Science and Engineering |
| **Submission Date** | January 30, 2025 |

## 📖 References

1. Ahmed, A., & Al-Hamadani, M. (2021). Designing a secure campus network. *Indonesian Journal of Electrical Engineering*.
2. Kornilovitch, P., Bicknell, R., & Yeo, J. (2009). Fully connected networks with local connections. *Applied Physics A*.
3. Clarke, G. E. (2009). *CompTIA Network+ Certification Study Guide*. McGraw-Hill.

## 📄 License

This project is for educational purposes as part of the CSE405 Computer Networks course.

## 🙏 Acknowledgments

- Md. Khalid Mahbub Khan for guidance and supervision
- Department of Computer Science and Engineering
- East West University

---

**📧 Contact**: For any questions regarding this project, please contact the course instructor or team members.

---
*Submitted in partial fulfillment of the requirements for CSE405 - Computer Networks*
