# Azure Infrastructure & Serverless Labs

Suggested repo name: `azure-infra-and-serverless-labs`

## Description

This repo has my notes from two Azure labs I did for my Public Cloud course.
Everything here was built and tested on my own **Azure for Students**
subscription, not a company or production account.

The first file covers the core building blocks of Azure - resource groups,
virtual networks, blob storage, a virtual machine running IIS, and IAM
roles. The second file is about Azure Functions - writing one, deploying
it, watching it with Application Insights, pulling secrets from Key Vault
instead of hardcoding them, and using Azure Firewall to control what
traffic can go in and out.

I wrote it step by step so I can follow it again later, and so anyone else
can reproduce the same setup. All personal identifiers (usernames, resource
names) have been swapped for `placeholder` since this is public.

## Contents

- [`azure-infrastructure-fundamentals.md`](./azure-infrastructure-fundamentals.md)
  - Resource groups, virtual networks, Blob storage, a Windows Server VM
  running IIS, IAM/RBAC, and cost estimation.
- [`azure-functions-monitoring-and-security.md`](./azure-functions-monitoring-and-security.md)
  - Azure Functions (local dev + deploy), Application Insights monitoring,
  Key Vault secret management, and an Azure Firewall setup.

## Prerequisites

- An Azure subscription (Azure for Students used here)
- [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli)
- Visual Studio Code + the **Azure Functions** extension (for the functions file)
- .NET 8.0 SDK (isolated worker model)




## Cleanup
for student subscription resource usage: 

```bash
az group delete --name rg-lab-public-cloud --yes --no-wait
az group delete --name NetworkWatcherRG --yes --no-wait
```

```powershell
Remove-AzResourceGroup -Name 'placeholder-RG' -Force -AsJob
```
