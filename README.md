# splunk-detection-lab


## Objective

Built a controlled, isolated virtualized environment to develop detection engineering and defensive security skills. This lab provides a safe space to understand attacker techniques and build effective detections using Splunk Enterprise. By simulating common attack scenarios in a closed environment, I practiced writing SPL queries and analyzing security logs without impacting real systems.

The goal was to understand how attacks actually work in order to build better detections when working in real security operations.

## Skills Learned

- Installed and configured Splunk Enterprise, set up Universal Forwarder, and configured log ingestion.
- Built SPL queries to identify suspicious authentication patterns, process execution, and network scanning.
- Learned to spot attack patterns in logs in order to write detection rules that catch them early.
- Parsed and correlated Windows event logs to identify attack indicators.

---

## Lab Architecture

**Environment:** VirtualBox  
**VMs:**
- **Windows 10** - Target machine (Splunk Universal Forwarder installed)
- **Kali Linux** - Attacker machine
- **Ubuntu Server** - Splunk Enterprise installation

**Attack Simulation Tools:**
- Nmap
- Native Windows tools
- Command-line utilities

---

## Lab Setup Process

### **Step 1: VM Configuration**
- Created three VirtualBox VMs (Windows 10, Kali Linux, Ubuntu Server)
- Allocated resources: 4GB RAM for Splunk server, 2GB for Windows target, 2GB for Kali

### **Step 2: Splunk Installation**
- Installed Splunk Enterprise on Ubuntu Server
- Configured receiving port (9997) for Universal Forwarder
- Created indexes for Windows logs

### **Step 3: Log Forwarding Setup**
- Installed Splunk Universal Forwarder on Windows 10 target
- Configured inputs.conf to forward event logs
- Verified log ingestion in Splunk

### **Step 4: Execution & Detection**
- Ran Nmap scans from Kali Linux
- Monitored log ingestion in real-time
- Tested SPL detection queries

## Disclaimer

This lab environment is for **educational purposes only**. All attacks were conducted in an isolated, controlled environment with no connection to production systems or networks.
