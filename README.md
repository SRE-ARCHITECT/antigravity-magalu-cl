# Antigravity Skill: Magalu Cloud

Esta é uma **Skill** personalizada para o ecossistema Google Antigravity (e compatíveis como Cursor/Windsurf), permitindo que seu agente de IA gerencie recursos diretamente na **Magalu Cloud**.

## 🚀 Funcionalidades

Com esta skill, seu agente pode:
- **Gerenciar VMs**: Listar, criar, iniciar e parar instâncias virtuais.
- **Object Storage**: Criar buckets e fazer upload de arquivos.
- **Kubernetes**: Listar clusters e configurar acesso kubeconfig.
- **Autenticação**: Verificar status e realizar login na CLI.

## 📦 Como Instalar

### Opção 1: Clonar diretamente na pasta de skills
Se você já usa o Antigravity ou dev-skills-toolkit:

```bash
cd ~/.agent/skills
git clone https://github.com/SEU_USUARIO/antigravity-magalu-cloud.git magalu-cloud
```

### Opção 2: Cópia manual
Copie a pasta `magalu-cloud` deste repositório para o diretório de skills do seu agente (geralmente `~/.agent/skills` ou `./.agent/skills` no seu projeto).

## 🛠️ Pré-requisitos

1. **Magalu Cloud CLI (`mgc`)**: Você precisa ter a ferramenta de linha de comando da Magalu instalada.
   - [Documentação Oficial da CLI](https://magalu.cloud/docs)
2. **Autenticação**: Execute `mgc auth login` no seu terminal antes de pedir tarefas ao agente.

## 💡 Exemplos de Prompts

- "Liste minhas máquinas virtuais na Magalu Cloud"
- "Crie um bucket chamado 'backup-projeto-alpha' na magalu"
- "Faça o deploy dessa aplicação usando uma nova instância small na Magalu"

## 📄 Estrutura

- `SKILL.md`: O arquivo de definição que ensina o agente (prompts e instruções).

---
*Desenvolvido com ❤️ para a comunidade brasileira de Cloud.*
