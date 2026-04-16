# PFSense Installation

```
> Download ISO

https://pfsense.com/download/

> Upload ISO to Proxmox
> 2 network port is required/attached to the VM pfsense
> 2 network needs to available on PVE
```

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

```
> select the vm pfsense
> option
> start at boot [checked]
```
