# IG-001: Installing Microsoft 365 Backup for Exchange Online

---

## Document Information

| Field | Value |
|-------|-------|
| Document ID | IG-001 |
| Product | Microsoft 365 Backup |
| Category | Installation Guide |
| Audience | Microsoft 365 Administrators |
| Author | Pranay Tak |
| Version | 1.0 |
| Last Updated | July 2026 |

---

## Overview

This installation guide describes the process of configuring Microsoft 365 Backup for Exchange Online workloads. It includes prerequisites, permissions, installation steps, and post-installation verification.

---

## Intended Audience

This guide is intended for:

- Microsoft 365 Administrators
- Backup Administrators
- Technical Support Engineers
- Cloud Operations Teams

---

## Prerequisites

Before beginning the installation, ensure that the following requirements are met:

### Microsoft 365 Requirements

- Active Microsoft 365 tenant
- Exchange Online enabled
- Global Administrator access
- Microsoft Entra ID access

### Permissions Required

The installation account must have:

- Global Administrator role
- Application Administrator role (optional but recommended)

### Network Requirements

Allow outbound connectivity to:

- Microsoft Graph API
- Microsoft Entra ID endpoints
- Exchange Online services

---

## Architecture Overview

The backup application communicates with Microsoft 365 services using Microsoft Graph APIs and OAuth authentication.

The following workloads are supported:

- Exchange Online
- SharePoint Online
- OneDrive for Business
- Microsoft Teams

---

## Installation Procedure

### Step 1: Create Application Registration

1. Open the Microsoft Entra Admin Center.
2. Navigate to:

   ```text
   Applications → App Registrations
   ```

3. Select **New Registration**.
4. Enter an application name.
5. Select the supported account type.
6. Click **Register**.

---

### Step 2: Configure API Permissions

Assign the required Microsoft Graph permissions.

Recommended permissions include:

- Mail.Read
- Sites.Read.All
- Files.Read.All
- User.Read
- Directory.Read.All

Grant administrator consent after assigning permissions.

---

### Step 3: Generate Client Secret

1. Open the application registration.
2. Navigate to:

   ```text
   Certificates & Secrets
   ```

3. Create a new client secret.
4. Store the generated value securely.

> **Important:** The client secret value cannot be retrieved after leaving the page.

---

### Step 4: Configure Backup Application

Provide the following details:

- Tenant ID
- Application ID
- Client Secret

Save the configuration.

---

### Step 5: Authorize the Connection

Authenticate using a Global Administrator account.

Grant consent for the requested permissions.

---

## Post Installation Verification

Verify the following:

- Connection status shows **Healthy**
- Exchange Online mailboxes are discovered
- Backup policies can be created
- Test backup job completes successfully

---

## Troubleshooting

### Authentication Failure

Verify:

- Tenant ID
- Application ID
- Client Secret
- Administrator Consent

---

### Mailbox Discovery Failure

Verify:

- Exchange Online license assignment
- Microsoft Graph permissions
- Service health status

---

## Best Practices

- Use dedicated service accounts.
- Rotate secrets regularly.
- Review permissions quarterly.
- Enable monitoring and alerts.
- Perform periodic test restores.

---

## Related Articles

- KB-001 OAuth Authentication Failure
- Restore Exchange Online Mailboxes
- Configure Backup Policies

---

## Version History

| Version | Date | Description |
|----------|------|-------------|
| 1.0 | July 2026 | Initial release |

---