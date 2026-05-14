# Azure Administration Foundations: Identity Management and RBAC Configuration

## Overview
This repository documents practical Azure administration work across three core areas: identity management, role‑based access control, and governance and compliance. The aim is to demonstrate real‑world Azure operational capability through structured, reproducible tasks aligned with enterprise practices.

---

# Identity Management: Provisioning Accounts and Establishing Group‑Based Access

## Objective
Create a foundational identity structure in Azure Active Directory by provisioning users and establishing group‑based access. This identity layer supports later work involving RBAC and governance controls.

## Work Completed

### Creating Azure AD Users
Two member accounts were created for access testing and role assignment scenarios:

- az104-user1  
- az104-user2  

<img width="313" height="325" alt="image" src="https://github.com/user-attachments/assets/9d8e7241-69d8-4ce6-a205-df791d01d1d8" />

Configuration applied:
- User type: Member  
- Default password set  
- No administrative roles assigned  

### Creating a Security Group
A security group was created to support group‑based access control.

Group details:
- Name: IT Lab Admins
- Type: Security  
- Membership: Assigned  

<img width="381" height="242" alt="image" src="https://github.com/user-attachments/assets/92dcf8b4-2a7c-48e5-a4f9-a67c6ea363cf" />

### Adding Users to the Group
Both users were added to the group:
- az104-user1  
- az104-user2  

### Validation
- Users appear correctly in the directory  
- Group membership confirmed  
- No RBAC roles assigned at this stage  

## Lessons Learned
- Group‑based access is more scalable than direct user assignment  
- Consistent naming supports clarity across identity, RBAC, and governance work  
- Identity provisioning forms the base layer for all access and governance controls  

# Role‑Based Access Control (RBAC)

## Objective
Organise access at scale by using management groups and applying both built‑in and custom role assignments.

## Work Completed

### Management Group Created
Created a management group named **az104-mg** to provide a higher‑level scope for organising and managing the subscription.

### Assigned Built‑In Role
Assigned the **Virtual Machine Contributor** role through Access Control (IAM) to allow management of virtual machines without granting full administrative permissions.

### Custom Role Created
Created a custom role named **Custom Support Request**, based on the Support Request Contributor role, with unnecessary permissions removed to follow least‑privilege principles.

<img width="348" height="250" alt="image" src="https://github.com/user-attachments/assets/9ba3c457-1bc2-4257-ba7c-ebf73674c186" />

### Activity Log Reviewed
Reviewed the **Activity Log** to confirm role assignment actions and verify that changes were recorded correctly.

<img width="340" height="325" alt="image" src="https://github.com/user-attachments/assets/9a7436e5-0227-4d9b-97b8-d4134adb2ba7" />

