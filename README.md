# Email Segmentation & Re-engagement Automation

Tiers new leads into VIP/Standard/Budget email sequences and auto-moves cold subscribers to re-engagement.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Email service API](https://img.shields.io/badge/-Email%20service%20API-333?style=flat-square) ![Analytics endpoint](https://img.shields.io/badge/-Analytics%20endpoint-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (new CRM lead: company_size, budget, industry, email, name)

Tiers new leads into VIP/Standard/Budget email sequences and auto-moves cold subscribers to re-engagement.

### Key Features

- Rule-based 3-tier segmentation
- Frequency-matched sequence enrollment
- Automatic re-engagement failover

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. New lead webhook receives CRM lead properties
2. Extract company size, budget, industry, email, and name
3. Segment into VIP / Standard / Budget tier by firmographic rules
4. Enroll the lead in the matching email sequence at the right send frequency
5. Track engagement; if opens are zero, move the lead to a re-engagement sequence

## Tech Stack

- n8n
- Email service API
- Analytics endpoint

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T30_Email_Segmentation_Automation.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T30_Email_Segmentation_Automation.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>
