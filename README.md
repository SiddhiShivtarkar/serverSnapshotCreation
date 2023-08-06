# serverSnapshotCreation
Creating server Snapshot to take backup of VM

This usecase is cloud automation usecase where we are creating snapshot in order to backup VM from disaster recovery. 
Tools: Ansible, Jenkins.

Snapshot is like taking image for taking backup of the VM, so this will capture image of VM along with OS, disks, memory, apps, data that VM is having at that time. so in future we can resttore that VM if required, without loosing data and this usecase helpful in disaster recovery. 

Steps: 
1) validate whether all the inputs are coming from SNOW.
2) Validate Instance (whether given host is present in specified zone and project or not, authenticate using service account, if host is not present fail the further execution.
3) Creating a snapshot (using ansible module, creating snapshot and at the end validating it, taking snapshot of all the disks attached to the host i.e. OS disk and data disk)
