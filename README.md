# Magalu Cloud

Esta skill integra o ecossistema Antigravity para orientar o gerenciamento de recursos na **Magalu Cloud** através da CLI oficial (`mgc`).

**Nota**: Esta skill **não executa** comandos diretamente no ambiente do usuário. Ela atua como um assistente especialista, sugerindo e gerando os comandos corretos da CLI `mgc` baseados na intenção do usuário.

## Overview

A skill Magalu Cloud capacita seu agente de IA a entender a arquitetura e os comandos da nuvem Magalu, facilitando operações de DevOps, provisionamento de infraestrutura e gerenciamento de armazenamento.

## Features

- **Virtual Machines**: Orientação para listar, criar, iniciar e parar instâncias.
- **Object Storage**: Comandos para gerenciamento de buckets e upload de objetos.
- **Kubernetes**: Auxílio na listagem de clusters e configuração de `kubeconfig`.
- **Autenticação**: Verificação de status e fluxo de login.

## Installation

### Opção 1: Git Clone
Clone este repositório dentro da sua pasta de skills do Antigravity:

```bash
git clone https://github.com/SRE-ARCHITECT/antigravity-magalu-cl.git magalu-cloud
```

### Opção 2: Download Manual
Baixe o conteúdo deste repositório e coloque na pasta `skills/magalu-cloud` do seu ambiente Antigravity.

## Prerequisites

Para utilizar as sugestões desta skill, você precisa ter:

1. **Magalu Cloud CLI (`mgc`)** instalada.
   - [Instalação e Visão Geral](https://docs.magalu.cloud/docs/devops-tools/cli-mgc/overview/)
2. Credenciais ativas configuradas via `mgc auth login`.

## Example Prompts

- "Como listo minhas máquinas virtuais na Magalu Cloud?"
- "Gere o comando para criar um bucket chamado 'meu-backup-2024'."
- "Preciso acessar meu cluster Kubernetes, qual o comando?"
- "Estou logado na CLI? Como verifico?"

## Repository Structure

```
magalu-cloud/
├── README.md        # Documentação principal (PT-BR)
├── README.en.md     # Documentation (English)
├── SKILL.md         # Definição técnica da skill e prompts
├── LICENSE          # Licença de uso
└── thumbnail.png    # Identidade visual da skill
```

## License

Este projeto está licenciado sob a [MIT License](LICENSE).
