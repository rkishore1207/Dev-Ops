# Dev-Ops
Learn basics and advanced concepts of dev-ops

#### What is DevOps
 - Improving Delivery
 - Automation
 - Quality
 - Continuous Monitoring
 - Continuous Testing

### Virtual Machines
- `Hypervisor` is the software or tool that helps the physical server (host machine) to separate a mulitple VMs by allocating Memory and Processor efficiently.
- All Physical Server has Hypervisor, but not all Desktops have Hypervisor on its own.
- If we want to create VMs on our own, then we have to install the Hypervisor manually. Eg, Oracle VirtualBox, VMware Workstation.
##### There are two types of Hypervisor
 * Bare-Metal (Installed directly on the Hardware), Eg-VMware ESXi, Hyper-v
 * Hosted (Install on the top of OS(Windows, Mac, Linux)), Eg-VirtualBox, VMware Workstation.

#### Use of DevOps in creating Resource
- If we want to create multiple number of Resources for the same specifications, then DevOps Engineers can write a script to create multiple number of Resource.

1. AWS CLI
2. AWS API
3. AWS CFT
4. Terraform (Use for all cloud provider)
5. AWS CDK

![Operating System](https://github.com/user-attachments/assets/2b3a47cd-7b36-4e07-aa76-df501e2fa237)

##### Kernel
* Kernel is the heart of OS. It helps the communication between OS and Hardware.
 1. Device Management
 2. Memory Management
 3. Process Management
 4. Handling System Parts

### Linux
* We are using Linux OS in the production level instead of Windows and Mac.
* Because,
 1. Fast
 2. Secure (No need of Antiviruses)
 3. Open Source
 4. Distributions

 ##### Why we move to cloud
  1. Management
  2. Cost Effective
* If we have a physical server, then we have to allocate some team to take care of this, but in cloud, we do not worry about that.
* In cloud, the charges will be based on **Pay as you go** so if we didn't use any resource, we are not getting paid, but in physical sever, Once we bought, then we have to pay the respective cost.
* But in Virtual Machine concept, if we created 100 VM's and didn't use it properly (not having enough developers to use) then those created cost will be wasted.
> So, we have to track it properly, that is `Tracking resource usage`

### Azure CLI
* az --version
* az login
* az account list
* az account list -o table (list accounts as table format)
* az account set --subscription <subscriptin ID>
* az account show (to view the current active subscription account)
* az group list
* vim <fileName.sh> (creating new executable shell file)
> while creating new shell file, it couldn't have any executable permission
* We have to explicitly given to it, once it got created
* chmod +x <fileName.sh>
* Once shell file is created, at the top we have to specify the shebang `#!/bin/bash`, then only this file will execute.
* Then specify the purpose of the script
``` shell
################
# Author - Kishore Ramesh
# Date - 04-05-2025
# Purpose - To list all the resources from the Portal
################

#list Storage accounts
echo "Listing Storage Accounts"
az storage account list -o table

#list Virtual Machines
echo "Listing Virtual Machines"
az vm list
```
* `echo` is used to print the value on the output
* az storage account list
* az vm list