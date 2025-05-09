# Overview: Brute Force Detection Rule in Microsoft Sentinel

## Sections Map

| Phase | Title                                                        | File Name                                    |
|-------|--------------------------------------------------------------|----------------------------------------------|
| 3.1   | Environment Setup                                             | [3.1-Environment-Setup.md](3.1-Environment-Setup.md)                       |
| 3.2   | Detection Rule Development                                    | [3.2-Detection-Rule-Development.md](3.2-Detection-Rule-Development.md)     |
| 3.3   | Deployment and Incident Detection                             | [3.3-Deployment-and-Incident-Detection.md](3.3-Deployment-and-Incident-Detection.md) |
| 3.4   | Post-Validation and Confirming No Compromise                  | [3.4-Post-Validation-and-Confirming-No-Compromise.md](3.4-Post-Validation-and-Confirming-No-Compromise.md) |
| 3.5   | Incident Resolution and Post-Mortem                           | [3.5-Incident-Resolution-and-Post-Mortem.md](3.5-Incident-Resolution-and-Post-Mortem.md) |
| 3.6   | Reflection and Skills Gained                                  | [3.6-Reflection-and-Skills-Gained.md](3.6-Reflection-and-Skills-Gained.md) |

---

## Project Summary

This project focused on designing, deploying, and validating a custom detection rule in Microsoft Sentinel to identify brute force login attempts targeting Azure virtual machines. The goal was to create a precise, low-noise detection mechanism that could trigger alerts when 10 or more failed login attempts were observed from the same remote IP to a specific host within a 5-hour window.

The core of the solution was a KQL query designed to filter, group, and surface only relevant failed login patterns. Once validated, the rule was deployed as a Scheduled Query Rule within Sentinel and configured to run every four hours. Upon deployment, the rule successfully detected multiple brute force attempts originating from external IP addresses.

Following detection, I carried out a structured incident response using Microsoft Sentinel's investigation tools and Microsoft Defender for Endpoint. This included reviewing endpoint activity, initiating antivirus scans, correlating threat indicators, and confirming no successful logins or signs of lateral movement.

The incident was documented, formally closed, and summarised in a post-mortem analysis. This project reinforced key principles of SOC operations — proactive detection, timely triage, and evidence-driven response.

---

## Detection Logic

- **Data Source:** `DeviceLogonEvents`
- **KQL Filters:** `ActionType == "LogonFailed"` and `TimeGenerated > ago(5h)`
- **Aggregation Logic:** Grouped failed logins by IP and device, flagged if count ≥ 10
- **Execution Frequency:** Every 4 hours
- **Alert Grouping:** Enabled by RemoteIP and DeviceName
- **Mapped MITRE ATT&CK Techniques:**
  - T1110: Brute Force
  - T1087: Account Discovery

---

## Key Outcomes

- Multiple brute force attempts detected across three Azure VMs.
- Five malicious IP addresses flagged and reviewed.
- No successful logins or secondary activity confirmed.
- The detection logic proved effective with no false positives or escalated risk.
- A full post-incident review was documented for internal reference.

---

## Skills Gained

| Skill Area                            | Description                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **KQL (Kusto Query Language)**        | Refined the ability to write performant queries for log analysis and detection tuning in Sentinel.              |
| **Microsoft Sentinel Rule Authoring** | Gained experience creating Scheduled Query Rules, managing alert logic, and applying grouping configuration.    |
| **Threat Detection Design**           | Designed a rule targeting specific brute force patterns using empirical thresholds and efficient filtering.     |
| **Log Analytics Investigation**       | Used Log Analytics to validate detection hypotheses and trace malicious activity based on login telemetry.      |
| **Incident Response Lifecycle**       | Conducted end-to-end response activities including ownership, investigation, containment, and closure.          |
| **Microsoft Defender for Endpoint**   | Reviewed endpoint behaviour, ran antivirus scans, and confirmed integrity of potentially targeted hosts.         |
| **Threat Intelligence Correlation**   | Identified and tracked attacking IPs with the potential for future watchlist integration or IOC enrichment.      |
| **Post-Incident Documentation**       | Documented investigation steps, conclusions, and lessons learned in alignment with SOC reporting standards.      |
| **Security Monitoring Practices**     | Gained a deeper appreciation for how scheduled analytics and telemetry-based detection strengthen SOC visibility.|
| **MITRE ATT&CK Mapping**              | Practised mapping detection events to MITRE techniques for standardised classification of threat activity.      |
| **Validation and Assurance Testing**  | Implemented follow-up queries to confirm no successful logins, ensuring accuracy and completeness of detection.  |
| **Rule Maintenance Strategy**         | Considered alert tuning, false positive management, and how to evolve rules for broader coverage.               |

---

## Final Reflection

This project strengthened my ability to contribute to detection engineering tasks within a SOC environment. It highlighted how tactical use of Microsoft Sentinel and Defender for Endpoint can help surface real threats while avoiding alert fatigue. Importantly, it showed how a focused, well-structured rule — combined with clear documentation and disciplined follow-through — can serve as an effective line of defence in the early stages of attack detection.

The approach used here can be expanded to other attack types, including password spraying, lateral movement detection, or cloud-based reconnaissance, forming the basis for a broader detection strategy in Azure environments.

