# hackernews-workflow

> Built with [VM0](https://github.com/vm0-ai/vm0)

## Setup Instructions

### 1. Initialize VM0 Agent

```bash
vm0 init
```

This will prompt you to enter an agent name and create the necessary files:
- `vm0.yaml` - Agent configuration
- `AGENTS.md` - Agent documentation

### 2. Setup GitHub Actions

Configure GitHub Actions workflows for automated publishing and running:

```bash
vm0 setup-github
```

This command will:
- Check prerequisites (GitHub CLI, authentication, vm0.yaml)
- Analyze vm0.yaml to detect required secrets and variables
- Create workflow files:
  - `.github/workflows/publish.yml`
  - `.github/workflows/run.yml`
- Automatically set up GitHub secrets and variables

### 3. Deploy

Commit and push the workflow files:
```bash
git add .
git commit -m "init: vm0 workflow"
git push origin main
```

Push to the main branch to trigger the publish workflow.
