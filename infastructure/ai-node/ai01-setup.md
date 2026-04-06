# AI Utility Node Deployment — AI01

## Overview

This document outlines the deployment of a lightweight AI utility node (AI01) using a Raspberry Pi 4. This node is designed to support the Active Directory lab with future capabilities such as log analysis, security triage, and automation.

## Purpose

* Provide local AI-assisted analysis (offline)
* Support future SOC-style workflows
* Assist with PowerShell and AD-related tasks
* Enable documentation generation

---

## System Configuration

| Component  | Value                               |
| ---------- | ----------------------------------- |
| Hostname   | AI01                                |
| Device     | Raspberry Pi 4                      |
| OS         | Raspberry Pi OS Lite (64-bit)       |
| Network    | Home LAN (isolated from AD-LAB)     |
| AI Runtime | Ollama                              |
| Model      | Gemma (2B parameter, CPU inference) |

---

## Network Design

AI01 is intentionally **not connected** to the AD-LAB internal network during initial deployment.

| Network  | Access        |
| -------- | ------------- |
| Home LAN | Enabled       |
| AD-LAB   | Not connected |

This ensures:

* Clean AD deployment baseline
* No interference with domain services
* Reduced troubleshooting complexity

---

## Installation Steps

### 1. System Preparation

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git htop ufw
```

---

### 2. Hostname Configuration

```bash
sudo hostnamectl set-hostname AI01
```

---

### 3. Firewall Configuration (UFW)

```bash
sudo ufw reset
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow from 192.168.1.0/24 to any port 22
sudo ufw allow from 192.168.1.0/24 to any port 11434
sudo ufw enable
```

---

### 4. Install Ollama

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

---

### 5. Run Gemma Model

```bash
ollama run gemma:2b
```

---

### 6. Enable Service

```bash
sudo systemctl enable ollama
```

---

## Security Considerations

* Default deny inbound firewall policy enforced
* Access restricted to local subnet (192.168.1.0/24)
* No external exposure of AI API (port 11434)
* Node is not domain-joined
* No integration with AD at this stage

---

## Performance Notes

* CPU-only inference (Raspberry Pi 4 limitation)
* Suitable for:

  * Lightweight queries
  * Log summarization (future)
* Not intended for heavy inference workloads

---

## Current Status

| Component         | Status                |
| ----------------- | --------------------- |
| AI Runtime        | Operational           |
| Model             | Loaded and functional |
| Network Isolation | Maintained            |
| AD Integration    | Not started           |

---

## Future Integration Plan

Planned in later phases:

* Connect AI01 to AD-LAB network
* Ingest Windows Event Logs from DC01
* Perform AI-assisted log analysis
* Support security detection workflows

---

## Outcome

Successfully deployed a lightweight AI utility node to simulate modern enterprise tooling and prepare for future security-focused automation within the lab.
