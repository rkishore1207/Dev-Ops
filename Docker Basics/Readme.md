# Docker
## What is Docker?
* We developed one application in our local machine and if we run our application in different machine it won't run properly.
* Because
    1. one or more files are missing
    2. Software versions are mismatching
    3. Different configuration settings
* Hence **Docker** comes to rescue this problems by make every applications to run in an **isolated environments** (Containers).
## Virtual Machines vs Containers
* One physical machine can run more virtual machines (*instances*) by the help of `Hypervisor` -> it is also a software to manage instances.
* Some of the Hypervisors are
    1. Virtual Box
    2. VM ware
    3. Hyper-V -> especially for windows
* For example one physical machine is running two VMs and one VM is execute one application having *node version 13* and another VM execute completely different application having *node version 9*.
* Hence it is possible to execute multiple application simultaneously with the help of `Vitual Machines`.
* But here are some prob lems,
    1. Each VM need full blown Os
    2. Slow to start 
    3. Resource Intensive
### Containers
* It also having the capability of doing the same thing but,
    1. Allows multiple apps in isolation
    2. Lightweight
    3. Use OS of the host
    4. Start quickly
    5. Need less hardware resource
