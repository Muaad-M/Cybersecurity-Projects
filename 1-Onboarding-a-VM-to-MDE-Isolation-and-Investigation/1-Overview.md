# Microsoft Defender for Endpoint (MDE) - VM Onboarding and Incident Response Project

## Project Overview

This project demonstrates a simulated hands-on Security Operations Center (SOC) workflow using Microsoft Defender for Endpoint (MDE) on a Windows 10 Virtual Machine (VM) hosted in Microsoft Azure. The goal is to showcase essential endpoint detection and response (EDR) practices—spanning VM deployment, onboarding to MDE, incident response, and forensic analysis. The lab environment was designed to reflect real-world cybersecurity operations in a cloud-based setting.

The project is broken down into four key sections, each representing a crucial part of the SOC analyst workflow.

---

## 🔹 Project Sections

### 1. [Onboarding Windows VM to Microsoft Defender for Endpoint](./1.1-Onboarding-MDE/1.1-Document.md)
Covers the end-to-end process of provisioning a Windows 10 VM and securely onboarding it into Microsoft Defender for Endpoint. Includes environment setup, onboarding package deployment, and validation.

### 2. [Incident Response - Isolating VM and Forensic Analysis](./1.2-Incident-Response/1.2-Document.md)
Simulates a security incident by isolating the VM and remotely collecting an investigation package. Demonstrates how endpoint telemetry is gathered and analyzed during threat containment.

### 3. [Network Testing - Validating Isolation and Connectivity](./1.3-Network-Testing/1.3-Document.md)
Describes the methodology for testing VM network isolation using ICMP traffic and NSG rule manipulation to simulate threat exposure and containment.

### 4. [Skills Acquired and Cybersecurity Correlation](./1.4-Skills-Documentation/1.4-Document.md)
Details the technical and procedural skills acquired through the project. Each skill is mapped to its corresponding cybersecurity domain, highlighting relevance to real-world SOC roles.

---

## 🧠 Skills Summary (ATS-Optimized)

| Skill Area                                 | Description                                                                 | Relevant Domain(s)                              |
|--------------------------------------------|-----------------------------------------------------------------------------|-------------------------------------------------|
| Azure Virtual Machine Deployment           | Built and configured secure Windows 10 VMs in Azure                         | Cloud Infrastructure, Platform Security         |
| Endpoint Detection and Response (EDR)      | Onboarded endpoints into Microsoft Defender for Endpoint                    | EDR Tools, Endpoint Security                    |
| Microsoft 365 Security Center Management   | Navigated the Defender portal to manage devices, alerts, and incidents      | Security Operations, Threat Management          |
| Incident Detection and Containment         | Isolated systems to prevent threat propagation                              | SOC Response, Incident Handling                 |
| Digital Forensics and Artifact Collection  | Collected forensic data for threat triage and investigation                 | Cyber Forensics, Threat Hunting                 |
| Network Security Group (NSG) Rule Tuning   | Modified NSG rules to test firewall behavior and simulate exposure          | Network Security, Cloud Defense                 |
| ICMP/Network Traffic Monitoring            | Conducted continuous ping tests for isolation validation                    | Monitoring, Detection Engineering               |
| PowerShell & Scripted Deployment           | Executed onboarding scripts using elevated privileges                       | Automation, Endpoint Hardening                  |
| Action Center Workflow Tracking            | Used MDE Action Center to track investigation package lifecycle             | Case Management, SOC Workflow                   |
| Adversary Simulation (Purple Team Concept) | Simulated compromise and tested containment playbooks                       | Security Testing, SOC Readiness                 |
| Secure Credential Management               | Used secure password policies during VM setup                               | Identity & Access Management (IAM)              |
| MITRE ATT&CK Alignment (Implied)           | Procedures mimic real-world tactics for detection and mitigation            | Threat Modeling, SOC Strategy                   |
| Documentation & Reporting                  | Wrote structured documentation of all SOC actions and procedures            | Audit Readiness, Cybersecurity Compliance       |

---

## 📚 Reference

This lab was completed using the resources and instructions provided in Josh Madakor’s Cybersecurity Lab Series:  
📎 [https://joshmadakor.tech/cyber/](https://joshmadakor.tech/cyber/)

---

## 💡 Summary

By completing this project, I developed key competencies in endpoint protection, Azure resource configuration, MDE functionality, and SOC response workflows. These skills align with the responsibilities of SOC Analysts, Security Engineers, and Incident Responders. This serves as both a practical portfolio artifact and a foundational exercise for a cybersecurity operations career.
