# Experiment 1: Performance Analysis of Type-1 and Type-2 Hypervisors

## 1. Aim

To study Type-1 and Type-2 hypervisors by creating virtual machines and analyzing their system configuration, resource utilization, and CPU performance using Sysbench.

---

## 2. Objectives

- To understand the concept of virtualization.
- To understand the working of hypervisors.
- To study Type-1 and Type-2 hypervisors.
- To create and configure a virtual machine using a Type-1 hypervisor.
- To create and configure a virtual machine using a Type-2 hypervisor.
- To verify the CPU, memory, disk, and operating system configuration of the virtual machines.
- To monitor system resource utilization.
- To perform CPU benchmarking using Sysbench.
- To record the obtained performance results.
- To compare the performance of the two virtualization environments.

---

# 3. Introduction

Virtualization is a technology that allows a physical computer to create and run multiple virtual machines.

A virtual machine behaves like an independent computer and can run its own operating system and applications. The resources of the physical machine, such as CPU, memory, storage, and network, are allocated to the virtual machines.

A hypervisor is the software layer responsible for creating, running, and managing virtual machines. It controls the allocation of physical resources to the virtual machines.

Hypervisors are mainly classified into two types:

1. Type-1 Hypervisor
2. Type-2 Hypervisor

In this experiment, the following hypervisors are studied:

- Proxmox VE as the Type-1 hypervisor
- VMware Workstation as the Type-2 hypervisor

The performance of the virtual machines is analyzed using system monitoring and Sysbench CPU benchmarking.

---

# 4. Types of Hypervisors

## 4.1 Type-1 Hypervisor

A Type-1 hypervisor is also called a bare-metal hypervisor.

It runs directly on the physical hardware without requiring a conventional host operating system between the hardware and the hypervisor.

The basic structure is:

```text
Physical Hardware
       |
       v
Type-1 Hypervisor
       |
       v
Virtual Machine
       |
       v
Guest Operating System
