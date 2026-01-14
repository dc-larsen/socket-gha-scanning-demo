# Socket GitHub Actions Scanning Demo

Test that Socket's GitHub Actions scanning is working on your organization.

## What This Demo Does

This repository contains a workflow file that references a **known malicious GitHub Action**. Socket's GitHub App will scan the workflow and flag it as critical/malware.

## Safety

**DO NOT run the workflow.** Socket scans workflow files statically without executing them. The malicious action is only dangerous if the workflow actually runs.

The workflow is configured with `workflow_dispatch` (manual trigger only) so it will never run automatically.

## Setup Instructions

### 1. Fork this repository

Click "Fork" in the top right to create a copy in your organization.

### 2. Verify Socket's GitHub App is installed

Go to your org's GitHub settings:
`https://github.com/organizations/YOUR-ORG/settings/installations`

Confirm the Socket app is installed and has access to the forked repo.

### 3. Check Socket Dashboard

1. Go to [socket.dev/dashboard](https://socket.dev/dashboard)
2. Select your organization
3. Look for the forked repo in your repositories list
4. You should see a **Critical** alert for `per0x1de-1337/pullpilot`

## Expected Results

Socket should flag the following:
- **Known Malware** - The action `per0x1de-1337/pullpilot` is in Socket's threat feed

## Cleanup

After testing, delete the forked repository from your organization.

## Questions?

Contact your Socket account team or visit [socket.dev/support](https://socket.dev/support).
