# terraform-azurerm-os-calculator
[Heavily inspired form Terraform Azure Compute Module](https://github.com/Azure/terraform-azurerm-compute)

Designed to be used with Libre DevOps VM modules, and will simplify the way of getting SKUs for your VM images without having to look it up.

Simple pass the OS you want to the variable, and it will output the values of the publisher, offer and SKU.  All versions are latest

```hcl
module "os_calculator" {
  source = "github.com/libre-devops/terraform-azurerm-linux-os-sku-with-plan-calculator"

  vm_os_simple = "CISUbuntu20.04L1" // will give you CIS Ubuntu20.04l1 sku properties, to be used in linux-vm module
}
```

For a full example build, check out the [Libre DevOps Website](https://www.libredevops.org/quickstart/utils/terraform/using-lbdo-tf-modules-example.html)

## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_storage_account.sa](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_standard_os"></a> [standard\_os](#input\_standard\_os) | n/a | `map` | <pre>{<br>  "CISCentOS7L1": "center-for-internet-security-inc,cis-centos-7-v2-1-1-l1,cis-centos7-l1",<br>  "CISCentOS8L1": "center-for-internet-security-inc,cis-centos-8-l1,cis-centos8-l1",<br>  "CISDebian10L1": "center-for-internet-security-inc,cis-debian-linux-10-l1,cis-debian10-l1",<br>  "CISDebian9L1": "center-for-internet-security-inc,cis-debian-linux-9-l1,cis-debian9-l1",<br>  "CISOracleLinux7L1": "center-for-internet-security-inc,cis-oracle-linux-7-v2-0-0-l1,cis-oracle7-l1-for-cis",<br>  "CISOracleLinux8L1": "center-for-internet-security-inc,cis-oracle-linux-8-l1,cis-oracle8-l1",<br>  "CISRHEL7L1": "center-for-internet-security-inc,cis-rhel-7-v2-2-0-l1,cis-rhel7-l1",<br>  "CISRHEL7L2": "center-for-internet-security-inc,cis-rhel-7-l2,cis-rhel7-l2",<br>  "CISRHEL8L1": "center-for-internet-security-inc,cis-rhel-8-l1,cis-rhel8-l1",<br>  "CISRHEL8L2": "center-for-internet-security-inc,cis-rhel-8-l2,cis-rhel8-l2",<br>  "CISSUSE15L1": "center-for-internet-security-inc,cis-suse15-l1,cis-suse15-l1",<br>  "CISUbuntu18.04L1": "center-for-internet-security-inc,cis-ubuntu-linux-1804-l1,cis-ubuntu1804-l1",<br>  "CISUbuntu20.04L1": "center-for-internet-security-inc,cis-ubuntu-linux-2004-l1,cis-ubuntu2004-l1"<br>}</pre> | no |
| <a name="input_vm_os_simple"></a> [vm\_os\_simple](#input\_vm\_os\_simple) | If using this module, pass one of the keys as the variable to get that image properties | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_calculated_value_os_offer"></a> [calculated\_value\_os\_offer](#output\_calculated\_value\_os\_offer) | Gets the offer value |
| <a name="output_calculated_value_os_publisher"></a> [calculated\_value\_os\_publisher](#output\_calculated\_value\_os\_publisher) | Gets the offer value |
| <a name="output_calculated_value_os_sku"></a> [calculated\_value\_os\_sku](#output\_calculated\_value\_os\_sku) | Gets the OS value |
## Requirements

No requirements.

## Providers

No providers.

## Modules

No modules.

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_standard_os"></a> [standard\_os](#input\_standard\_os) | n/a | `map` | <pre>{<br>  "CISCentOS7L1": "center-for-internet-security-inc,cis-centos-7-v2-1-1-l1,cis-centos7-l1",<br>  "CISCentOS8L1": "center-for-internet-security-inc,cis-centos-8-l1,cis-centos8-l1",<br>  "CISDebian10L1": "center-for-internet-security-inc,cis-debian-linux-10-l1,cis-debian10-l1",<br>  "CISDebian9L1": "center-for-internet-security-inc,cis-debian-linux-9-l1,cis-debian9-l1",<br>  "CISOracleLinux7L1": "center-for-internet-security-inc,cis-oracle-linux-7-v2-0-0-l1,cis-oracle7-l1-for-cis",<br>  "CISOracleLinux8L1": "center-for-internet-security-inc,cis-oracle-linux-8-l1,cis-oracle8-l1",<br>  "CISRHEL7L1": "center-for-internet-security-inc,cis-rhel-7-v2-2-0-l1,cis-rhel7-l1",<br>  "CISRHEL7L2": "center-for-internet-security-inc,cis-rhel-7-l2,cis-rhel7-l2",<br>  "CISRHEL8L1": "center-for-internet-security-inc,cis-rhel-8-l1,cis-rhel8-l1",<br>  "CISRHEL8L2": "center-for-internet-security-inc,cis-rhel-8-l2,cis-rhel8-l2",<br>  "CISSUSE15L1": "center-for-internet-security-inc,cis-suse15-l1,cis-suse15-l1",<br>  "CISUbuntu18.04L1": "center-for-internet-security-inc,cis-ubuntu-linux-1804-l1,cis-ubuntu1804-l1",<br>  "CISUbuntu20.04L1": "center-for-internet-security-inc,cis-ubuntu-linux-2004-l1,cis-ubuntu2004-l1",<br>  "RockyLinux8FreeGen2": "erockyenterprisesoftwarefoundationinc1653071250513,rockylinux,free"<br>}</pre> | no |
| <a name="input_vm_os_simple"></a> [vm\_os\_simple](#input\_vm\_os\_simple) | If using this module, pass one of the keys as the variable to get that image properties | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_calculated_value_os_offer"></a> [calculated\_value\_os\_offer](#output\_calculated\_value\_os\_offer) | Gets the offer value |
| <a name="output_calculated_value_os_publisher"></a> [calculated\_value\_os\_publisher](#output\_calculated\_value\_os\_publisher) | Gets the offer value |
| <a name="output_calculated_value_os_sku"></a> [calculated\_value\_os\_sku](#output\_calculated\_value\_os\_sku) | Gets the OS value |
