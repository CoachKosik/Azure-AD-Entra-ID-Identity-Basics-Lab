# Azure AD / Entra ID — Identity Basics Lab

**Objective:** Demonstrate identity creation, grouping, and role-based access control (RBAC) within Microsoft Entra ID (Azure AD). This lab establishes core IAM fundamentals used in enterprise identity management and access governance.

## Tenant
- Tenant: `[yourtenant.onmicrosoft.com]`
- Admin role used: **Global Administrator**

## Tasks Completed
1. Created five users:
   - Maverick Blaze  
   - Nathan Dash  
   - Leah Vanta  
   - Dawsyn Echo  
   - Eddie Spark  
2. Created two security groups:
   - `GG-Support-Agents`  
   - `GG-Contractors`  
3. Added members to each group based on access needs.
4. Assigned roles:
   - Maverick → **User Administrator**
   - Nathan → **Password Administrator**
   - Contractors → **No roles** (least privilege)
5. Documented least-privilege decisions.

## RBAC & Least Privilege Table

| User      | Group               | Role                   | Reason (Least Privilege) |
|-----------|----------------------|-------------------------|---------------------------|
| Maverick  | GG-Support-Agents    | User Administrator      | Needs to manage identities |
| Nathan    | GG-Support-Agents    | Password Administrator  | Only handles password resets |
| Leah      | GG-Contractors       | None                    | Contractor, minimal access |
| Dawsyn    | GG-Contractors       | None                    | Contractor, minimal access |
| Eddie     | GG-Contractors       | None                    | Contractor, minimal access |

## Screenshots

   ### Users
      ![Users List](screenshots/users-list.png)

   ### Groups
      ![Groups List](screenshots/groups-list.png)

   ### Group Memberships
      ![Support Agents Members](screenshots/support-agents-members.png)
      ![Contractors Members](screenshots/contractors-members.png)

   ### Role Assignments
      ![Maverick User Administrator](screenshots/mav-user-admin.png)
      ![Nathan Password Administrator](screenshots/nate-password-admin.png)


## What I Learned
- How to create and manage identities in Microsoft Entra ID  
- How to create and manage security groups  
- The relationship between identities, groups, and directory roles  
- How RBAC enforces least privilege and reduces security risk  
- Why separating identity admins and password admins limits blast radius  

## Next Steps
- Implement MFA requirements and test sign-in scenarios (Project 2)  
- Build Joiner–Mover–Leaver lifecycle (Project 3)  
- Configure Conditional Access (future project)  
