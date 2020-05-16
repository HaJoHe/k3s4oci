# k3s4oci
K3S Cluster running on Oracle Cloud Infrastructure as always free

## Motivation
Running K3S on an OCI Cloud is probably the cheapest way to play arround with kubernetes as a cluster.
Well, the 2 VMs offered as always free are not high perfomance VMs, but it's enough power to serve a NEXTCLOUD instance and some more funny things.

Description how to setup a cluster including a glusterfs for locsl storage

* ### Disable Scheduling on Master node
it's probably a good idea for not overcharging the Master VM, to disable workload on this node. I personally found, that playing arround with some uncorrect yaml ;-), ... k3s is running in high load very easyly, and ends with refusing to accept commands. Solution: systemctl restart k3s... or 
 <br/>kubectl taint nodes master-node node-role.kubernetes.io/master=effect:NoSchedule
