# File-Share-Access-Management

File Share Access Management &amp; NTFS Permissions

## Overview
This project demonstrates enterprise file share management by resolving user access issues through proper NTFS permissions configuration. It covers security principles, access control, and permission inheritance in Windows Server environments.

## Environment & Technologies
- Windows Server 2022
- Active Directory Domain Services
- NTFS Permissions
- Network File Sharing
- Jira Service Management
- Oracle VirtualBox

## Step-by-Step Implementation

### 1. Access Request
- User submitted ticket requesting access to company shared folder
- Ticket described inability to access `\\HOMELAB01\Shared\IT_SHARE`

### 2. Initial Verification
- Confirmed "Access Denied" error message on user's machine
- Verified the shared folder existed and was accessible to other users

### 3. Account Validation
- Checked Active Directory to ensure user account was active and not locked
- Verified user was in correct organizational units and groups

### 4. Permissions Investigation
- Navigated to shared folder properties on file server
- Examined Security tab and NTFS permissions
- Identified user was missing from access control list

### 5. Permission Assignment
- Added user to folder security permissions
- Assigned appropriate access level (Read & Execute)
- Applied changes and propagated permissions

### 6. Access Verification
- Requested user to test shared folder access
- Confirmed user could now browse and open files
- Verified appropriate access level functionality

### 7. Documentation
- Updated service ticket with permission changes
- Documented security group membership requirements
- Closed incident with successful resolution

## Challenges & Solutions
- **Challenge**: User unable to access job-critical resources
- **Solution**: Systematic permission audit and appropriate access assignment
- **Challenge**: Maintaining security while providing necessary access
- **Solution**: Principle of least privilege implementation

## Key Learnings
- NTFS vs Share permissions differences
- Active Directory security group management
- Permission inheritance and propagation
- Access control list (ACL) management
- Security auditing and compliance

## Screenshots
![Access Request](/screenshots/1.png)
![Access Denied Error](/screenshots/2.png)
![AD Verification](/screenshots/3.png)
![NTFS Permissions](/screenshots/4.png)
![Permission Assignment](/screenshots/5.png)
![Access Restored](/screenshots/6.png)
![Access Restored](/screenshots/7.png)
