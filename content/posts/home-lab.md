---
title: "How I built my Home Lab"
date: '2026-03-20'
draft: false
---

Hi, today I will show how I built my home lab for practicing both red & blue team skills.
I used KVM (virt-manager) for virtualization since there are kernel problems in Ubuntu for VMware.
## Why KVM
- I chose KVM over VMware because of its native integration with the Linux kernel and better resource management.
Dealing with VMware's kernel module errors on Ubuntu was taking too much time, so I switched to a more robust, open-source solution.

### Target 1 -- Kali Linux:
- To perform network scanning, exploitation, and post-exploitation.
- 2 CPUs and 3 GB RAM -- enough for Kali
### Target 2 -- Windows 10:
- To monitor logs, set up Sysmon, and observe how real attacks look on a Windows target.
- 4 CPUs and 7 GB RAM -- because Windows wants more RAM for analyzing logs

![KVM Home Lab Setup](/images/lab-setup/lab-setup.png)

## Networking
Both VMs are connected to a NAT network, allowing them to communicate with each other while staying protected from the external network.
