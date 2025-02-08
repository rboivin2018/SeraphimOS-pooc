---
layout: guide
title: Threat Model
parent: Advanced Security Guide
nav_order: 1
---

# Threat Model

## Attack Surface
- **Container Escape**: Exploits in namespaces/cgroups.
- **Kernel Vulnerabilities**: eBPF verifier flaws, privilege escalations.
- **Hardware DMA Attacks**: Unauthorized memory access via PCI devices.

## Assumptions
- The master container is *trusted* but not *infallible*.
- Kernel-level isolation (namespaces/cgroups) is correctly configured.
