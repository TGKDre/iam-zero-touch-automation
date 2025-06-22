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

![Onboarding Flow](screenshots/onboarding-flow.png)  
*Manual trigger and email action for onboarding*

![Offboarding Compose Step](screenshots/offboarding-compose.png)  
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

