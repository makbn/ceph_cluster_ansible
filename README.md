### Ceph Ansible playbook

Install and configure a Ceph (Nautilus) Cluster on CentOS 7 Servers with 2 compute nodes and a single monitoring server. Change Inventory to add/remove mode nodes.

- Disclaimer: I wrote this playbook just as a practise for learning Ansible, use at your own risk!

### Inventory

Change the list of nodes inside `/inventory/hosts` [file](https://github.com/makbn/ceph_cluster_ansible/blob/master/inventory/hosts)

```
[ceph-controller]
192.168.1.30

[ceph-compute]
192.168.1.31
192.168.1.32

[ceph-monitor]
192.168.1.33  

[all]
192.168.96.128
#192.168.1.30
#192.168.1.31
#192.168.1.32
#192.168.1.33
```

### How To
After running the playbook, you need to disks as OSD using the following commands:

```bash
ceph-deploy osd create --data {disk}
```
