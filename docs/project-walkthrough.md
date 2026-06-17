Azure VM Backup & Disaster Recovery Project Walkthrough
Project Objective

The goal of this project was to implement a backup and disaster recovery solution for an Azure Virtual Machine to protect business data from accidental deletion, corruption, or system failure.
Environment Setup
Resource Group-rg-vmbackup-project
This resource group contains all resources related to the backup solution.
Virtual Machine-VM01
A Windows Azure Virtual Machine used as the workload that needs protection.
Recovery Services Vault-RSV01
Used to manage Azure Backup operations, backup policies, retention settings, and recovery points.
Storage Account-rsvstorage001

Used for backup-related storage and recovery operations.

Step 1: Create Virtual Machine
Created Azure VM VM01 inside rg-vmbackup-project.
Purpose:
Simulate a production server
Store files that require protection

Step 2: Create Recovery Services Vault
Created RSV01 in the same resource group.
Purpose:
Centralized backup management
Store recovery points
Manage retention policies

Step 3: Configure Backup
Enabled backup for VM01.
Configured:
Backup schedule
Retention policy
Daily recovery point creation
Purpose:
Automatically protect VM data
Reduce risk of data loss

Step 4: Run On-Demand Backup
Triggered a manual backup job.
Result:
Recovery point successfully created
Backup status verified
Purpose:
Validate backup configuration
Ensure restore readiness

Step 5: Test File Recovery
Deleted or simulated loss of a file.
Used Azure Backup File Recovery option to:
Mount recovery point
Browse backup data
Recover selected file

Result:
File restored successfully
Business Benefit:
No need to restore entire VM
Faster recovery
Reduced downtime

Step 6: Test Full VM Restore
Selected recovery point from Recovery Services Vault.
Performed:
Restore Virtual Machine
Azure created a restored VM from backup.
Result:
VM restored successfully
Data and configuration recovered

Business Benefit:
Complete disaster recovery
Rapid service restoration
