[Home](../README.md) |
|--------------------------------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.
2. From the list of solution pack that appears, search for and select **Lacework FortiCNAPP Composite Alert Incident Response**.
3. Click the **Lacework FortiCNAPP Composite Alert Incident Response** solution pack card.
4. Click **Install** on the lower part of the screen to begin the installation.

## Prerequisites
The **Lacework FortiCNAPP Composite Alert Incident Response** solution pack depends on the following solution packs that are installed automatically &ndash; if not already installed.
| Solution Pack Name | Version | Purpose |
| :--------------------- | :---------------------| :--------------------------------------- |
| SOAR Framework | v2.0.0 and later | Required for Incident Response modules                   |



# Configuration
For optimal performance of **Lacework FortiCNAPP Composite Alert Incident Response** solution pack, you can install and configure the connectors that help with the following:

* **AWS EC2** - Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage.. To configure and use the AWS EC2 connector, refer to [Configuring AWS EC2](https://docs.fortinet.com/fortisoar/connectors/aws-ec2)
    * **Permissions**: `ec2:StopInstances`, `ec2:StartInstances`, `ec2:DescribeInstances`, `ec2:CreateSnapshot`, `ec2:DescribeVolumes`   
    * IAM role example:
        ```json   
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Action": [
                        "ec2:StopInstances",
                        "ec2:StartInstances",
                        "ec2:DescribeInstances"
                    ],
                    "Effect": "Allow",
                    "Resource": "*"
                },
                {
                    "Action": [
                        "ec2:CreateSnapshot",
                        "ec2:DescribeVolumes"
                    ],
                    "Effect": "Allow",
                    "Resource": "*"
                }
            ]
        }
        ```

    * **Note**: Connector name must match the AWS account number integrated into Lacework. 

* **Azure Commands** - Azure Commands are used to run Azure native commands for Azure resources configurations directly from FortiSOAR.. To configure and use the Azure Commands connector, refer to [Configuring Azure Commands](https://docs.fortinet.com/fortisoar/connectors/azure-commands)
    * **Permissions**: `Virtual Machine Contributor`, `Disk Snapshot Contributor `  
    * **Note**: Connector name must match the lower-case Azure subscription name integrated into Lacework. 

* **Google Cloud Compute** - Google Compute Engine's tooling and workflow supports to create advanced networks on the regional levels and load balancing capabilities in cloud computing. This connector facilitates automated operation related to GCE operations.. To configure and use the Google Cloud Compute connector, refer to [Configuring Google Cloud Compute](https://docs.fortinet.com/fortisoar/connectors/googlecloudcompute)
    * **Permissions**: `roles/backupdr.computeEngineOperator`  
    * **Note**: Connector name must match the lower-case GCP project name integrated into Lacework.

* **Lacework FortiCNAPP** - Lacework delivers end-to-end visibility into what’s happening across your cloud environment, including detecting threats, vulnerabilities, misconfigurations, and unusual activity, so you can innovate with speed and safety.. To configure and use the Lacework FortiCNAPP connector, refer to [Configuring Lacework FortiCNAPP](https://docs.fortinet.com/fortisoar/connectors/lacework)
    * **Permissions**: API key for a service account with admin user access (or a custom role that allows alert read/write)   
    * **Configuration**: Create a service user in the Lacework console, download API keys, and configure the FortiSOAR connector with the subaccount name and the API keys.   
    * **Note**: Connector name must match the lower-case subaccount name. 

* **Slack** - Slack is a cloud-based set of proprietary team collaboration tools and services. This connector facilitates automated operations like list channels, list users, send message etc. This release of Slack connector supports bi-directional communication between Slack and FortiSOAR, allowing you to leverage the power of FortiSOAR as part of your daily communications and threat investigation routines.. To configure and use the Slack connector, refer to [Configuring Slack](https://docs.fortinet.com/fortisoar/connectors/slack2)

* **Azure Compute** - Azure Virtual Machines are image service instances that provide on-demand and scalable computing resources with usage-based pricing. This connector facilitates automated operations to get list of Azure Compute VM, get information about an Azure Compute VM, create, start, restart, stop and delete of an Azure Compute VM. To configure and use the Azure Compute connector, refer to [Configuring Azure Compute](https://docs.fortinet.com/fortisoar/connectors/azure-compute)


# Next Steps
| [Usage](./usage.md) | [Contents](./contents.md) |
|---------------------|---------------------------|