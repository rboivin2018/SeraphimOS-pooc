---
layout: guide
title: Example Workflows
parent: Functional Documentation
nav_order: 3
---

# Example Workflows

## Bluetooth Device Access
1. **User Action**: A slave app runs `hcitool scan`.
2. **Syscall Interception**: The Container Manager’s `eBPF` program detects the `ioctl` call on `/dev/hci0`.
3. **Proxy Daemon**: The master’s daemon receives the request, activates Bluetooth via `rfkill`, and returns scan results.
4. **User Perception**: The slave app behaves as if it directly scanned for devices.

## Dynamic Hardware Allocation
1. **User Request**: `POST /hardware/assign {device: "bluetooth", slave: "container-id"}`.
2. **Master Handling**: Configures device permissions via cgroups.
3. **Slave Access**: The slave interacts with `/dev/virtual_bt`.
