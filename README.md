# SOC-automation-project

## Security Event Management Flow

1. **Windows 10 Client Wazuh Agent (Event Collection)**
   - An agent installed on a Windows 10 client machine collects security-related data such as logs, network activity, and system changes. The agent then forwards these events to the Wazuh Manager.

2. **Wazuh Manager (Event Processing)**
   - The Wazuh Manager serves as the central processing hub for the received events. It aggregates, normalizes, and analyzes the data to detect potential security threats.

3. **Alert Generation**
   - Upon identifying possible security threats, the Wazuh Manager generates alerts. These alerts are then sent to Shuffle for further processing.

4. **IOC Enrichment**
   - IOC stands for Indicators of Compromise. In Shuffle, these IOCs are enriched by correlating the incoming data with known threat intelligence sources, such as VirusTotal.

5. **Alert Dispatch to TheHive**
   - After enrichment, the refined alerts are forwarded to TheHive for deeper investigation, team collaboration, and case management.

6. **Email Notifications**
   - Simultaneously, alerts can also be sent via email to administrators, security analysts, or other relevant stakeholders to ensure timely awareness and response.

7. **SOC Analyst**
   - The SOC Analyst, depicted as a desktop computer with dual screens, receives alerts from both TheHive and direct email notifications. Their role involves analyzing the incidents, responding to potential threats, and taking necessary actions.

This project implements the process of security event management within an organization, covering event collection, analysis, alerting, IOC enrichment, and communication with the appropriate personnel.
