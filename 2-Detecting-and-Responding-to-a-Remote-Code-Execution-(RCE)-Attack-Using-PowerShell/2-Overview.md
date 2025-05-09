# Overview: PowerShell-Based Remote Code Execution (RCE) Detection & Response Project

## Project Summary

In this project, I simulated a PowerShell-based Remote Code Execution (RCE) attack on a Windows 10 virtual machine within Microsoft Azure. The goal was to detect the attack using Microsoft Defender for Endpoint (MDE), respond automatically, and analyse the outcome through forensic investigation.

The simulation involved using PowerShell commands to download and install a potentially malicious application (7-Zip), triggering a custom detection rule in MDE. Upon detection, the compromised device was automatically isolated, and an investigation package was collected for analysis. This project reflected real-world SOC workflows, demonstrating the value of proactive threat detection, automated incident response, and evidence-based forensic review.

---

## Project Sections

- [**2.1 Environment Setup**](2.1-Environment-Setup.md)
- [**2.2 Detection Engineering**](2.2-Detection-Engineering.md)
- [**2.3 Attack Simulation**](2.3-Attack-Simulation.md)
- [**2.4 Automated Response**](2.4-Automated-Response.md)
- [**2.5 Forensic Investigation**](2.5-Forensic-Investigation.md)
- [**2.6 Lessons Learned**](2.6-Lessons-Learned.md)

---
##  Skills Table

| Skill                          | Tools/Technologies                        | Application in Project                                             |
|-------------------------------|-------------------------------------------|--------------------------------------------------------------------|
| **Threat Detection**          | Microsoft Defender for Endpoint, KQL      | Created custom KQL detection rules to identify PowerShell-based RCE |
| **Incident Response**         | MDE, Automation Rules                     | Automated device isolation and collection of forensic evidence     |
| **Digital Forensics**         | MDE Investigation Packages                | Analysed process trees, event logs, and file/registry activity     |
| **Cloud Security**            | Microsoft Azure                           | Deployed and managed the Windows VM environment                    |
| **Scripting & Automation**    | PowerShell                                | Simulated attacker behaviour using command-line scripts            |
| **Detection Engineering**     | Kusto Query Language (KQL)                | Wrote precise queries targeting malicious PowerShell behaviour     |
| **Security Operations (SOC)** | MDE Portal, Action Centre                 | Followed SOC processes for alert triage, investigation, and response |
| **Endpoint Protection**       | Microsoft Defender for Endpoint           | Configured advanced endpoint monitoring and response mechanisms    |

---



## Summary of Lessons Learned

This project reinforced several key concepts:

- **Proactive Detection Is Essential**: Creating custom rules targeting attacker TTPs (Tactics, Techniques, and Procedures) greatly enhances threat visibility.
- **Automation Speeds Up Response**: Leveraging automated actions like device isolation and evidence collection drastically reduces response time.
- **KQL Mastery Adds Defensive Depth**: Understanding how to translate malicious behaviours into queries is critical for modern detection engineering.
- **Forensics Validates Response**: Analysing forensic data ensures not only that the alert was accurate but also that the response was effective and complete.
- **Simulations Build Confidence**: Testing detection and response capabilities in a controlled environment mirrors real-world SOC challenges and prepares me for on-the-job scenarios.

---

## Final Thoughts

This hands-on lab project deepened my skills in threat detection, response automation, and forensic analysis using enterprise-grade tools. It closely mirrors the day-to-day responsibilities of a SOC analyst and positions me to contribute to proactive cyber defence efforts in real environments.
