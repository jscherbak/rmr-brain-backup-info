---
layout: default
permalink: /privacy/
---

# rmr-brain Backup — privacy policy

Last updated: 6 November 2026.

## Purpose and data

This application stores encrypted recovery copies of a single GitHub repository in Google Drive. It processes the backup file, its file ID, name, size, parent folder and checksum to upload and verify recovery copies.

## Google Drive access

The application requests drive.file access. This permission covers files created or explicitly selected for this application. Backup copies are uploaded to the folder configured for this project and downloaded to verify their checksums.

## Processing and storage

Backup generation and verification run in GitHub Actions. Backup contents are encrypted with AES-256-GCM before upload to Google Drive. The OAuth refresh credential is stored in this repository’s GitHub Actions secrets, with a recovery copy in the project’s 1Password vault. The encryption key is stored separately in project-scoped secret entries. Technical run logs may contain file IDs, counts, checksums and status messages.

## Providers and use

GitHub, Google Drive and 1Password provide the execution, storage and credential services described above. The operator uses the data for backup and recovery. Google user data is not used for advertising or to train generalized AI models.

## Retention and controls

Backup files remain in Google Drive until the owner deletes them. This workflow currently has no automatic backup retention deletion. Run logs follow the GitHub repository’s retention settings. The owner can revoke this application’s access in Google Account permissions and remove its credentials from GitHub and 1Password.

## Contact

The operator can be contacted at jscherbak@gmail.com.
