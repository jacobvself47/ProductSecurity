## Overview
- Secrets are what users use to authenticate to other computers.
- Examples of secrets include: passwords, API secrets, certificates, hash, and connection strings

### Finding Secrets
- Secret scanner tools most often use RegEx to look for Entropy
  - Entropy - long and random bunches of characters
- Secret scanners also search for keywords: "password","secret","key"
- After finding secrets - immediate next step is to rotate that secret

### Preventing Secrets in the Code
- Best method to prevent secrets is to use 'pre-commit hook'
- Pre-commit hooks allow you to run secret scans on only the new or change code you are checking in  
  - Stops the code from being checked in - thus it is never logged or backed up
  - Pre-commit hooks prevent the secret from having to be rotated.

### Secret Management
- Manage secrets for machines - not the same as password manager
- Only machines can retrieve the secret
