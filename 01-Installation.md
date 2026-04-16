# PFSense Installation

## preparation
```
> Download ISO

https://pfsense.com/download/

> Upload ISO to Proxmox
> 2 network port is required/attached to the VM pfsense
> 2 network needs to available on PVE
```

## PFSense VM Creation
```
> Create the VM over Proxmox
> VM name and other details
> [optional] you can add the tag for filter the vm
> Mount the pfsense.iso
> Type: linux
> Disk: 25 GiB [5 GiB is fine to install]
> CPU: 1
> Memory: 2 [1 GiB is fine]
> Network: Bridge [vmbr0] default
> Finished
```

## Additional Network setup
```
> Dont start the VM
> Add additional network interface
```



```
> select the vm pfsense
> Hardware
> network
> add network
> bridge : [vmbr1]
```
## Start vm at pve boot

```
> select the vm pfsense
> option
> start at boot [checked]
```

## PFSense Installation
```
> Start the vm
> Accept the license
> Install : install pfsense [ok]
> Partitioning: Auto ZFS [ok]
> ZFS Configuration: Install Process with Installation [select]  
  stripe - no redundancy [ok]
  [space] to selete : da0 qumu harddisk [ok]
  [yes]
> reboot
```

```
> Enter thre WAN Interface: vtnet0 [for internet, external]
> Enterr the LAN Interface: vtnet1
> Do you want to process: y 
```


```
> Get the LAN IP and try to access over browser
> Username: admin
> Password: pfsense
> next
> next

[General Setup]
> Hostname: pfsense
> Domain: cloud-lab.j2ctechnologies.com
> Primary dns: 
> Secondary dns:

[Time server]
> Time server hostname:
> Timezone

[Network setup]
> Select type: static
> Ip details

[LAN Interface]
>
>

[Set Admin Password]
> Admin password:
> Admin password again:

```
