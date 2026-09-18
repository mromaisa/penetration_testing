# Pentesting Lab & Security Assessment

A structured penetration-testing and cybersecurity learning repository documenting practical security assessments, laboratory environments, reconnaissance, enumeration, vulnerability assessment, exploitation, and post-exploitation activities.

This repository is maintained as a hands-on learning portfolio, with an emphasis on understanding **why security tools and techniques work**, documenting findings, and following an authorized testing methodology.

> **Disclaimer:** All testing documented in this repository is performed only against systems that I own, intentionally vulnerable laboratory environments, or systems for which explicit authorization has been obtained. The material is provided for educational and defensive security research purposes. Do not use these techniques against systems or networks without permission.

---

## Objectives

The primary objectives of this repository are to:

* Build practical penetration-testing skills through controlled laboratory environments.
* Understand the methodology used during professional security assessments.
* Practice identifying and documenting security weaknesses.
* Develop familiarity with industry-standard security tools.
* Understand the relationship between reconnaissance, enumeration, vulnerability discovery, exploitation, and post-exploitation.
* Maintain reproducible documentation of security experiments and findings.
* Develop a professional security portfolio demonstrating practical cybersecurity work.

---

# Assessment Methodology

The repository follows a phased penetration-testing workflow. Individual assessments may not require every phase, depending on the scope and objective of the exercise.

```text
                    ┌─────────────────────┐
                    │  Scope & Planning   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Reconnaissance      │
                    │ & Footprinting      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Scanning &          │
                    │ Enumeration         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Vulnerability       │
                    │ Assessment          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Exploitation        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Post-Exploitation   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Privilege Escalation│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Persistence &       │
                    │ Lateral Movement    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Reporting & Risk    │
                    │ Analysis            │
                    └─────────────────────┘
```

The phases are treated as an interconnected process rather than isolated tool exercises.

---

# Repository Structure

The repository is organized so that additional penetration-testing phases can be added without requiring a redesign of the project structure.

```text
Pentesting/
│
├── README.md
│
├── 01-Lab-Setup/
│   └── lab-setup.pdf
│
├── 02-Reconnaissance/
│   └── fingerprinting-and-reconnaissance.pdf
│
├── 03-Scanning-Enumeration/
│   └── ...
│
├── 04-Vulnerability-Assessment/
│   └── ...
│
├── 05-Exploitation/
│   └── ...
│
├── 06-Post-Exploitation/
│   └── ...
│
├── 07-Privilege-Escalation/
│   └── ...
│
├── 08-Lateral-Movement/
│   └── ...
│
├── 09-Persistence/
│   └── ...
│
├── 10-Reporting/
│   └── ...
│
└── Evidence/
    ├── screenshots/
    ├── scan-results/
    ├── notes/
    └── artifacts/
```

The exact structure may evolve as the laboratory expands.

---

# Current Progress

## Phase 1 — Lab Setup

The initial documentation covers the preparation of the penetration-testing environment, including the systems and tools used for controlled security testing.

**Status:** Completed

Documentation:

* `01-Lab-Setup/lab-setup.pdf`

---

## Phase 2 — Reconnaissance & Footprinting

This phase documents passive and active reconnaissance activities performed against authorized targets and controlled laboratory systems.

Activities include:

* Domain footprinting
* WHOIS information gathering
* DNS enumeration
* Subdomain and certificate discovery
* Technology fingerprinting
* HTTP header inspection
* Web application fingerprinting
* WAF detection
* Public information gathering
* Network discovery
* Host identification
* Initial attack-surface mapping

Tools explored include:

* WHOIS
* `host`
* `nslookup`
* DNSRecon
* WhatWeb
* Wafw00f
* Curl
* crt.sh
* Netcraft
* theHarvester
* Nmap
* Zenmap

**Status:** Completed

Documentation:

* `02-Reconnaissance/fingerprinting-and-reconnaissance.pdf`

---

# Planned Phases

As the laboratory progresses, the repository will expand into the following areas.

## Phase 3 — Scanning & Enumeration

Focus:

* Host discovery
* Port scanning
* Service enumeration
* Version detection
* Operating-system detection
* Network service identification
* Web server enumeration
* SMB enumeration
* SSH enumeration
* FTP and other service enumeration
* Network topology analysis

Typical tools:

```text
Nmap
Zenmap
Netcat
Enum4linux
Nikto
Gobuster
```

---

## Phase 4 — Vulnerability Assessment

Focus:

* Identifying vulnerabilities in discovered services
* Configuration weaknesses
* Outdated software
* Web application weaknesses
* Authentication issues
* Network-service vulnerabilities
* Prioritizing findings by risk

Potential tools:

```text
Nmap NSE
Nessus
OpenVAS / Greenbone
Nikto
SearchSploit
Burp Suite
```

Findings will be documented with evidence, affected components, risk, and recommended remediation.

---

## Phase 5 — Exploitation

This phase will document controlled exploitation of vulnerabilities identified during previous phases.

Focus:

* Understanding exploit prerequisites
* Exploit selection
* Controlled exploitation
* Obtaining limited access
* Validating vulnerability impact
* Recording evidence
* Maintaining scope throughout testing

Exploitation will only be performed against authorized laboratory targets or systems explicitly approved for testing.

Potential tools:

```text
Metasploit Framework
SearchSploit
Burp Suite
Nmap NSE
Custom scripts
```

---

## Phase 6 — Post-Exploitation

Focus:

* Understanding the obtained access
* System and user enumeration
* Process inspection
* Network configuration discovery
* Credential and configuration analysis
* Identifying accessible resources
* Assessing the impact of compromised access

The objective is to understand what an attacker could realistically access after initial compromise without exceeding the authorized scope.

---

## Phase 7 — Privilege Escalation

Privilege-escalation exercises will examine how a low-privileged compromise can potentially become a higher-privileged compromise.

Areas of study:

### Linux

* SUID/SGID binaries
* File permissions
* Sudo configuration
* Cron jobs
* PATH manipulation
* Kernel and software weaknesses
* Writable files and directories
* Misconfigured services

### Windows

* Service misconfigurations
* Weak permissions
* Scheduled tasks
* Registry configuration
* Credential exposure
* Token and privilege abuse
* Local privilege-escalation vulnerabilities

---

## Phase 8 — Lateral Movement

Where supported by the laboratory environment, this phase will examine movement between systems after an initial compromise.

Topics may include:

* Network trust relationships
* Credential reuse
* SMB
* SSH
* Remote administration services
* Internal network enumeration
* Segmentation weaknesses
* Pivoting concepts

Testing will remain restricted to intentionally configured laboratory environments.

---

## Phase 9 — Persistence

This phase will study how an attacker could maintain access after compromising a system and, more importantly, how defenders can detect and remove such mechanisms.

Topics may include:

* Scheduled tasks
* Services
* Startup mechanisms
* SSH keys
* User accounts
* Configuration-based persistence
* Detection and cleanup

Persistence mechanisms will be implemented only in isolated laboratory environments.

---

# Reporting & Risk Analysis

A major objective of this repository is to move beyond simply running security tools.

Each significant finding should attempt to answer:

1. **What was discovered?**
2. **How was it discovered?**
3. **Why does it matter?**
4. **What could an attacker potentially do with it?**
5. **What is the associated risk?**
6. **What evidence supports the finding?**
7. **How can it be mitigated?**

Where appropriate, findings will include:

```text
Finding
Affected Asset
Description
Evidence
Attack Surface
Potential Impact
Risk Level
Recommended Remediation
Validation
```

The final reporting phase will consolidate technical findings into a structured security assessment.

---

# Tools & Technologies

The toolkit used throughout the repository will evolve with the assessment phases.

### Reconnaissance

```text
WHOIS
DNSRecon
Nslookup
Host
crt.sh
Netcraft
theHarvester
WhatWeb
Wafw00f
Curl
```

### Network Security

```text
Nmap
Zenmap
Netcat
Wireshark
```

### Vulnerability Assessment

```text
Nmap NSE
OpenVAS / Greenbone
Nessus
Nikto
SearchSploit
```

### Web Security

```text
Burp Suite
Gobuster
Nikto
Curl
```

### Exploitation

```text
Metasploit Framework
SearchSploit
```

### Operating Systems & Environment

```text
Kali Linux
Linux
Windows
Virtual Machines
Local Network Lab
```

Additional tools will be added as new techniques and phases are studied.

---

# Documentation Philosophy

This repository is intended to document **understanding, not just tool output**.

For each practical exercise, documentation should explain:

```text
Objective
    ↓
Method
    ↓
Tool / Command
    ↓
Observed Result
    ↓
Security Significance
    ↓
Risk
    ↓
Recommendation
```

Screenshots, command output, configuration details, and other evidence are included where useful to make the work reproducible and verifiable.

Sensitive information such as real credentials, private keys, tokens, personal information, or unauthorized target information will not be committed to the repository.

---

# Legal & Ethical Scope

All activities in this repository are conducted within an authorized environment.

Testing targets may include:

* Personal systems
* Intentionally vulnerable machines
* Isolated cybersecurity laboratories
* Training platforms
* Systems covered by explicit written authorization

Unauthorized scanning, exploitation, credential attacks, persistence, or access to third-party systems is outside the scope of this repository.

The techniques documented here should be used for legitimate security testing, education, research, and defensive purposes.

---

# Learning Outcomes

Through the progression of this repository, the goal is to develop practical understanding of:

* Attack-surface discovery
* Network reconnaissance
* Service enumeration
* Vulnerability identification
* Exploitation methodology
* Linux and Windows security
* Privilege escalation
* Post-exploitation analysis
* Network segmentation
* Web application security
* Security risk assessment
* Technical security reporting

The long-term objective is to develop the ability to **reason through an assessment from the target's exposed attack surface to the security impact of a confirmed finding**, rather than relying solely on automated tools.

---

# Project Status

**Current stage:** Reconnaissance / Network Scanning

```text
[✓] Lab Setup
[✓] Reconnaissance & Footprinting
[✓] Initial Network Discovery
[ ] Scanning & Enumeration
[ ] Vulnerability Assessment
[ ] Exploitation
[ ] Post-Exploitation
[ ] Privilege Escalation
[ ] Lateral Movement
[ ] Persistence
[ ] Final Security Assessment
```

This checklist will be updated as additional phases are completed.

---

## Disclaimer

This repository represents a personal cybersecurity learning and assessment portfolio. It does not represent authorization to test any system, network, application, organization, or individual.

**Always obtain explicit permission and define the testing scope before performing security testing against systems that you do not own.**
