[Home](../README.md) |
 | -------------------------------------------- |

# Usage

## Playbook Configuration 

### FortiSOAR \> API Token

* **Overview** The alerts webhook playbook will use the configured FortiSOAR API token both to authenticate remote consumers and to execute the alerts webhook playbook itself. This is an important understanding especially with regards to configuring the assigned Role for the API Keys.
* **Key** In Settings > Security Management > API Keys create a new API key called "Lacework". Copy the value for the key as you will need it as part of the Lacework FortiCNAPP setup. 
* **Role** Either create a new Role or use an existing role for this API Key. Required permissions are:

    - **Alerts**: Create/Read/Update
    - **Application**: Read
    - **Indicators**: Create/Read/Update
    - **Playbooks**: Read/Execute

### Lacework FortiCNAPP \> Alerts Webhook 

* **Setup**: Configure a webhook in the Lacework console (e.g., `https://<your-fortisoar-instance>/api/triggers/v1/deferred/lacework_forticnapp_composite?api_token=<FORTISOAR API TOKEN>`).   
* **Rule**: Create a new alert rule with Critical and High severity and Composite category.

### Lacework FortiCNAPP \> Potentially Compromised Host Alert Generate (Optional) 

* **Setup**: Pull alerts from Lacework using `lacework_account` and `lacework_subaccount` as parameters. The Approval Action step will require a valid Slack email address. A placeholder value will need to be updated (default value is `<A VALID SLACK EMAIL ADDRESS>`)
* **Usage**: Playbook can be run manually or integrated into workflows. 

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