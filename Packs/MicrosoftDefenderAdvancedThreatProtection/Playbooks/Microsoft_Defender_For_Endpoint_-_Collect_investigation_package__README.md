This playbook aims to simplify the collection of investigation package retrieval into XSOAR from only supported machines (according to the article -  https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/collect-investigation-package?view=o365-worldwide). 

The playbook receives information regarding the target devices (by hostnames, IPs, device ids), validates that those devices exist, and retrieves the collection package from those machines into the XSOAR console. Note that this action may time and the average size of such a package is around ~15 MB.

## Dependencies
This playbook uses the following sub-playbooks, integrations, and scripts.

### Sub-playbooks
* GenericPolling

### Integrations
* MicrosoftDefenderAdvancedThreatProtection

### Scripts
* http

### Commands
* microsoft-atp-get-investigation-package-sas-uri
* microsoft-atp-collect-investigation-package
* endpoint

## Playbook Inputs
---

| **Name** | **Description** | **Default Value** | **Required** |
| --- | --- | --- | --- |
| AutoCollectinvestigationPackege | Choose if to skip user validation on retrieving the Investigation pack within the provided assets. | True | Optional |
| Hostnames | Comma-separated values of hostnames |  | Optional |
| MachineIDs | Comma-separated values of machine IDs |  | Optional |
| IPs | Comma-separated values of machine IPs |  | Optional |

## Playbook Outputs
---
There are no outputs for this playbook.

## Playbook Image
---
![Microsoft Security Defender For Endpoint - Collect investigation package ](../doc_files/Microsoft_Defender_For_Endpoint_-_Collect_investigation_package.png)