# Joule Development - Setup & Onboarding Guide


# Official Documentation

## Joule Onboarding

https://help.sap.com/docs/joule/integrating-joule-with-sap/onboarding-joule

## Joule Development Tools

https://help.sap.com/docs/joule/joule-development-guide-ba88d1ec6a1b442098863d577c19b0c0/pro-code-development-tools-for-joule

---

# 1. High-Level Development Flow

```text
Admin Setup
    ↓
Developer Access & Roles
    ↓
Environment Setup
    ↓
Choose Development Approach
    ├── Joule Studio CLI Tool
    └── Joule Studio Code Editor
```

---

# 2. Admin / Tenant Prerequisites

> Usually handled by administrator/platform team.

---

## Required Setup

- Joule service subscription instance created
- SAP product supporting Joule integration available
- Identity Authentication integrated
- SAP BTP global account available
- Same SAP Cloud Identity Services tenant used
- Required entitlements configured

---

## Important Services

- SAP BTP
- Cloud Identity Services
- Identity Authentication
- Identity Provisioning
- SAP Build Work Zone

---

## Preview Tenant Requirement

For Joule Preview tenant:

```text
EU10 or EU30 subaccounts required
```

---

# Required Roles

| Role | Purpose |
|---|---|
| `capability_developer` | Build/compile runtime artifacts |
| `capability_release_admin` | Deploy/configure runtime artifacts |
| `end_user` | Access Joule web client |

---

# Reference Screenshot

![Onboarding Prerequisites](images/joule-onboarding-prerequisites.png)

---

# 3. Developer Setup

## Required Developer Roles

Developer should be assigned:

### extensibility_developer

Can:
- access Joule standalone Web Client
- compile capabilities
- deploy capabilities

---

### end_user

Can:
- create conversations with Joule

---

## Environment Requirements

- Cloud Foundry subaccount
- Joule service subscription + instance

---

# 4. Development Approaches

There are two main ways to develop/manage Joule assistants.

---

# Option 1 — Joule Studio CLI Tool

## What It Is

CLI tool used directly from terminal.

Supports:
- local development
- compilation
- deployment
- CI/CD integration
- secure authentication

---

## Best For

- advanced developers
- automation
- CI/CD pipelines
- Git-based workflows

---

## Prerequisites

### Node.js Installed

Verify:

```bash
node -v
npm -v
```

---

# Install Joule CLI

## Install Latest Version

```bash
npm install -g @sap/joule-studio-cli
```

---

## Install Specific Version

```bash
npm install -g @sap/joule-studio-cli@<version>
```

---

## Verify Installation

```bash
joule -V
```

---

## Common Workflow

```bash
joule login
joule compile
joule lint
joule deploy
```

---

# Why CLI Is Powerful

- lightweight
- terminal-driven
- easy automation
- integrates with Git workflows
- suitable for enterprise pipelines

---

# Option 2 — Joule Studio Code Editor

## What It Is

VS Code extension/tooling for Joule development.

Provides:
- templates
- validation
- quick fixes
- schema updates
- linting
- deployment
- assistant management

---

## Best For

- visual development
- beginners
- guided development
- faster onboarding

---

## Features

- Generate from template
- Validate content
- Quick Fix
- Schema Update
- Lint content
- Create connections
- Compile capabilities
- Deploy assistants
- Launch assistants
- Delete assistants

---

## Prerequisites

### Node.js Installed

```bash
node -v
npm -v
```

---

# Which Approach Should I Use?

| Scenario | Recommended |
|---|---|
| Quick onboarding | Code Editor |
| Visual development | Code Editor |
| CI/CD automation | CLI |
| Git-heavy workflow | CLI |
| Enterprise deployments | CLI |
| Learning Joule basics | Code Editor first |

---

# Suggested Initial Setup Workflow

## Step 1

Install Node.js

---

## Step 2

Install Joule CLI

```bash
npm install -g @sap/joule-studio-cli
```

---

## Step 3

Login

```bash
joule login
```

---

## Step 4

Validate Environment

```bash
joule status
```

---

# Reference Screenshot

![Development Setup](images/joule-development-setup.png)

---

# My Notes

## Key Understanding

- Joule development is capability-driven.
- CLI approach is more enterprise/devops oriented.
- Code Editor approach is more onboarding-friendly.
- Identity setup is critical.
- BTP + Cloud Foundry knowledge becomes important quickly.
