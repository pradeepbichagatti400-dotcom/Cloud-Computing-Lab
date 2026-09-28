# Experiment 1: Hypervisor Performance Analysis

> **Performance Analysis of Type-1 and Type-2 Hypervisors using Sysbench**

---

## 📌 Overview

This experiment analyzes and compares the performance of virtual machines running on two different types of hypervisors:

- **Type-1 Hypervisor:** Proxmox VE
- **Type-2 Hypervisor:** VMware Workstation

For a fair comparison, virtual machines are configured with the same basic resources and the same Ubuntu operating system. CPU performance is measured using **Sysbench**.

The experiment focuses on observing CPU performance, system configuration, resource utilization, and benchmark results for both hypervisor types.

---

## 🎯 Objectives

The main objectives of this experiment are:

- To understand the concept of Type-1 and Type-2 hypervisors.
- To create a virtual machine using **Proxmox VE**.
- To create a virtual machine using **VMware Workstation**.
- To configure comparable virtual machine resources in both environments.
- To analyze CPU, memory, disk, and system configuration.
- To perform CPU benchmarking using **Sysbench**.
- To record execution time, events, events per second, and latency.
- To observe resource utilization of the virtual machines.
- To compare the performance results obtained from both hypervisors.

---

## 🧠 Hypervisor Types

### Type-1 Hypervisor

A Type-1 hypervisor runs directly on the physical hardware and manages virtual machines without requiring a conventional host operating system underneath it.

In this experiment, **Proxmox VE** is used as the Type-1 hypervisor.

### Type-2 Hypervisor

A Type-2 hypervisor runs as an application on top of a host operating system and provides virtualization services to guest virtual machines.

In this experiment, **VMware Workstation** is used as the Type-2 hypervisor.

---

## 🖥️ Hypervisors Used

| Hypervisor | Type | Guest OS | Purpose |
|---|---|---|---|
| Proxmox VE | Type-1 | Ubuntu | CPU and resource performance analysis |
| VMware Workstation | Type-2 | Ubuntu | CPU and resource performance analysis |

---

## ⚙️ Standard Virtual Machine Configuration

The same basic virtual machine configuration is used for both hypervisors to support a fair performance comparison.

| Resource | Configuration |
|---|---|
| Guest Operating System | Ubuntu 22.04 or later |
| CPU | 2 vCPU |
| Memory | 2 GB RAM |
| Disk | 20 GB |
| Benchmark Tool | Sysbench |
| CPU Benchmark | `sysbench cpu --cpu-max-prime=20000 run` |

Both virtual machines should use the same resource configuration for the performance comparison.

---

## 🔬 Experimental Methodology

The experiment is performed in two parts.

### Part A — Type-1 Hypervisor

The virtual machine is created and tested using **Proxmox VE**.

The following activities are performed:

1. Access the Proxmox VE web interface.
2. Create a new virtual machine.
3. Configure Ubuntu as the guest operating system.
4. Allocate 2 vCPU.
5. Allocate 2 GB RAM.
6. Configure a 20 GB virtual disk.
7. Configure the virtual network.
8. Install Ubuntu.
9. Verify the VM configuration.
10. Analyze CPU configuration using `lscpu`.
11. Analyze memory configuration using `free -h`.
12. Analyze disk configuration using `df -h`.
13. Monitor system resources using `top`.
14. Install Sysbench.
15. Run the CPU benchmark.
16. Record the benchmark results.
17. Observe resource utilization from Proxmox VE.

Detailed implementation and screenshots:

➡️ **[Type-1 Proxmox](./Type1-Proxmox/README.md)**

---

### Part B — Type-2 Hypervisor

The virtual machine is created and tested using **VMware Workstation**.

The following activities are performed:

1. Launch VMware Workstation.
2. Create a new virtual machine.
3. Select the Ubuntu ISO image.
4. Configure the virtual machine.
5. Allocate 2 vCPU.
6. Allocate 2 GB RAM.
7. Configure a 20 GB virtual disk.
8. Configure the network adapter.
9. Install Ubuntu.
10. Verify the VM configuration.
11. Analyze CPU configuration using `lscpu`.
12. Analyze memory configuration using `free -h`.
13. Analyze disk configuration using `df -h`.
14. Monitor system resources using `top`.
15. Install Sysbench.
16. Run the CPU benchmark.
17. Record the benchmark results.
18. Observe the virtual machine resources.

Detailed implementation and screenshots:

➡️ **[Type-2 VMware](./Type2-VMware/README.md)**

---

## 🧪 System Verification Commands

The following Linux commands are used during the experiment.

### Host and Operating System Information

```bash
hostnamectl
