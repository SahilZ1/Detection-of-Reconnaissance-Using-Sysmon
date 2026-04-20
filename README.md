#  Detection of Network Reconnaissance Using Sysmon

## Overview
This project demonstrates the detection of network reconnaissance activity in a virtual SOC lab environment.

A simulated attacker (Kali Linux) performed an Nmap port scan against a Windows 10 virtual machine. The activity was successfully detected and analysed using Sysmon Event ID 3 logs, which capture network connections at the endpoint level.

## Lab Environment

- **Attacker Machine:** Kali Linux (VirtualBox)
- **Target Machine:** Windows 10 VM (VirtualBox)
- **Monitoring Tool:** Sysmon
- **Network Configuration:** Host-only network

## Attack Simulation

The following Nmap command was used to simulate reconnaissance activity:
nmap -n -sT -Pn -p 80,135,445,3389 192.168.56.103

Detection & Analysis

Sysmon Event ID 3 logs were used to detect network connections originating from the attacker machine.

### Key Findings
- Source IP: 192.168.56.102
- Destination IP: 192.168.56.103
- Multiple connection attempts across ports
- Behaviour consistent with port scanning

  
