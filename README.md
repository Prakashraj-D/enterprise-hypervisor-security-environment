# Enterprise-Hypervisor-Security-Environment

## Overview

This project demonstrates the deployment of an enterprise-grade virtualization infrastructure designed for both production workloads and cybersecurity monitoring.

The environment integrates virtualization, SIEM monitoring, and threat intelligence to create a secure SOC-ready infrastructure.

## Architecture Components

• Linux Hypervisor  
• ZFS Storage Pool  
• RAID 1 Storage Redundancy  
• Virtual Machine Infrastructure  
• Wazuh SIEM  
• MISP Threat Intelligence  
• Automation Server (n8n)

## Storage Architecture

Base OS Storage
RAID 1 (3TB + 1TB → 1TB usable)

Virtualization Storage
RAID 1 (4TB + 4TB → 4TB usable)

Filesystem: ZFS

Benefits:
• Data integrity
• Snapshots
• Self-healing
• High availability

## Virtual Machines Deployed

HRMS Server
- Ubuntu
- 16 vCPU
- 16 GB RAM

Wazuh SIEM
- 16 vCPU
- 8 GB RAM
- 2 TB storage

n8n Automation Server
- Workflow automation
- Security alert automation

MISP Threat Intelligence
- IOC sharing
- Threat enrichment

## Security Integration

Wazuh + MISP Integration Workflow

Security Events  
↓  
Wazuh Log Analysis  
↓  
IOC Lookup via MISP  
↓  
Threat Intelligence Enrichment  
↓  
Enhanced Alerts

## Skills Demonstrated

- Hypervisor deployment
- Linux server administration
- ZFS storage management
- SIEM implementation
- Threat intelligence integration
- Security infrastructure design
