---
name: magalu-cloud
description: Gerencia implantação e recursos na Magalu Cloud usando a CLI mgc.
---

# Magalu Cloud Skill

Esta skill permite gerenciar recursos e fazer deploy de aplicações na Magalu Cloud.

## Pré-requisitos
- CLI `mgc` instalada e configurada no PATH.
- Credenciais configuradas (via `mgc auth` ou variáveis de ambiente).

## Capacidades

1.  **Autenticação e Configuração**:
    *   Verificar status da autenticação: `mgc auth status`
    *   Login (se necessário): `mgc auth login`

2.  **Object Storage (Buckets)**:
    *   Listar buckets: `mgc object-storage buckets list`
    *   Criar bucket: `mgc object-storage buckets create [nome-do-bucket]`
    *   Upload de arquivos: `mgc object-storage objects upload [bucket] [arquivo]`

3.  **Máquinas Virtuais (Instances)**:
    *   Listar instâncias: `mgc virtual-machine instances list`
    *   Criar instância: `mgc virtual-machine instances create --name [nome] --image [imagem] --machine-type [tipo]`
    *   Parar/Iniciar instância: `mgc virtual-machine instances stop [id]`, `mgc virtual-machine instances start [id]`

4.  **Kubernetes (K8s)**:
    *   Listar clusters: `mgc kubernetes clusters list`
    *   Obter kubeconfig: `mgc kubernetes clusters kubeconfig [id]`

5.  **Deploy Automático**:
    *   Se o usuário pedir deploy simples, sugira containerizar a aplicação (Docker) e usar Kubernetes ou VM.
    *   Para sites estáticos, use Object Storage com configuração de site público.

## Exemplos de Uso
- "Liste minhas instâncias na Magalu Cloud" -> Execute `mgc virtual-machine instances list`
- "Crie um bucket chamado 'meu-backup' na Magalu" -> Execute `mgc object-storage buckets create meu-backup`
