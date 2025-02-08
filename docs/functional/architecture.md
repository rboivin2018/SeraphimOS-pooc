---
layout: guide
title: Architecture Overview
parent: Functional Documentation
nav_order: 1
---

# Architecture Overview

## Master-Slave Model
- **Master Container**: Exclusive hardware access (GPIO, USB, Bluetooth, etc.).
- **Slave Containers**: Isolated environments where apps interact with hardware via the master.
- **Container Manager**: Rust-based orchestration layer for lifecycle, security, and communication.

## Communication Flow
{% include mermaid.html %}

graph TD
  User[Slave Container Apps] -->|Proxied Syscalls| CM[Container Manager]
  CM -->|mTLS| Master[(Master Container)]
  Master -->|Hardware Access| HW[GPU/USB/Bluetooth]
  CM --> Sec[Security Layer]
  Sec --> eBPF[eBPF Filters]
  Sec --> SecComp[Seccomp Policies]

---

**See Also**  
- [Example Workflows]({{ '/functional/workflows' | relative_url }})  
- [Threat Model]({{ '/security/threat-model' | relative_url }})  
