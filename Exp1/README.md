# Experiment 1: Performance Analysis of Type-1 and Type-2 Hypervisors

## 1. Aim

To study and compare the performance of a Type-1 hypervisor and a Type-2 hypervisor by creating similarly configured virtual machines and performing CPU performance analysis using Sysbench.

The experiment uses:

- Proxmox VE as the Type-1 hypervisor
- VMware Workstation as the Type-2 hypervisor
- Ubuntu as the guest operating system
- Sysbench as the CPU benchmarking tool

---

# 2. Objectives

1. To understand the concept of virtualization and hypervisors.
2. To study Type-1 and Type-2 hypervisors.
3. To create and configure a virtual machine using Proxmox VE.
4. To create and configure a virtual machine using VMware Workstation.
5. To use comparable CPU, memory and disk configurations in both virtual machines.
6. To install and configure Ubuntu as the guest operating system.
7. To verify CPU, memory and disk configurations.
8. To monitor system resource utilization.
9. To install and use Sysbench for CPU performance analysis.
10. To record benchmark results from both virtualization environments.
11. To compare the measured performance of Type-1 and Type-2 hypervisors.

---

# 3. Introduction

Virtualization is a technology that allows a physical computer's resources to be used to create one or more virtual machines.

A virtual machine behaves like an independent computer and can run its own operating system and applications.

A hypervisor, also called a Virtual Machine Monitor (VMM), manages virtual machines and provides access to the underlying computing resources.

Hypervisors are mainly classified into two types:

- Type-1 Hypervisor
- Type-2 Hypervisor

---

# 4. Types of Hypervisors

## 4.1 Type-1 Hypervisor

A Type-1 hypervisor, also known as a bare-metal hypervisor, runs directly on the physical hardware.

The basic architecture is:

```text
Physical Hardware
       |
       v
Type-1 Hypervisor
       |
       +----------------+
       |                |
       v                v
 Virtual Machine 1   Virtual Machine 2
       |
       v
 Guest Operating System
