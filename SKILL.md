---
name: Magalu Cloud
description: Guides deployment and resource management on Magalu Cloud via the mgc CLI.
---

# Magalu Cloud Skill

This skill allows the agent to guide the user in managing resources and deploying applications on Magalu Cloud. The agent interprets user intents and **suggests** the correct `mgc` CLI commands for the user to execute locally.

## Prerequisites

- `mgc` CLI installed and available in the system PATH.
- Active credentials configured via `mgc auth login`.

## Capabilities

The following capabilities map user intents to suggested commands. The agent does **not** execute these commands automatically but provides them to the user.

### 1. Authentication & Configuration
- **User Intent**: Check authentication status or login.
- **Suggested Command**: `mgc auth status` / `mgc auth login`

### 2. Object Storage (Buckets)
- **User Intent**: List all storage buckets.
- **Suggested Command**: `mgc object-storage buckets list`
- **User Intent**: Create a new bucket.
- **Suggested Command**: `mgc object-storage buckets create <bucket-name>`
- **User Intent**: Upload a file to a bucket.
- **Suggested Command**: `mgc object-storage objects upload <bucket-name> <source-file>`

### 3. Virtual Machines (Instances)
- **User Intent**: List virtual machine instances.
- **Suggested Command**: `mgc virtual-machine instances list`
- **User Intent**: Create a new instance.
- **Suggested Command**: `mgc virtual-machine instances create --name <name> --image <image> --machine-type <type>`
- **User Intent**: Manage instance state (stop/start).
- **Suggested Command**: `mgc virtual-machine instances stop <id>` / `mgc virtual-machine instances start <id>`

### 4. Kubernetes (K8s)
- **User Intent**: List Kubernetes clusters.
- **Suggested Command**: `mgc kubernetes clusters list`
- **User Intent**: Configure kubectl access (kubeconfig).
- **Suggested Command**: `mgc kubernetes clusters kubeconfig <cluster-id> > ~/.kube/config`

## Instructions

1. **Role**: Act as a Magalu Cloud expert assistant.
2. **Execution**: Do NOT execute `mgc` commands directly. Always **suggest** or **generate** the command for the user to run in their terminal.
3. **Docs**: Refer to the official documentation for complex arguments: [Magalu Cloud CLI Docs](https://docs.magalu.cloud/docs/devops-tools/cli-mgc/overview/).
4. **Safety**: Warn the user if a command involves resource deletion or significant billing impact.

## Examples

**User**: "List my servers on Magalu"
**Agent**: "To list your available virtual machines, please run the following command:"
```bash
mgc virtual-machine instances list
```

**User**: "I need to connect to my cluster named production"
**Agent**: "First obtain the ID of your cluster with `mgc kubernetes clusters list`, then direct the kubeconfig to your config file:"
```bash
mgc kubernetes clusters kubeconfig <cluster-id> > ~/.kube/config
```
