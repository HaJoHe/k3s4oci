# k3s4oci
K3S Cluster running on Oracle Cloud Infrastructure as always free

Description how to setup a cluster including a glusterfs for locsl storage

* Disable Scheduling on Master node
kubectl taint nodes master-node node-role.kubernetes.io/master=effect:NoSchedule
