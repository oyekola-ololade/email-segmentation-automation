# Email Segmentation & Re-engagement Automation

Tiers new leads into VIP/Standard/Budget email sequences and auto-moves cold subscribers to re-engagement.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Email service API](https://img.shields.io/badge/-Email%20service%20API-333?style=flat-square) ![Analytics endpoint](https://img.shields.io/badge/-Analytics%20endpoint-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

## Table of Contents

- [Problem](#problem)
- [Solution](#solution)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Configuration](#configuration)
- [Error Handling & Resilience](#error-handling--resilience)
- [Use Cases](#use-cases)
- [Demo](#demo)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Problem

Every lead gets the same generic email cadence regardless of how valuable they actually are.

## Solution

**Trigger:** Webhook (new CRM lead: company_size, budget, industry, email, name)

Tiers new leads into VIP/Standard/Budget email sequences and auto-moves cold subscribers to re-engagement. The workflow runs as a single n8n automation with 12 functional nodes (trigger, logic, and integration steps combined).

### Key Features

- Rule-based 3-tier segmentation
- Frequency-matched sequence enrollment
- Automatic re-engagement failover

## Architecture

```
CRM
    │
    ▼
n8n Ingestion & Routing
    │
    ▼
Business Logic Processing
    │
    ├── Firmographic Tier Segmentation
    ├── Sequence Enrollment
    ├── Engagement Tracking
    └── Re-engagement Failover
    │
    ▼
Structured Result
    │
    ▼
Delivery & Integrations
    │
    ├── Email Service
    └── Analytics
```
