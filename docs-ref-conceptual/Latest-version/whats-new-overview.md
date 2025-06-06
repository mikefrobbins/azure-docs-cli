---
title: Azure CLI release highlights | Microsoft Docs
description: Learn what's new in the Azure CLI. Read about new features and upcoming changes. Check here for announcements.
ms.service: azure-cli
ms.custom: devx-track-azurecli
keywords: Azure CLI, new articles, new references, new samples, announcements
#customer intent: As an Azure CLI developer, I want an easy way to see product change highlights and upcoming breaking change announcements.
---

# Azure CLI release highlights

This page highlights new features and upcoming changes for Azure CLI.

## Important notice for Azure Stack Hub customers

> [!IMPORTANT]
> If you're using **Azure Stack Hub**, do not upgrade Azure CLI beyond version 2.66.x.

Starting with **Azure CLI 2.73.0**, Azure profiles are deprecated and no longer supported:

- `2017-03-09-profile`
- `2018-03-01-hybrid`
- `2019-03-01-hybrid`
- `2020-09-01-hybrid`

These profiles are required for Azure Stack Hub compatibility. Newer versions of Azure CLI do
**not** include them. To ensure compatibility with Azure Stack Hub, use **Azure CLI version 2.66.x
(LTS)**.

If you upgrade to a newer version of Azure CLI, you must roll back to version **2.66.x** to restore
Azure Stack Hub compatibility.

## Multifactor authentication (MFA)

[!INCLUDE [MFA](includes/multifactor-authentication.md)]

## Ignite 2024

There are several new Azure CLI features being released for Ignite 2024.

- Improved credential protection
- New end-to-end scenarios in Azure Copilot
- Support for Azure CLI on Azure Linux 3.0
- Refined Azure CLI extension management

For details on the new features, see
[Azure CLI and Azure PowerShell Ignite 2024 Announcement][19].

## AI Shell

AI Shell introduces a seamless way to obtain assistance from Copilot in Azure directly within your
command-line interface (CLI). Generate Azure CLI commands using natural language right in your
preferred terminal environment. For more information, see
[Use Microsoft Copilot in Azure with AI Shell][10].

## Docker container image

Beginning with Azure CLI version 2.67.0, to be released on November 19, 2024, the default Docker
container image for Azure CLI is based on Azure Linux. To avoid any disruptions, review and update
any dependencies you might have on the default Docker container image for Azure CLI.

For more information, see [How to run Azure CLI in a Docker container][08].

## Select your subscription at time of login

We listened to your feedback and improved Azure CLI interactive login experience to include a
subscription selector. To use the new feature, see [Sign in interactively with Azure CLI ][01].

## Protect sensitive information

Beginning in [Azure CLI 2.57][07], a warning message can be displayed when reference commands result
in the output of sensitive information. For more information, see
[Manage Azure secrets using Azure CLI][02].

## Azure Copilot for Azure CLI

[Microsoft Copilot for Azure][17] (preview) is published. Copilot is an AI-powered tool that helps
you do more with Azure. It unifies knowledge and data across hundreds of Azure services to increase
productivity, reduce costs, and provide deep insights. Microsoft Copilot for Azure (preview) helps
you learn about Azure by answering questions, and it provides information tailored to your own Azure
resources and environment. By letting you express your goals in natural language, Copilot simplifies
your Azure management experience. This benefits Azure CLI users because the knowledge of Azure CLI
is built into Copilot.

Access Microsoft Copilot for Azure (preview) in the Azure portal, and tell Copilot what you would
like to do using Azure CLI. For example:

- I want to create a virtual machine using Azure CLI.
- I want to update service principal credentials using Azure CLI.
- I want to create a web app using Azure CLI.

To enable access to Microsoft Copilot for Azure (preview) for your organization,
[complete the registration form][18]. The application process only needs to be completed once per
tenant. Check with your administrator if you have questions about joining the preview.

## Reduced Docker image size

With the release of Azure CLI version 2.54.0, the size of the Docker image of `azure-cli` is reduced
from 1.1 GB to 700 MB. This reduction is a 36.3% decrease, resulting in improved download speed and
faster startup. For more information, see "Trim Azure CLI's docker image size" in
[Azure Command-line Tools Ignite 2023 Announcement][20].

## 64-bit Windows install

You can now [install the Azure CLI on Windows][21] with a 64-bit MSI. The 32-bit MSI, PowerShell
command, and Windows Package Manager are still available, but the 64-bit MSI is new. Anytime you
install the Azure CLI, previously installed versions are updated automatically. This behavior allows
you to try out the 64-bit install but reinstall the 32-bit MSI if you choose.

## ZIP file Windows install

Beginning in [Azure CLI 2.57.0][07], Azure CLI can be installed using a ZIP file in Windows
environments. See the ZIP tab in [Install Azure CLI on Windows][03] for more information.

## Tab completion in PowerShell

If you run Azure CLI in PowerShell, tab completion is now available. Follow the instructions in
[enable tab completion on PowerShell][14]. The parameter values needed for PowerShell's
`Register-ArgumentCompleter` command are provided in the article.

Tab completion is also available in [Azure Cloud Shell][09] and in most Linux distributions.

## Sign in with Web Account Manager (WAM)

The Azure CLI now offers preview support for sign in with Web Account Manager (WAM). Read about the
benefits of WAM and how to enable the feature in [Sign in with Web Account Manager][13].

## Reference type and status

Reference type and status information is now available in Azure CLI reference content. Why is this
important? Reference command status determines the support level.

You see this information in three places:

- **New "type" and "status" columns in reference list tables.**

  ![status table][05]

  For a live example, see the [reference index][15] or drill down to [az account][11].

- **New status indicators under command names.**

  ![status badges][04]

  If there's no status indicator, the command group or reference command is generally available
  (GA). For a live example, see [az account subscription][12].

- **New status indicator for parameters.** Only deprecated parameters show a status. All other
  parameters inherit the status of the reference command.

For more information on Azure CLI statuses, see [Azure CLI terminology and support levels][06].

## New onboarding tools

Are you new to Azure CLI? Check out the new Onboarding Cheat Sheet to jump-start your journey, and
find code examples in the A to Z indexes.

- [Onboarding cheat sheet][16]
- [Azure CLI conceptual article index][22]
- [Azure CLI sample index][23]

<!-- link references -->

[01]: ./authenticate-azure-cli-interactively.md#interactive-login
[02]: ./azure-cli-manage-secrets.md
[03]: ./install-azure-cli-windows.md?tabs=zip#install-or-update
[04]: ./media/status-badges.png
[05]: ./media/status-table.png
[06]: ./reference-types-and-status.md#what-is-reference-status
[07]: ./release-notes-azure-cli.md#february-06-2024
[08]: ./run-azure-cli-docker.md
[09]: /azure/cloud-shell/quickstart?toc=%2Fcli%2Fazure%2Ftoc.json&bc=%2Fcli%2Fazure%2Fbreadcrumb%2Ftoc.json&tabs=azurecli
[10]: /azure/copilot/ai-shell-overview
[11]: /cli/azure/account
[12]: /cli/azure/account/subscription
[13]: /cli/azure/authenticate-azure-cli#sign-in-with-web-account-manager-wam
[14]: /cli/azure/install-azure-cli-windows#enable-tab-completion-on-powershell
[15]: /cli/azure/reference-index
[16]: cheat-sheet-onboarding.md
[17]: https://aka.ms/MicrosoftCopilotforAzureDocs
[18]: https://aka.ms/MSCopilotforAzurePreviewRequest
[19]: https://techcommunity.microsoft.com/blog/azuretoolsblog/azure-cli-and-azure-powershell-ignite-2024-announcement/4304204
[20]: https://techcommunity.microsoft.com/t5/azure-tools-blog/azure-command-line-tools-ignite-2023-announcement/ba-p/3984502
[21]: install-azure-cli-windows.md
[22]: reference-docs-index.md
[23]: samples-index.md
