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
* To see a particular property from the object, then we have to parse it down (Json Parser and YAML parser).
* az storage account list | jq '.[].encryption.services.blob.enabled'
* Another way, az storage account list --query '[].encryption.services.blob.enabled' (available only in azure cli).
> To install new package, sudo apt update -> sudo apt install <Name>(jq)

### Communicate with API using Shell script
* Instead of GUI(Graphical User Interface), we can communicate to a system by **programmatically** with API(Application Programming Interface).
* There are lot **modules** present on each fields such as `Request` is the Module for **Python**, `cURL` is the module for **Shell**, etc..
* To know the exact api url, we have to look into that particular organization's **API Doc Reference**.
* Kubernetes's cli is `KubeCTL`.

### Version Control System
1. Centralized Version Control System (CVCS):
- This VCS only have one Central place to share the codes.
- We can't clone it into our local machine.
- So, If we want to commit, it needs Network connection to commit into Central Repo.
- Risk of Data Loss

2. Distributed Version Control System (DVCS):
- This VCS allows to clone into the respective devs machine.
- We can Do branching and Merging strategies in order to deliver perfect code base
- We can do local commit, without internet
- No worry about Data loss, because we have copy in our local machine
- Fast compare to CVCS

#### Files inside a .git Folder
1. `HEAD`
2. `config` - used to configure the **user credential**
3. `hooks` - used to prevent the unintentionally committing **Passwords and user tokens**
4. `Objects and Refs` - Git consider all files and everything as a Objects