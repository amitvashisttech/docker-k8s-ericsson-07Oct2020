# Docker VM Installation & Configuration.

## GCP Cloud Platform 

## Create a Firewall by Going into VPC Network Section -> Firewall
```
Name     	: k8s-demo
Tag          	: k8s-demo
IP Range 	: 0.0.0.0/0
Protocol 	: tcp
Ports   		: 80,8000-9000,30000-33000
```

## Create a VM by Going into the Compute Engine Section -> Create New VM. 

-> Keep everything default except the below parameters. 
```
  1. Change Boot Disk : Ubuntu 16.04
  2. Firewall -> Networking -> Network tags : k8s-demo
  3. Firewall -> Allow ( Http & Https )
```
