# Zero-Touch IAM Onboarding & Offboarding Automation

This project demonstrates how to automate user lifecycle management using Microsoft Entra ID (Azure AD) and Microsoft Power Automate. The flows simulate onboarding and offboarding processes with email notifications and logging — all built using free-tier tools.
---

## Features

- Manual trigger flows to simulate HR onboarding and offboarding requests  
- Automated user group assignments for role-based access control (RBAC)  
- Email notifications via Power Automate (simulated using Compose action if email connectors are restricted)  
- Logging of offboarding events for audit and compliance  
- No premium connectors required; suitable for free Microsoft 365 tenants

---

## Tools & Technologies

- Microsoft Entra ID (Azure Active Directory)  
- Microsoft Power Automate (Free Tier)  
- Office 365 Outlook connector (or simulated Compose logging)  
- Microsoft Forms (optional)

---

## How to Use

1. Import the Power Automate flow JSON files into your Power Automate environment via the portal.  
2. Customize manual trigger inputs to simulate new hire or offboarding requests.  
3. Run flows manually to verify email notifications or logs.  
4. Optionally integrate with Microsoft Forms or SharePoint for automated triggering.

---

## Project Structure

- `Onboard-User-Flow.json` — Power Automate flow for onboarding process  
- `Offboard-User-Flow.json` — Power Automate flow for offboarding simulation  
- `README.md` — Project documentation

---

## Screenshots

![Entra ID Setup](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20User%20Page.JPG)
![Entra ID Setup](https://github.com/TGKDre/iam-zero-touch-automation/blob/38ab5356b558c895c4de96ece161eb94a6f1638b/EntraID%20Groups%20Page.JPG)
*Entra ID Users and Groups page for simulated workplace environment*

![Onboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Rocksteady%20Industries%20Power%20Automate%20Flow%201.JPG) 
![Onboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Send%20Welcome%20Email%20Step%201.JPG) 
![Onboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Basic%20SWE%20Flow%201.JPG)
![Onboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Basic%20SWE%20Flow%202.JPG)
![Onboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Basic%20SWE%20Flow%203.JPG)
*Manual trigger and email action for onboarding*

![Offboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/1c4cf2e67e75fac0666a6bdeb9599297e948ae75/Rocksteady%20Industries%20Power%20Automate%20Flow%201.JPG)
![Offboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%201.JPG)
![Offboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%202.JPG)
![Offboarding Flow](https://github.com/TGKDre/iam-zero-touch-automation/blob/91b2cd76947fcb1ca3d188991930d179b0aaa879/Offboard%203.JPG)
*Compose action simulating offboarding email/logging*

---

## Notes & Limitations

- Email sending uses Office 365 Outlook connector. If restricted, Compose action simulates email sends.  
- Premium Azure AD triggers are not used to keep the project free and accessible.  
- Ideal for demonstrating IAM lifecycle automation skills in resumes or portfolios.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Contact

For questions or collaboration, reach out at: andre.obiuzo@gmail.com

