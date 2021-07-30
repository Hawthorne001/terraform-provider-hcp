---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "hcp_hvn_peering_connection Data Source - terraform-provider-hcp"
subcategory: ""
description: |-
  The HVN peering connection data source provides information about an existing peering connection between HVNs.
---

# hcp_hvn_peering_connection (Data Source)

The HVN peering connection data source provides information about an existing peering connection between HVNs.

## Example Usage

```terraform
data "hcp_hvn_peering_connection" "test" {
  peering_id = var.peering_id
  hvn_1      = var.hvn_1
  hvn_2      = var.hvn_2
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **hvn_1** (String) The unique URL of one of the HVNs being peered.
- **hvn_2** (String) The unique URL of one of the HVNs being peered.
- **peering_id** (String) The ID of the peering connection.

### Optional

- **id** (String) The ID of this resource.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- **created_at** (String) The time that the peering connection was created.
- **expires_at** (String) The time after which the peering connection will be considered expired if it hasn't transitioned into `ACCEPTED` or `ACTIVE` state.
- **organization_id** (String) The ID of the HCP organization where the peering connection is located. Always matches the HVNs' organization.
- **project_id** (String) The ID of the HCP project where the peering connection is located. Always matches the HVNs' project.
- **self_link** (String) A unique URL identifying the peering connection

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **default** (String)

