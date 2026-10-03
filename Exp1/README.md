# Experiment 1: Performance Analysis of Type-1 and Type-2 Hypervisors

## 1. Aim

To study Type-1 and Type-2 hypervisors and analyze their performance using virtual machines, system resource monitoring, and CPU benchmarking with Sysbench.

---

## 2. Objectives

1. To understand the concept of virtualization and hypervisors.
2. To study Type-1 and Type-2 hypervisors.
3. To create and configure a virtual machine using Proxmox VE.
4. To create and configure a virtual machine using VMware Workstation.
5. To monitor CPU, memory, disk, and system resource utilization.
6. To perform CPU benchmarking using Sysbench.
7. To compare the performance of Type-1 and Type-2 hypervisors using the obtained results.

---

## 3. Introduction

A hypervisor, also known as a Virtual Machine Monitor (VMM), is a virtualization layer that allows virtual machines to run on a physical computer.

Hypervisors are mainly classified into two types:

- Type-1 Hypervisor
- Type-2 Hypervisor

### 3.1 Type-1 Hypervisor

A Type-1 hypervisor, also called a bare-metal hypervisor, runs directly on the physical hardware. It manages the hardware resources and provides virtual machines with the required resources.

In this experiment, Proxmox VE is used as the Type-1 hypervisor.

### 3.2 Type-2 Hypervisor

A Type-2 hypervisor, also called a hosted hypervisor, runs on top of a host operating system. The host operating system provides the underlying hardware interaction for the virtual machines.

In this experiment, VMware Workstation is used as the Type-2 hypervisor.

---

## 4. Hypervisor Architecture

The basic difference between Type-1 and Type-2 hypervisors can be represented as follows.

```mermaid
flowchart TB

    subgraph Type1["Type-1 Hypervisor"]
        H1["Physical Hardware"]
        HYP1["Proxmox VE"]
        VM1["Ubuntu Virtual Machine"]

        H1 --> HYP1
        HYP1 --> VM1
    end

    subgraph Type2["Type-2 Hypervisor"]
        H2["Physical Hardware"]
        OS["Host Operating System"]
        HYP2["VMware Workstation"]
        VM2["Ubuntu Virtual Machine"]

        H2 --> OS
        OS --> HYP2
        HYP2 --> VM2
    end
