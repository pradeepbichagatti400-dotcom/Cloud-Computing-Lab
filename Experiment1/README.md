# Experiment 1: Performance Analysis of Type-1 and Type-2 Hypervisors

## Aim

To study and analyze the performance of Type-1 and Type-2 hypervisors by creating similarly configured virtual machines and performing system resource monitoring and CPU benchmarking using Sysbench.

---

## Objectives

- To understand the concept of Type-1 and Type-2 hypervisors.
- To create and configure a virtual machine using Proxmox VE.
- To create and configure a virtual machine using VMware Workstation.
- To analyze CPU, memory, disk and system resource utilization.
- To perform CPU benchmarking using Sysbench.
- To compare the performance of Type-1 and Type-2 hypervisors based on the obtained benchmark results.

---

# 1. Introduction

A hypervisor, also known as a Virtual Machine Monitor (VMM), is a virtualization layer that allows multiple virtual machines to run on a physical computer.

Hypervisors are broadly classified into two types:

- Type-1 Hypervisor
- Type-2 Hypervisor

### Type-1 Hypervisor

A Type-1 hypervisor, also called a bare-metal hypervisor, runs directly on the physical hardware and provides virtualization services to virtual machines.

**Example used in this experiment:** Proxmox VE.

### Type-2 Hypervisor

A Type-2 hypervisor, also called a hosted hypervisor, runs on top of an existing host operating system and provides virtualization through the host operating system.

**Example used in this experiment:** VMware Workstation.

---

# 2. Experimental Setup

The experiment consists of two virtualization environments:

| Hypervisor         |  Type  | Virtual Machine |
|--------------------|--------|-----------------|
|     Proxmox VE     | Type-1 |     Ubuntu      |
| VMware Workstation | Type-2 |     Ubuntu      |

The virtual machines are configured with similar resources so that their performance can be compared using the same benchmarking procedure.

---

# 3. Type-1 Hypervisor – Proxmox VE

## 3.1 Virtual Machine Configuration

A virtual machine was created in Proxmox VE with the required CPU, memory, storage and networking configuration.

![Virtual Machine Configuration](01_create_vm.png)

---

## 3.2 Virtual Machine Resource Overview

The Proxmox VE virtual machine was started and its resource allocation and current resource usage were observed.

![Virtual Machine Summary](02_vm_summary.png)

---

## 3.3 Operating System and Virtualization Details

The operating system and virtualization environment were verified using the system information.

```bash
hostnamectl
