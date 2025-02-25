---
layout: "checkpoint"
page_title: "checkpoint_management_proxmox_data_center_server"
sidebar_current: "docs-checkpoint-Resource-checkpoint-management-proxmox-data-center-server"
description: |- Use this data source to get information on an existing Proxmox Data Center Server.
---

# Resource: checkpoint_management_proxmox_data_center_server

Use this data source to get information on an existing Proxmox Data Center Server.

## Example Usage

```hcl
resource "checkpoint_management_proxmox_data_center_server" "testProxmox" {
  name     = "MyProxmox"
  username = "USERNAME"
  realm    = "REALM"
  token_id = "TOKEN_ID"
  secret   = "SECRET"
  hostname = "HOSTNAME"
}

data "checkpoint_management_proxmox_data_center_server" "data_proxmox_data_center_server" {
  name = "${checkpoint_management_proxmox_data_center_server.testProxmox.name}"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Optional) Object name.
* `uid` - (Optional) Object unique identifier.
