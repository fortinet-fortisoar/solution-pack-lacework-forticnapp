# Release Information 

- **Version**:  1.0.0![](./docs/res/icon-preview.svg)
- **Certified**: No
- **Publisher**: Fortinet 
- **Contributor**: Jamie Mcmurray 
- **Compatible Version**: FortiSOAR v7.4.0 and above

>[!NOTE]
>Preview releases are a beta release. This means that the release is intended to get feedback and might not be best suited for production level deployments. The functionality might change in backward-incompatible ways or have limited support. A beta release is not subject to any SLA, Quality Assurance or deprecation policy. Feature availability and support for preview releases will continue to improve as the solution matures.

## Overview

The **Lacework FortiCNAPP Composite Alerts** Solution Pack for FortiSOAR demonstrates an incident response flow for the "Potentially Compromised Host" composite alert. Alerts are either pulled or pushed (via webhook) into FortiSOAR, creating a local alert. Once the alert is created, IP, Domain, and FileHash indicators are enriched using configured sources (e.g., Fortinet FortiGuard Threat Intelligence connector). The incident response playbook is then triggered, prompting the user to select one of four actions: Stop Instance, Stop Instance & Snapshot, Take Snapshot, or No Action. FortiSOAR uses the appropriate cloud connector to execute the selected action and notifies the user upon completion, with a prompt to close the alert in the Lacework FortiCNAPP console.

 # Next Steps
 | [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) | 
 |--------------------------------------------|----------------------------------------------|------------------------|------------------------------|