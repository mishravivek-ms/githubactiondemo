# GitHub Actions Demo Repository

This repository demonstrates the basic functionality of GitHub Actions through a simple Continuous Integration (CI) workflow.

## Repository Structure

```
├── .github/
│   └── workflows/
│       └── blank.yml          # GitHub Actions CI workflow
└── README.md                  # This documentation file
```

## What This Repository Demonstrates

This is a minimal GitHub Actions demo that showcases:

1. **Basic CI Workflow Setup**: Demonstrates how to create a GitHub Actions workflow
2. **Trigger Events**: Shows different ways to trigger workflows (push, pull request, manual)
3. **Secret Usage**: Illustrates how to use GitHub repository secrets in workflows
4. **Multi-step Jobs**: Example of running multiple commands in a workflow

## GitHub Actions Workflow Details

The repository contains a single workflow file (`.github/workflows/blank.yml`) that:

### Triggers
- **Push events**: Runs when code is pushed to the `main` branch
- **Pull request events**: Runs when pull requests are opened/updated targeting the `main` branch  
- **Manual dispatch**: Can be triggered manually from the GitHub Actions tab

### Job Configuration
- **Runner**: Uses `ubuntu-latest` 
- **Steps**:
  1. **Checkout**: Uses `actions/checkout@v4` to access repository code
  2. **Secret Demo**: Demonstrates accessing repository secrets (`MY_SECRET`)
  3. **Multi-line Script**: Shows how to run multiple shell commands

### Example Workflow Output
When the workflow runs, it will:
- Check out the repository code
- Print the value of the `MY_SECRET` repository secret
- Display sample build/test/deploy messages

## How to Use This Demo

1. **Fork this repository** to your GitHub account
2. **Set up a repository secret**:
   - Go to your forked repo → Settings → Secrets and variables → Actions
   - Create a new repository secret named `MY_SECRET` with any value
3. **Trigger the workflow** by:
   - Pushing changes to the `main` branch
   - Creating a pull request to `main`
   - Manually running it from the Actions tab

## Learning Objectives

This demo helps you understand:
- GitHub Actions workflow syntax and structure
- How to configure workflow triggers
- Working with repository secrets
- Basic CI/CD concepts with GitHub Actions
- Running shell commands in workflow jobs

## Next Steps

To extend this demo, you could:
- Add actual build/test steps for a real project
- Include multiple jobs running in parallel
- Add deployment steps
- Use marketplace actions for specific technologies
- Set up matrix builds for multiple environments
