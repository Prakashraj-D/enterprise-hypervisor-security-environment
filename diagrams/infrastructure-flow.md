
# Infrastructure Flow

## 1. Physical Infrastructure

```

Enterprise Server Hardware
│
├── CPU: Multi-core Enterprise Processor
├── RAM: 32 GB
├── Disk 1: 3 TB
├── Disk 2: 1 TB
├── Disk 3: 4 TB
└── Disk 4: 4 TB

```

---

## 2. Storage Architecture

```

Storage Layer
│
├── Base OS Storage
│   └── RAID 1 (3 TB + 1 TB)
│        └── Usable Space: ~1 TB
│
└── Virtualization Storage Pool
└── RAID 1 (4 TB + 4 TB)
└── ZFS Filesystem
├── Data Integrity Checks
├── Snapshot Support
├── Compression
└── Self-Healing

```

---

## 3. Virtualization Layer

```

Linux Hypervisor Host
│
├── Virtual Machine Network
│
├── VM1 – HRMS Server
│   ├── OS: Ubuntu
│   ├── vCPU: 16
│   ├── RAM: 16 GB
│   └── Purpose: Internal HR management system
│
├── VM2 – Wazuh SIEM
│   ├── vCPU: 16
│   ├── RAM: 8 GB
│   ├── Storage: 2 TB
│   └── Purpose: Security monitoring & log analysis
│
├── VM3 – n8n Automation
│   ├── vCPU: 4
│   ├── RAM: 4 GB
│   └── Purpose: Security workflow automation
│
└── VM4 – MISP Threat Intelligence
├── vCPU: 4
├── RAM: 8 GB
└── Purpose: IOC & threat intelligence management

```

---

## 4. Security Monitoring Flow

```

Infrastructure Logs
│
▼
Wazuh SIEM
│
▼
Threat Intelligence Enrichment
│
▼
MISP Platform
│
▼
IOC Matching & Alert Enrichment

```

---

## 5. Automation Layer

```

Security Alert Generated
│
▼
n8n Automation Workflow
│
├── Alert Processing
├── Data Enrichment
├── Notification
└── Incident Response Workflow

```

---

## 6. Security Ecosystem Overview

```

Physical Server
│
▼
Linux Hypervisor
│
▼
ZFS Storage Pool
│
▼
Virtual Machines
│
├── HRMS (Business Application)
├── Wazuh SIEM (Security Monitoring)
├── n8n (Automation Engine)
└── MISP (Threat Intelligence)

```

---

## 7. Key Security Benefits

- Storage redundancy using RAID 1
- ZFS data integrity and snapshot capability
- Segregated virtual machine environment
- Centralized SIEM monitoring using Wazuh
- Threat intelligence integration using MISP
- Security workflow automation using n8n
