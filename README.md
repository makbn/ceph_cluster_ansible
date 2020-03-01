### Ceph Ansible playbook

Install and configure Ceph (Nautilus) Cluster on CentOS 7 Servers with 2 compute nodes and a single monitoring server. Change Inventory to add/remove mode nodes.

- Disclaimer: I wrote this playbook just for learning Ansible, use at your own risk!

After running playbook, you need to disks as OSD using following commands:

```bash
ceph-deploy osd create --data {disk}
```
