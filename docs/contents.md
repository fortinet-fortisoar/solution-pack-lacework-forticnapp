| [Home](../README.md) |
 | -------------------------------------------- |

  # Contents

The **Lacework FortiCNAPP Composite Alert Incident Response** solution pack contains the following resources.

## Connector

| Name | Description |
| :- | :- |
| AWS EC2 | Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. |
| Azure Commands | Azure Commands are used to run Azure native commands for Azure resources configurations directly from FortiSOAR. |
| Azure Compute | Azure Virtual Machines are image service instances that provide on-demand and scalable computing resources with usage-based pricing. This connector facilitates automated operations to get list of Azure Compute VM, get information about an Azure Compute VM, create, start, restart, stop and delete of an Azure Compute VM. |
| Google Cloud Compute | Google Compute Engine's tooling and workflow supports to create advanced networks on the regional levels and load balancing capabilities in cloud computing. This connector facilitates automated operation related to GCE operations. |
| Lacework FortiCNAPP | Lacework delivers end-to-end visibility into what’s happening across your cloud environment, including detecting threats, vulnerabilities, misconfigurations, and unusual activity, so you can innovate with speed and safety. |
| Microsoft Teams | Microsoft Teams is a chat-based workspace in Office 365 that provides global, remote, and dispersed teams with the ability to work together and share information using a common space. This connector facilitates automated operation related to teams. |
| Slack | Slack is a cloud-based set of proprietary team collaboration tools and services. This connector facilitates automated operations like list channels, list users, send message etc. This release of Slack connector supports bi-directional communication between Slack and FortiSOAR, allowing you to leverage the power of FortiSOAR as part of your daily communications and threat investigation routines. |

## Playbook Collection

| 10 - SP - Lacework FortiCNAPP Composite Alert Incident Response |
|:------------:|

| Playbook Name | Description |
| :- | :- |
| Lacework FortiCNAPP > Alert Webhook Auth | Authenticates Lacework Webhook Call |
| Lacework FortiCNAPP > Alerts Webhook | Alert Webhook |
| Lacework FortiCNAPP > Create FortiSOAR alert from Lacework FortiCNAPP Alert | Creates a FortiSOAR alert from a Lacework FortiCNAPP alert |
| Lacework FortiCNAPP > Extract Indicators | Extracts and creates indicators from the specified data and then enriches specific fields in alerts with the indicator data. |
| Lacework FortiCNAPP > Potentially Compromised Host Alert | Incident response playbook with slack approval chain for stop instance and take volume snapshot. |
| Lacework FortiCNAPP > Potentially Compromised Host Alert Generate | Fetches Potentially Compromised Host Alerts from Lacework and Creates records in FortiSOAR. |
| Lacework FortiCNAPP > Potentially Compromised Identity Alert | Incident response playbook with chatops approval chain for disable access keys and revoke active sessions. |

>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.

# Next Steps
| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
| ----------------------------------------- | ------------------------------------------- | --------------------- |