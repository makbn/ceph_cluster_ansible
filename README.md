### Ceph Ansible playbook

Install and configure a Ceph (Nautilus) Cluster on CentOS 7 Servers with 2 compute nodes and a single monitoring server. Change Inventory to add/remove mode nodes.

- Disclaimer: I wrote this playbook just as a practise for learning Ansible, use at your own risk!

### Inventory

Change list of nodes inside `/inventory/hosts` 

### How To
After running the playbook, you need to disks as OSD using the following commands:

```bash
ceph-deploy osd create --data {disk}
```
