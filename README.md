# gpg-test

## GPG Signed Commits from GitHub Actions

This repository demonstrates how to create GPG-signed commits from GitHub Actions.

### Features

- Workflow that can be triggered manually
- Automatically generates a GPG key for GitHub Actions
- Creates a random file with timestamp
- Signs the commit with the generated GPG key
- Uploads the public GPG key as an artifact

### How to Use

1. Go to the "Actions" tab in this repository
2. Select the "GPG Signed Commit" workflow
3. Click "Run workflow" button
4. Wait for the workflow to complete
5. Check the repository commits to see the GPG-signed commit (look for the "Verified" badge)
6. You can download the public GPG key from the workflow artifacts if needed

### Technical Details

The workflow performs the following steps:
- Sets up Git identity for GitHub Actions bot
- Generates a new 4096-bit RSA GPG key
- Configures Git to use the generated key for signing
- Creates a random file with timestamp
- Commits and pushes the file with GPG signature