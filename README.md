[![StarApp-Infra-Release](https://github.com/diegodocs/starapp-infra-release/actions/workflows/terraform-starapp-release.yml/badge.svg)](https://github.com/diegodocs/starapp-infra-release/actions/workflows/terraform-starapp-release.yml)

# 5 StarsApp-Infra-Release

This repository you can find files regarding infrastructure creation for 5 Stars Application (5starsApp).

## Usage example

```hcl
module "vm_001" {
    
    source = "./modules/vm"
    
    #VM        
    business_product_name = "5starsApp"
    owner      = "dev@test.io"
    costcenter = "123456-001"
    monitoring = true
    env        = "dev"
    suffix     = "001"

    #NETWORK
    vnet_resource_group_name = "dev-governance-rg-001"
    vnet_name                = "dev-br-vnet-001"
    subnet_name              = "dev-br-snet-001"

    #SIZE                       
    vm_size      = "Standard_B1s"
    vm_publisher = "MicrosoftWindowsServer"
    vm_offer     = "WindowsServer"
    vm_sku       = "2022-Datacenter"
    vm_version   = "latest"  
          
}
```

## You shouldn't find

- Secrets or sensitive info hardcoded committed to source control.
- Unnecessary project or library references or third party frameworks.
- Binaries
