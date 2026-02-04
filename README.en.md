# Magalu Cloud

This skill integrates with the Antigravity ecosystem to guide resource management on **Magalu Cloud** using the official CLI (`mgc`).

**Note**: This skill **does not execute** commands directly in the user's environment. It acts as an expert assistant, suggesting and generating the correct `mgc` CLI commands based on user intent.

## Overview

The Magalu Cloud skill empowers your AI agent to understand Magalu's cloud architecture and commands, facilitating DevOps operations, infrastructure provisioning, and storage management.

## Features

- **Virtual Machines**: Guidance for listing, creating, starting, and stopping instances.
- **Object Storage**: Commands for bucket management and object uploads.
- **Kubernetes**: Assistance with listing clusters and configuring `kubeconfig`.
- **Authentication**: Status verification and login flow.

## Installation

### Option 1: Git Clone
Clone this repository into your Antigravity skills folder:

```bash
git clone https://github.com/SRE-ARCHITECT/antigravity-magalu-cl.git magalu-cloud
```

### Option 2: Manual Download
Download the contents of this repository and place them in the `skills/magalu-cloud` folder of your Antigravity environment.

## Prerequisites

To use the suggestions provided by this skill, you need:

1. **Magalu Cloud CLI (`mgc`)** installed.
   - [Installation and Overview](https://docs.magalu.cloud/docs/devops-tools/cli-mgc/overview/)
2. Active credentials configured via `mgc auth login`.

## Example Prompts

- "How do I list my virtual machines on Magalu Cloud?"
- "Generate the command to create a bucket named 'my-backup-2024'."
- "I need to access my Kubernetes cluster, what is the command?"
- "Am I logged into the CLI? How do I check?"

## Repository Structure

```
magalu-cloud/
├── README.md        # Main Documentation (PT-BR)
├── README.en.md     # Documentation (English)
├── SKILL.md         # Technical skill definition and prompts
├── LICENSE          # Usage License
└── thumbnail.png    # Skill visual identity
```

## License

This project is licensed under the [MIT License](LICENSE).
