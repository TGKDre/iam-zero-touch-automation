# Zero-Touch IAM Onboarding & Offboarding Automation

![License](https://img.shields.io/badge/license-MIT-blue?style=flat)
![Last Commit](https://img.shields.io/badge/last%20commit-2026--06-blue?style=flat)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Entra%20ID-0078D4?style=flat&logo=microsoft)
![Tool](https://img.shields.io/badge/tool-Power%20Automate-0066FF?style=flat&logo=microsoft)
![Tier](https://img.shields.io/badge/tier-free%20tier-green?style=flat)

---

## 📋 Overview

Automated user lifecycle management using Microsoft Entra ID (Azure AD) and Microsoft Power Automate. This project simulates enterprise-grade onboarding and offboarding workflows with group-based RBAC, email notifications, and audit logging — all built entirely on free-tier tooling. It demonstrates how organizations can achieve zero-touch IAM provisioning without premium licenses.

---

## 🏗️ Architecture

### Onboarding Flow

```
HR Trigger (Manual)
      │
      ▼
┌─────────────────┐
│  Create User in  │
│  Entra ID        │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Assign RBAC     │
│  Group(s)        │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Send Welcome    │
│  Email           │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Log Event to    │
│  Audit Trail     │
└─────────────────┘
```

### Offboarding Flow

```
HR Trigger (Manual)
      │
      ▼
┌─────────────────┐
│  Remove User     │
│  from Groups     │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Disable User    │
│  Account         │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Send Notification│
│  (Email or Log)  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Audit Log Entry │
│  for Compliance  │
└─────────────────┘
```

Power Automate flows orchestrate the entire lifecycle. Onboarding creates the user in Entra ID, assigns group memberships for role-based access, sends a welcome email, and logs the event. Offboarding reverses the process: removing group assignments, disabling the account, and recording the event for compliance documentation.

---

## ✨ Features

- Manual trigger flows that simulate HR-initiated onboarding and offboarding requests
- Automated user group assignments for role-based access control (RBAC)
- Email notifications via Power Automate (with Compose action fallback for restricted tenants)
- Audit logging of offboarding events for compliance documentation
- No premium connectors required; fully functional on free Microsoft 365 tenants

---

## ⚡ Quick Start

### Prerequisites

- A Microsoft 365 tenant (free or paid)
- Microsoft Power Automate access
- Microsoft Entra ID (Azure AD) available in your tenant

### Setup

```bash
git clone https://github.com/TGKDre/iam-zero-touch-automation.git
cd iam-zero-touch-automation
```

### Import and run

1. Navigate to [Power Automate](https://make.powerautomate.com)
2. Import `Onboard-User-Flow.json` as a new cloud flow
3. Import `Offboard-User-Flow.json` as a new cloud flow
4. Customize the manual trigger inputs to simulate new hire or offboarding requests
5. Run flows manually to verify email notifications and logs
6. Optionally connect Microsoft Forms or SharePoint for automated triggering

---

## 🛠️ Tech Stack

| Technology                     | Role                                |
|--------------------------------|--------------------------------------|
| Microsoft Entra ID (Azure AD)  | Identity store and user provisioning |
| Microsoft Power Automate       | Workflow orchestration               |
| Office 365 Outlook connector   | Email notifications                  |
| Microsoft Forms (optional)     | Automated trigger source             |

---

## 📸 Screenshots

### Entra ID Environment

![Entra ID Users](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20User%20Page.JPG?raw=true)
![Entra ID Groups](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20Groups%20Page.JPG?raw=true)

*Entra ID Users and Groups pages for simulated workplace environment*

### Onboarding Flow

![Onboarding Flow 1](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Rocksteady%20Industries%20Power%20Automate%20Flow%201.JPG?raw=true)
![Onboarding Flow 2](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Send%20Welcome%20Email%20Step%201.JPG?raw=true)
![Onboarding Flow 3](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Basic%20SWE%20Flow%201.JPG?raw=true)

*Manual trigger and email action for onboarding; user created, groups assigned, welcome email sent*

### Offboarding Flow

![Offboarding Flow 1](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%201.JPG?raw=true)
![Offboarding Flow 2](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%202.JPG?raw=true)
![Offboarding Flow 3](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%203.JPG?raw=true)

*Compose action simulating offboarding email and audit logging for compliance*

---

## 📁 Repository Structure

```
iam-zero-touch-automation/
├── Onboard-User-Flow.json      Power Automate flow for onboarding
├── Offboard-User-Flow.json     Power Automate flow for offboarding simulation
├── EntraID User Page.JPG       Screenshot: Entra ID users
├── EntraID Groups Page.JPG     Screenshot: Entra ID groups
├── Basic SWE Flow 1-3.JPG      Screenshots: onboarding flow steps
├── Rocksteady Industries...JPG Screenshot: flow trigger
├── Send Welcome Email Step 1.JPG Screenshot: email action
├── Offboard 1-3.JPG            Screenshots: offboarding flow steps
└── README.md
```

---

## 📝 Notes & Limitations

- Email sending uses the Office 365 Outlook connector. If restricted, the Compose action logs the simulated send.
- Premium Azure AD triggers are intentionally avoided to keep the project free and accessible.
- Built as a portfolio demonstration of IAM lifecycle automation principles applicable to enterprise environments.

---

## 🔗 Related Projects

- [iam-homelab](https://github.com/TGKDre/iam-homelab) — Self-hosted IAM & SSO lab on OCI with Authentik and Gitea
- [iam-portfolio](https://github.com/TGKDre/iam-portfolio) — Production-grade IAM infrastructure with Traefik reverse proxy and ForwardAuth middleware

---

Built by [Andre Uzoukwu](https://github.com/TGKDre) — [LinkedIn](https://linkedin.com/in/andre-uzoukwu-tgkdre)
