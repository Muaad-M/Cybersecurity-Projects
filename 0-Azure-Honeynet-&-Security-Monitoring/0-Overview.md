# Overview
As an aspiring security professional, I am committed to building my skills and knowledge in cybersecurity by gaining hands-on experience with real-world technologies and practices. To support this goal, I undertook an independent project to deploy a honeypot infrastructure within Microsoft Azure and integrate Azure Sentinel for centralized log collection and security monitoring. This project provided me with the opportunity to simulate real-world cyber threats and gain practical experience using Azure-native tools, helping me to develop a solid foundation in cloud security, event analysis, and threat detection as I continue to learn and grow in the field.
# Goals

## Azure Infrastructure Setup:

- **Azure Subscription**: Configured an Azure subscription and set up the environment to support security monitoring activities, laying the groundwork for further exploration into security practices and cloud infrastructure.
  
- **Resource Group Creation**: Organised resources within a dedicated Resource Group to ensure clear management and easy tracking of all related components throughout the project.

- **Virtual Network Deployment**: Deployed a Virtual Network in Azure to securely host the honeypot VM, ensuring proper traffic segregation between private and public-facing zones, which aligned with basic security principles.

## Security Configuration:

- **Network Security Groups (NSGs)**: Configured a Network Security Group (NSG) to expose the honeypot VM to a variety of potential attack scenarios, allowing inbound traffic from any source. This setup helped to simulate a vulnerable environment for testing purposes.

- **VM Configuration**: Deployed a Windows 10 virtual machine (VM), and intentionally exposed it to attack simulations by disabling the Windows Firewall and allowing unrestricted traffic, which helped simulate a compromised environment.

- **Vulnerability Simulation**: By allowing all inbound traffic and disabling the firewall protection, I created a simulated vulnerable environment, which provided valuable experience in testing and observing attack scenarios.

## Log Collection and Analysis:

- **Log Analytics Workspace (LAW)**: Set up a Log Analytics Workspace (LAW) to centralise the collection and analysis of security logs, which provided a centralised location for efficient log management and simplified troubleshooting.

- **Azure Sentinel Integration**: Integrated Azure Sentinel with the LAW to store, collect, and query security logs. Focusing on failed login attempts (Event ID 4625), I was able to enhance monitoring and improve my understanding of security log analysis.

- **Kusto Query Language (KQL) Querying**: Applied Kusto Query Language (KQL) to query the logs within Azure Sentinel, which allowed me to identify patterns and gain a deeper understanding of the data, helping me improve my ability to detect and investigate potential security issues.

## GeoIP Enrichment and Attack Map Creation:

- **GeoIP Data Integration**: Imported a GeoIP Watchlist into Azure Sentinel and used KQL to link security logs with geographical data, providing additional context to enrich the analysis and broaden my understanding of where attacks originated.

- **Attack Map Visualization**: Developed an interactive Attack Map within Azure Sentinel, which visualised the distribution of failed login attempts across different geographical locations. This helped me better interpret attack patterns and improve my approach to data analysis.
