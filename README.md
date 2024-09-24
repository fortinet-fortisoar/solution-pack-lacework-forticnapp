## Release Information

- **Version**:  0.1.0 (Beta)
- **Certified**: Yes 
- **Publisher**: Fortinet 
- **Compatible Version**: FortiSOAR v7.4.0 and above

## Overview

The **Lacework FortiCNAPP Solution Pack** for FortiSOAR demonstrates an incident response flow for the "Potentially Compromised Host" composite alert. Alerts are either pulled or pushed (via webhook) into FortiSOAR, creating a local alert. Once the alert is created, IP, Domain, and FileHash indicators are enriched using configured sources (e.g., Fortinet FortiGuard Threat Intelligence connector). The incident response playbook is then triggered, prompting the user to select one of four actions: Stop Instance, Stop Instance & Snapshot, Take Snapshot, or No Action. FortiSOAR uses the appropriate cloud connector to execute the selected action and notifies the user upon completion, with a prompt to close the alert in the Lacework FortiCNAPP console.

# Next Steps 
 
| [Overview](https://github.com/credibleforce/solution-pack-lacework-forticnapp/blob/develop/docs/setup.md#overview) | [Connector Configuration](https://github.com/credibleforce/solution-pack-lacework-forticnapp/blob/develop/docs/setup.md#fortisoar-connector-configuration) | [Playbook Configuration](https://github.com/credibleforce/solution-pack-lacework-forticnapp/blob/develop/docs/setup.md#playbook-configuration) | [First Run Configuration](https://github.com/credibleforce/solution-pack-lacework-forticnapp/blob/develop/docs/setup.md#first-run-configuration) |
|--------------------------------------------|----------------------------------------------|------------------------|------------------------------|