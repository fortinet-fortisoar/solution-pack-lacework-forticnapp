[Home](../README.md) |
 | -------------------------------------------- |

# Usage

## Playbook Configuration 

### Lacework FortiCNAPP \> Alerts Webhook 

* **Setup**: Configure a webhook in the Lacework console (e.g., `https://<your-fortisoar-instance>/api/triggers/v1/deferred/<unique-GUID>`).   
* **Rule**: Create a new alert rule with Critical and High severity and Composite category.   
* **FortiSOAR Configuration**: Edit the webhook playbook in FortiSOAR, provide the same GUID, and validate via Lacework. 

### Lacework FortiCNAPP \> Potentially Compromised Host Alert Generate (Optional) 

* **Setup**: Pull alerts from Lacework using `lacework_account` and `lacework_subaccount` as parameters.   
* **Usage**: Playbook can be run manually or integrated into workflows. 

## First Run Configuration 

Playbooks in the solution pack are *Deactivated* by default, once configuration is complete the of the included playbooks should be *Activated*. To do this browse to the **SP \- Lacework FortiCNAPP v0.1.0 (Beta)** folder in ForitSOAR, select all playbooks and click the *Activate* button.

## Appendix 

### Playbook Workflow Diagram 

```mermaid
flowchart TD
    A[Lacework FortiCNAPP Alert] --> |Pulled/Pushed via Webhook| B[FortiSOAR Alert Created]
    B --> C[Enrichment of IP, Domain, FileHash Indicators]
    C --> D[Trigger Incident Response Playbook]
    D --> E[Message Sent to FortiSOAR Application Channel]
    E --> F{End-User Chooses Action}
    
    F --> |Stop Instance| G1[Use Cloud Provider Connector to Stop Instance]
    F --> |Stop Instance & Take Snapshot| G2[Use Cloud Provider Connector to Stop Instance & Take Snapshot]
    F --> |Take Snapshot| G3[Use Cloud Provider Connector to Take Snapshot]
    F --> |No Action| G4[No Action Taken]
    
    G1 --> H1[Send Summary of Action]
    G2 --> H2[Send Summary of Action]
    G3 --> H3[Send Summary of Action]
    G4 --> H4[Send No Action Summary]
    
    H1 --> I[Prompt to Close Alert in Lacework FortiCNAPP Console]
    H2 --> I
    H3 --> I
    H4 --> I

```

# Next Steps
| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
| ----------------------------------------- | ------------------------------------------- | --------------------------- |