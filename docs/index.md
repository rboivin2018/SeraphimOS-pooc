---
layout: default
title: ContainOS Documentation
---

# ContainOS Documentation

Welcome to the official documentation for **ContainOS**, a minimal, container-centric OS with hardware isolation.

## Table of Contents
- **Functional Documentation**
  - [Architecture Overview]({{ '/functional/architecture' | relative_url }})  
  - [Core Components]({{ '/functional/components' | relative_url }})  
  - [Example Workflows]({{ '/functional/workflows' | relative_url }})  

- **Advanced Security Guide**  
  - [Threat Model]({{ '/security/threat-model' | relative_url }})  
  - [Exploit Mitigations]({{ '/security/mitigations' | relative_url }})  
  - [Security Playbook]({{ '/security/playbook' | relative_url }})  

---

## Getting Started
1. Clone the repo:  
   ```bash
   git clone https://github.com/your-repo/containos.git
   ```
2. Build the container manager:
   ```bash
   cargo build --release --target x86_64-unknown-linux-musl
   ```
