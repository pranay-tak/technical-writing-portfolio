# UG-001: Getting Started with Microsoft 365 Backup

---

## Document Information

| Field | Value |
|-------|-------|
| Document ID | UG-001 |
| Product | Microsoft 365 Backup |
| Category | User Guide |
| Audience | Microsoft 365 Administrators |
| Author | Pranay Tak |
| Version | 1.0 |
| Last Updated | July 2026 |

---

## Overview

This guide helps administrators perform the initial configuration of Microsoft 365 Backup and create their first backup job.

---

## Supported Workloads

Microsoft 365 Backup supports the following workloads:

- Exchange Online
- SharePoint Online
- OneDrive for Business
- Microsoft Teams

---

## Before You Begin

Ensure the following prerequisites are met:

- Microsoft 365 tenant is active.
- Administrator permissions are available.
- OAuth authorization is configured.
- Backup application is successfully connected.

---

## Accessing the Backup Console

1. Sign in to the backup administration portal.
2. Navigate to:

```text
Workloads → Microsoft 365
```

3. Verify that all workloads display a healthy connection status.

---

## Creating Your First Backup Job

### Step 1: Select Workload

Choose the workload to protect:

- Exchange Online
- SharePoint Online
- OneDrive
- Teams

---

### Step 2: Select Objects

Select the objects to include:

- Users
- Mailboxes
- Sites
- Teams

---

### Step 3: Configure Schedule

Select a backup schedule:

- Daily
- Weekly
- Monthly

Configure:

- Backup time
- Retention period
- Notification preferences

---

### Step 4: Review and Save

Review the configuration and click:

```text
Save
```

The backup job will now appear in the Jobs dashboard.

---

## Monitoring Backup Jobs

Navigate to:

```text
Jobs → Active Jobs
```

Monitor:

- Success rate
- Duration
- Data protected
- Errors and warnings

---

## Running a Test Restore

It is recommended to perform a test restore after initial deployment.

Verify:

- Mailbox restoration
- File restoration
- SharePoint item restoration

---

## Best Practices

- Schedule backups outside business hours.
- Configure notifications for failed jobs.
- Perform quarterly restore tests.
- Review backup coverage periodically.

---

## Related Articles

- KB-001 OAuth Authentication Failure
- IG-001 Installing Microsoft 365 Backup
- TG-001 Troubleshooting Backup Failures

---

## Version History

| Version | Date | Description |
|----------|------|-------------|
| 1.0 | July 2026 | Initial release |

---