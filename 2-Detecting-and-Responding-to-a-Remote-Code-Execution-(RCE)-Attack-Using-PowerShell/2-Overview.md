# Overview of Remote Code Execution (RCE) Attack Detection & Response Using PowerShell

This project demonstrates the process of detecting and responding to a Remote Code Execution (RCE) attack using PowerShell, with Microsoft Defender for Endpoint (MDE) configured for monitoring and automated incident response. The attack involves the attacker using PowerShell to download and execute a malicious file (7-Zip installer) on a compromised Windows VM. 

The primary objective of the project is to showcase the creation of a custom detection rule, automate incident response actions such as isolating the compromised VM, and performing detailed forensic analysis to investigate the attack. This simulation highlights the importance of proactive detection, rapid response, and continuous monitoring in a Security Operations Centre (SOC) environment.

## Project Purpose & Goals

- **Simulate a Remote Code Execution (RCE) attack** using PowerShell.
- **Detect and respond** to the attack with Microsoft Defender for Endpoint (MDE).
- **Create a custom detection rule** to identify malicious PowerShell commands.
- **Automate incident response actions** like isolating devices and collecting forensic data.
- **Perform an incident investigation** using collected data to analyse attack vectors.

## Hyperlinks to Sections

- [01 - Environment Setup](./01-Environment-Setup/README.md)
- [02 - Detection Engineering](./02-Detection-Engineering/README.md)
- [03 - Attack Simulation](./03-Attack-Simulation/README.md)
- [04 - Automated Response](./04-Automated-Response/README.md)
- [05 - Forensic Investigation](./05-Forensic-Investigation/README.md)
- [06 - Lessons Learned](./06-Lessons-Learned/README.md)

## Summary Table of Skills & Cybersecurity Domains

| Skill/Technology                | Description                                                       | Relevant Cybersecurity Domain       |
|----------------------------------|-------------------------------------------------------------------|--------------------------------------|
| **Microsoft Defender for Endpoint (MDE)** | A platform for endpoint protection, threat detection, and automated response. | Endpoint Protection, Threat Detection |
| **PowerShell**                   | Scripting language used for automating the download and execution of files. | Incident Response, Malware Analysis  |
| **KQL (Kusto Query Language)**   | Language for querying logs to create custom detection rules.       | Threat Detection, Incident Response |
| **Windows Virtual Machines**     | Virtualized operating systems used for testing and simulating attacks. | Cloud Security, Endpoint Protection |
| **Investigation Packages**       | Forensic data gathered to understand the impact of a security event. | Digital Forensics, Incident Response |
| **Cloud Security (Microsoft Azure)** | Securing cloud-based environments to protect virtual machines and data. | Cloud Security, Endpoint Protection |

## Key Takeaways

- **Custom Detection Rules:** Tailored detection rules improve threat detection capabilities.
- **Automated Response:** Automating actions like isolating compromised devices accelerates response times and reduces manual effort.
- **Forensic Analysis:** Detailed investigation packages help in understanding the attack's impact and can guide recovery and future prevention.
- **SOC Operations:** This project reflects the essential day-to-day tasks of a SOC Analyst, particularly in detecting and responding to advanced threats.
  
## Keywords & Tags

- **SOC (Security Operations Centre)**
- **EDR (Endpoint Detection and Response)**
- **Cloud Security**
- **RCE (Remote Code Execution)**
- **PowerShell Scripting**
- **Incident Response Automation**
- **Forensic Analysis**
- **Threat Detection Rules**
- **MDE (Microsoft Defender for Endpoint)**
- **KQL (Kusto Query Language)**

---

This `overview.md` file provides an overview of the project's objectives, skills gained, and useful links to different sections. It's structured to ensure a professional presentation for anyone reviewing the repository, such as recruiters or potential collaborators.

Let me know if you'd like to modify or enhance any part of the document!
