[![StarApp-Infra-Release](https://github.com/diegodocs/starapp-infra-release/actions/workflows/terraform-starapp-release.yml/badge.svg)](https://github.com/diegodocs/starapp-infra-release/actions/workflows/terraform-starapp-release.yml)

# Starapp-Infra-Release
<<<<<<< HEAD

This repository you can find files regarding infrastructure creation for Star Application (StarApp).

## Usage example

```hcl
module "deploy_starapp" {
    
    source = "./modules/vm"
    
    #VM        
    business_product_name       = "starapp"
    
    #NETWORK
    vnet_resource_group_name    = "dev-governance-rg-001"
    vnet_name                   = "dev-br-vnet-001"
    subnet_name                 = "dev-br-snet-001"
    
    #SIZE                       
    vm_size                     = "Standard_B1s"
    vm_publisher                = "MicrosoftWindowsServer"
    vm_offer                    = "WindowsServer"
    vm_sku                      = "2022-Datacenter"
    vm_version                  = "latest"        

    #GOVERNANCE
    owner                       = "devteam@test.io"
    costcenter                  = "123456-001"  
    monitoring                  = true  
    env                         = "dev"
          
}
```

## You shouldn't find:
- Secrets or sensitive info hardcoded committed to source control.
- Unnecessary project or library references or third party frameworks.
- Binaries
=======
>>>>>>> 6ff198d88b4dc6d3f1c42ccac10ee2a20ebeb69b
