# Experiment 1: Performance Analysis of Type-1 and Type-2 Hypervisors

## 1. Aim

To study the working of Type-1 and Type-2 hypervisors and analyze their performance using virtual machines, system resource monitoring, and CPU benchmarking with Sysbench.

---

## 2. Objectives

1. To understand the concept of hypervisors and virtualization.
2. To study Type-1 and Type-2 hypervisors.
3. To create and configure a virtual machine using Proxmox VE.
4. To create and configure a virtual machine using VMware Workstation.
5. To monitor CPU, memory, disk, and system resource utilization.
6. To perform CPU benchmarking using Sysbench.
7. To compare the performance of Type-1 and Type-2 hypervisors using the obtained benchmark results.

---

## 3. Introduction

A hypervisor, also known as a Virtual Machine Monitor (VMM), is software or a virtualization layer that allows multiple virtual machines to run on a physical computer.

Hypervisors are mainly classified into two types:

- Type-1 Hypervisor
- Type-2 Hypervisor

### 3.1 Type-1 Hypervisor

A Type-1 hypervisor, also called a bare-metal hypervisor, runs directly on the physical hardware. It manages the hardware resources and provides virtual machines with the required resources.

In this experiment, **Proxmox VE** is used as the Type-1 hypervisor.

### 3.2 Type-2 Hypervisor

A Type-2 hypervisor, also called a hosted hypervisor, runs on top of a host operating system. The virtual machines are created and managed through the host operating system.

In this experiment, **VMware Workstation** is used as the Type-2 hypervisor.

---

# 4. Experimental Environment

| Parameter | Type-1 Environment | Type-2 Environment |
|---|---|---|
| Hypervisor | Proxmox VE | VMware Workstation |
| Hypervisor Type | Type-1 | Type-2 |
| Guest Operating System | Ubuntu | Ubuntu |
| Benchmark | Sysbench | Sysbench |
| Main Performance Test | CPU Benchmark | CPU Benchmark |

The virtual machines are configured with comparable resources so that the benchmark results can be used for performance analysis.

---

# 5. Type-1 Hypervisor: Proxmox VE

## 5.1 Proxmox Dashboard

The Proxmox VE environment was accessed and the virtual machine management interface was verified.

![Proxmox Dashboard](Type1-Proxmox/01-proxmox-dashboard.png)

---

## 5.2 Virtual Machine Configuration

A virtual machine was created in Proxmox VE with the required CPU, memory, storage, and network configuration.

The VM configuration includes:

- 2 CPU cores
- 2 GB memory
- 20 GB virtual disk
- Ubuntu operating system
- Virtual network interface

![Proxmox VM Configuration](Type1-Proxmox/02-proxmox-vm-configuration.png)

---

## 5.3 Virtual Machine Running Status

The created virtual machine was started successfully and its resource utilization was observed through the Proxmox interface.

![Proxmox VM Running](Type1-Proxmox/03-proxmox-vm-running.png)

---

## 5.4 Ubuntu System Information

The guest operating system and virtualization environment were verified using:

```bash
hostnamectl
