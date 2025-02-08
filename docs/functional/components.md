---
layout: guide
title: Core Components
parent: Functional Documentation
nav_order: 2
---

# Core Components

## Container Manager (Rust)
- Lifecycle management (create/delete containers).
- Hardware permission API (`GET /hardware`, `POST /attach_device`).

## Hardware Proxy (Rust + eBPF)
- Syscall interception/redirection.
- Virtual device emulation (e.g., `/dev/virtual_bt`).

## Security Layer
- eBPF-powered syscall validation.
- TPM-signed audit logs.

## Communication Module
- Async I/O with `tokio`.
- mTLS handshake via `rustls`.
