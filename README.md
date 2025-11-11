<p align="center">
  <img src="screenshots/identity_basics_banner.png" 
       alt="Project 1 — Identity Basics Banner" width="100%">
</p>

# 🔐 Project 1 — Microsoft Entra ID  
## Identity Administration Basics (Users • Groups • RBAC)

![Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-IAM-blue?style=flat-square)
![RBAC](https://img.shields.io/badge/RBAC-Least_Privilege-blue?style=flat-square)
![Security](https://img.shields.io/badge/Access_Governance-Directory_Roles-blue?style=flat-square)
![Identity](https://img.shields.io/badge/Identity_Management-Users%2FGroups-blue?style=flat-square)

---

<details open>
  <summary><h2>📘 Executive Summary</h2></summary>

This project establishes **foundational Microsoft Entra ID (Azure AD) identity administration skills**, including:

✅ Creating users  
✅ Building & managing security groups  
✅ Applying Directory Roles using RBAC  
✅ Implementing least-privilege decision making  
✅ Documenting access governance with screenshots  

These tasks represent the core day-to-day responsibilities of an IAM Analyst, Identity Administrator, or Access Governance specialist.  
The lab demonstrates not only *how* to configure Entra ID, but *why* each choice aligns with enterprise IAM best practices.

</details>

---

<details open>
  <summary><h2 id="objective">🎯 Objective</h2></summary>

Build a clean, governed identity structure inside Microsoft Entra ID by:

- Creating user identities  
- Assigning them to appropriate security groups  
- Applying directory roles using **RBAC**  
- Enforcing the **principle of least privilege**  
- Documenting all IAM decisions for auditability  

This project lays the foundation for MFA enforcement (Project 2) and the full Joiner–Mover–Leaver lifecycle (Project 3).

</details>

---

<details open>
  <summary><h2 id="architecture">🏗️ Identity Architecture</h2></summary>

### ✅ **Tenant Details**
- **Tenant:** `yourtenant.onmicrosoft.com`
- **Role used for lab setup:** Global Administrator (for demonstration only)

### ✅ **Security Groups Created**
| Group Name | Purpose |
|-----------|---------|
| `GG-Support-Agents` | Users responsible for identity/helpdesk support |
| `GG-Contractors` | Temporary/contract workforce with minimal access |

### ✅ **Directory Roles Assigned**
| Role | Assigned To | Reason |
|------|-------------|--------|
| **User Administrator** | Maverick Blaze | Needs to manage identities & groups |
| **Password Administrator** | Nathan Dash | Handles password resets only |
| **None** | Contractors | Enforces proper least-privilege |

This architecture models real enterprise identity structures.

</details>

---

<details open>
  <summary><h2 id="tasks">✅ Tasks Completed</h2></summary>

### ✅ **1. Users Created**
- Maverick Blaze  
- Nathan Dash  
- Leah Vanta  
- Dawsyn Echo  
- Eddie Spark  

### ✅ **2. Security Groups Created**
- `GG-Support-Agents`  
- `GG-Contractors`

### ✅ **3. Group Memberships Assigned**
Support Agents:
- Maverick  
- Nathan  

Contractors:
- Leah  
- Dawsyn  
- Eddie  

### ✅ **4. Directory Roles Assigned**
- Maverick → **User Administrator**  
- Nathan → **Password Administrator**  
- Contractors → **No roles**  

### ✅ **5. Documented Least Privilege Decisions**
Each assignment is tied to minimal required access and includes justification.

</details>

---

<details open>
  <summary><h2 id="rbac">🛡️ RBAC & Least Privilege Matrix</h2></summary>

| User      | Group               | Role                   | Reason (Least Privilege) |
|-----------|----------------------|-------------------------|---------------------------|
| Maverick  | GG-Support-Agents    | User Administrator      | Needs to manage identities |
| Nathan    | GG-Support-Agents    | Password Administrator  | Handles password resets only |
| Leah      | GG-Contractors       | None                    | Contractor → minimal rights |
| Dawsyn    | GG-Contractors       | None                    | Contractor → minimal rights |
| Eddie     | GG-Contractors       | None                    | Contractor → minimal rights |

**Principle Enforced:**  
Provide the **minimum access necessary** to perform job duties, reducing the attack surface and protecting the directory from misuse.

</details>

---

<details>
  <summary><h2 id="governance">🔐 Access Governance & Security Justification</h2></summary>

### ✅ **Why RBAC Matters**
- Prevents privilege misuse  
- Reduces blast radius of credential compromise  
- Simplifies access audits  
- Ensures predictable, governed access patterns  

### ✅ **Why User Admin ≠ Password Admin**
Segregation of duties ensures:
- No single account controls too much  
- Identity creation is separate from credential resets  
- Better compliance alignment  

### ✅ **Why Contractors Receive No Admin Roles**
Contractors:
- Often temporary  
- Do not require privileged access  
- Represent increased risk if overscoped  

### ✅ **Least Privilege Done Correctly**
Every user, group, and role assignment ties back to:
- Job duties  
- Actual need  
- Security posture  
- IAM governance best practices  

</details>

---

<details>
  <summary><h2 id="screenshots">🖼️ Evidence & Screenshots</h2></summary>

### ✅ Users Created
![Users List](users-list.png)

### ✅ Security Groups
![Groups List](groups-list.png)

### ✅ Group Memberships
![Support Agents Members](support-agents-members.png)  
![Contractors Members](contractors-members.png)

### ✅ Directory Role Assignments
![Maverick User Administrator](mav-user-admin.png)  
![Nathan Password Administrator](nate-password-admin.png)

</details>

---

<details>
  <summary><h2 id="learned">📘 What I Learned</h2></summary>

- How to create and manage user identities in Entra ID  
- How to design and manage access with security groups  
- How Directory Roles enforce RBAC  
- How to apply least privilege in real IAM environments  
- Why access governance is essential for enterprise security  
- How identity, groups, and roles work together as a security boundary  

</details>

---

<details>
  <summary><h2 id="next-steps">📋 Next Steps</h2></summary>

✅ **Project 2 — MFA Enforcement Lab**  
Configure Authentication Method Policies + Registration Campaign  
→ Enforces secure sign-in for the Support Agents group.

✅ **Project 3 — Joiner → Mover → Leaver Lifecycle**  
Full identity lifecycle management across HR events.

🔜 **Future Projects:**  
- Conditional Access Policies  
- Passwordless Authentication  
- Privileged Identity Management (PIM)  
- Secure Admin Accounts  
- Access Reviews & Governance  

</details>

---

<details>
  <summary><h2 id="repo-structure">📂 Repo Structure</h2></summary>

```text
project-1-identity-basics/
│ README.md
└── screenshots/
    ├─ identity_basics_banner.png
    ├─ users-list.png
    ├─ groups-list.png
    ├─ support-agents-members.png
    ├─ contractors-members.png
    ├─ mav-user-admin.png
    ├─ nate-password-admin.png
