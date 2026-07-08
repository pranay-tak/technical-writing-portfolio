# TG-001: Troubleshooting Microsoft 365 Backup Failures

---

## Document Information

| Field | Value |
|-------|-------|
| Document ID | TG-001 |
| Product | Microsoft 365 Backup |
| Category | Troubleshooting Guide |
| Audience | Microsoft 365 Administrators, Support Engineers |
| Author | Pranay Tak |
| Version | 1.0 |
| Last Updated | July 2026 |

---

## Overview

This guide provides troubleshooting steps for common Microsoft 365 backup failures involving Exchange Online, SharePoint Online, OneDrive, and Microsoft Teams workloads.

---

## Common Backup Failures

### 1. Authentication Failure

#### Symptoms

- Backup jobs fail immediately.
- OAuth errors appear in logs.
- Connection status displays unhealthy.

#### Possible Causes

- Expired client secret.
- Revoked permissions.
- Missing administrator consent.

#### Resolution

- Verify client secret validity.
- Reauthorize the application.
- Confirm Graph API permissions.

---

### 2. Mailbox Discovery Failure

#### Symptoms

- Exchange mailboxes are missing.
- Users are not discovered.

#### Possible Causes

- License not assigned.
- Mailbox not provisioned.
- Permission issue.

#### Resolution

- Verify Exchange Online license assignment.
- Confirm mailbox exists.
- Validate discovery permissions.

---

### 3. SharePoint Backup Failure

#### Symptoms

- Site collections fail backup.
- Backup jobs remain in progress indefinitely.

#### Possible Causes

- Site access issue.
- Permission changes.
- Microsoft service issue.

#### Resolution

- Verify site accessibility.
- Confirm application permissions.
- Check Microsoft service health.

---

### 4. OneDrive Backup Failure

#### Symptoms

- User OneDrive data is skipped.
- Backup completes with warnings.

#### Possible Causes

- User never accessed OneDrive.
- Provisioning incomplete.

#### Resolution

- Confirm OneDrive provisioning.
- Ask the user to access OneDrive once.
- Run discovery again.

---

## Log Collection

Collect the following information before escalating:

- Job ID
- Tenant ID
- Timestamp
- Error message
- Affected workload
- Screenshot of failure

---

## Escalation Checklist

Before escalation, verify:

- Authentication status
- Permissions
- Service health
- Application registration
- Network connectivity

---

## Best Practices

- Monitor failed jobs daily.
- Review alerts regularly.
- Perform periodic restore testing.
- Maintain documentation for configuration changes.

---

## Related Articles

- KB-001 OAuth Authentication Failure
- IG-001 Installation Guide
- UG-001 Getting Started Guide

---

## Version History

| Version | Date | Description |
|----------|------|-------------|
| 1.0 | July 2026 | Initial release |

---