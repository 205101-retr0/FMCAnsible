# getAllVrfEigrpPolicyModel

The getAllVrfEigrpPolicyModel operation handles configuration related to [/api/fmc_config/v1/domain/{domainUUID}/devices/devicerecords/{containerUUID}/routing/virtualrouters/{virtualrouterUUID}/eigrproutes](/paths//api/fmc_config/v1/domain/{domain_uuid}/devices/devicerecords/{container_uuid}/routing/virtualrouters/{virtualrouter_uuid}/eigrproutes.md) path.&nbsp;
## Description
**Retrieves, deletes, creates, or modifies the EIGRP associated for a specified virtual router with the specified ID. Also, retrieves list of all EIGRP.**

## Path Parameters
| Parameter | Required | Type | Description |
| --------- | -------- | ---- | ----------- |
| virtualrouterUUID | True | string <td colspan=3> Unique identifier of Virtual Router |
| containerUUID | True | string <td colspan=3> The container id under which this specific resource is contained. |
| domainUUID | True | string <td colspan=3> Domain UUID |

## Query Parameters
| Parameter | Required | Type | Description |
| --------- | -------- | ---- | ----------- |
| offset | False | integer <td colspan=3> Index of first item to return. |
| limit | False | integer <td colspan=3> Number of items to return. |
| expanded | False | boolean <td colspan=3> If set to true, the GET response displays a list of objects with additional attributes. |

## Example
```yaml
- name: Execute 'getAllVrfEigrpPolicyModel' operation
  cisco.fmcansible.fmc_configuration:
    operation: "getAllVrfEigrpPolicyModel"
    path_params:
        virtualrouterUUID: "{{ virtualrouter_uuid }}"
        containerUUID: "{{ container_uuid }}"
        domainUUID: "{{ domain_uuid }}"
    query_params:
        offset: "{{ offset }}"
        limit: "{{ limit }}"
        expanded: "{{ expanded }}"

```