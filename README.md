# Release Information 

- **Version**:  2.0.0
- **Certified**: No
- **Publisher**: Fortinet 
- **Contributor**: Jamie Mcmurray 
- **Compatible Version**: FortiSOAR v7.4.0 and above

## Overview

The **Lacework FortiCNAPP Composite Alert Incident Response** Solution Pack for FortiSOAR demonstrates an incident response flow for the "Potentially Compromised Host" and "Potentially Compromised AWS Identity" composite alert. Alerts are either pulled or pushed (via webhook) into FortiSOAR, creating a local alert. Once the alert is created, IP, Domain, and FileHash indicators are enriched using configured sources (e.g., Fortinet FortiGuard Threat Intelligence connector). The incident response playbooks are then triggered, prompting the user in Teams or Slack to select one of four actions for Host Releated Alerts: Stop Instance, Stop Instance & Snapshot, Take Snapshot, or No Action. Or for Identity related alerts one of four actions: Disable Access Keys, Revoke Sessions, Disable Access Keys & Revoke Sessions or No Action. FortiSOAR uses the appropriate cloud connector to execute the selected action and notifies the user upon completion, with a prompt to close the alert in the Lacework FortiCNAPP console.

 # Next Steps
 | [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) | 
 |--------------------------------------------|----------------------------------------------|------------------------|------------------------------|