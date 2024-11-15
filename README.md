# terraform-azurerm-module-ubuntu-24.04-app

# module-ubuntu-24.04-app/azurerm

## Description
 Terraform module for Ubuntu 24.04 application deployment on Microsoft Azure

## Deployment
This module creates a single instance having a single network interface.

## Usage
```tf
module "App" {
	source  = "armdupre/module-ubuntu-linux-app/azurerm"
	Eth0SubnetId = module.Vnet.PublicSubnet.id
	ResourceGroupName = azurerm_resource_group.ResourceGroup.name
	SshKeyName = azurerm_ssh_public_key.SshKey.name
}
```