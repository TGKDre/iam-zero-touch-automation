# Zero-Touch IAM Onboarding & Offboarding Automation

![Platform](https://img.shields.io/badge/platform-Microsoft%20Entra%20ID-0078D4?style=flat&logo=microsoft)
![Tool](https://img.shields.io/badge/tool-Power%20Automate-0066FF?style=flat&logo=microsoft)
![Tier](https://img.shields.io/badge/tier-free%20tier-green?style=flat)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat)

Automated user lifecycle management using Microsoft Entra ID (Azure AD) and Microsoft Power Automate. Simulates enterprise-grade onboarding and offboarding workflows with group-based RBAC, email notifications, and audit logging, all built on free-tier tooling.

---

## Features

- Manual trigger flows that simulate HR-initiated onboarding and offboarding requests
- Automated user group assignments for role-based access control (RBAC)
- Email notifications via Power Automate (with Compose action fallback for restricted tenants)
- Audit logging of offboarding events for compliance documentation
- No premium connectors required; fully functional on free Microsoft 365 tenants

---

## Tools & Technologies

- Microsoft Entra ID (Azure Active Directory)
- Microsoft Power Automate (Free Tier)
- Office 365 Outlook connector
- Microsoft Forms (optional trigger)

---

## Project Structure

```
iam-zero-touch-automation/
├── Onboard-User-Flow.json     Power Automate flow for onboarding
├── Offboard-User-Flow.json    Power Automate flow for offboarding simulation
└── README.md
```

---

## How to Use

```bash
git clone https://github.com/TGKDre/iam-zero-touch-automation.git
```

Import the flow JSON files into your Power Automate environment via the portal. Customize the manual trigger inputs to simulate new hire or offboarding requests. Run flows manually to verify email notifications and logs. Optionally connect Microsoft Forms or SharePoint for automated triggering.

---

## Screenshots

### Entra ID Environment

![Entra ID Users](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20User%20Page.JPG?raw=true)
![Entra ID Groups](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20Groups%20Page.JPG?raw=true)

*Entra ID Users and Groups pages for simulated workplace environment*

### Onboarding Flow

![Onboarding Flow 1](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Rocksteady%20Industries%20Power%20Automate%20Flow%201.JPG?raw=true)
![Onboarding Flow 2](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Send%20Welcome%20Email%20Step%201.JPG?raw=true)
![Onboarding Flow 3](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Basic%20SWE%20Flow%201.JPG?raw=true)

*Manual trigger and email action for onboarding*

### Offboarding Flow

![Offboarding Flow 1](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%201.JPG?raw=true)
![Offboarding Flow 2](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%202.JPG?raw=true)
![Offboarding Flow 3](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%203.JPG?raw=true)

*Compose action simulating offboarding email and audit logging*

---

## Notes & Limitations

- Email sending uses the Office 365 Outlook connector. If restricted, the Compose action logs the simulated send.
- Premium Azure AD triggers are intentionally avoided to keep the project free and accessible.
- Built as a portfolio demonstration of IAM lifecycle automation principles applicable to enterprise environments.

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

## Author

**Andre Uzoukwu** — IAM & Cybersecurity Engineer

- GitHub: [@TGKDre](https://github.com/TGKDre)
- LinkedIn: [linkedin.com/in/andre-uzoukwu-tgkdre](https://www.linkedin.com/in/andre-uzoukwu-tgkdre/)
- Email: andre.obiuzo@gmail.com
