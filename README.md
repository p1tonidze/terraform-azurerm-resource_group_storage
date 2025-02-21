# Terraform Azure Resource Group and Storage Account Module

This Terraform module creates an Azure Resource Group and an Azure Storage Account. It provides a simple way to provision these essential resources within a specified region.

---
## Features:

* Creates an Azure Resource Group.
* Provisions an Azure Storage Account within the created resource group.
* Outputs the IDs of both the Resource Group and Storage Account for reference.
---
## Requirements:

* Terraform: v1.0.0 or higher
* Azure Provider: v3.0 or higher
* Azure Subscription
---
## Usage:

```hcl
module "resource_group_storage" {
  source                = "p1tonidze/resource_group_storage"
  version               = "1.0.0"
  resource_group_name   = "my-resource-group"
  storage_account_name  = "mystorageaccount"
  location              = "West US"
}
```
---
## Inputs:

| Variable Name          | Description                             | Default Value             | Required |
|------------------------|-----------------------------------------|---------------------------|----------|
| `resource_group_name`  | The name of the resource group          | `"example-resources"`     | No       |
| `storage_account_name` | The name of the storage account         | `"examplestorageaccount"` | No       |
| `location`             | The location for all resources          | `"East US"`               | No       |
---
## Outputs:

| Output Name            | Description                                  |
|------------------------|----------------------------------------------|
| `resource_group_id`    | The ID of the created Resource Group         |
| `storage_account_id`   | The ID of the created Storage Account        |
---
## Example Deployment:

1. Initialize Terraform:

```hcl
terraform init
```

2. Plan the deployment:

```hcl
terraform plan
```

3. Apply the configuration:

```hcl
terraform apply
```
