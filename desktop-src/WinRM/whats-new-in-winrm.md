---
title: Новые возможности WinRM 2,0
description: Новые возможности доступны в служба удаленного управления Windows версии 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412607"
---
# <a name="whats-new-in-winrm-20"></a><span data-ttu-id="b7d75-104">Новые возможности WinRM 2,0</span><span class="sxs-lookup"><span data-stu-id="b7d75-104">What's New in WinRM 2.0</span></span>

<span data-ttu-id="b7d75-105">Новые возможности доступны в служба удаленного управления Windows версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7d75-105">New features are available in Windows Remote Management version 2.0.</span></span> <span data-ttu-id="b7d75-106">(WinRM 2,0)</span><span class="sxs-lookup"><span data-stu-id="b7d75-106">(WinRM 2.0)</span></span>

<span data-ttu-id="b7d75-107">WinRM 2,0 входит в Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7d75-107">WinRM 2.0 is included in Windows Server 2008 R2 and Windows 7.</span></span>

<span data-ttu-id="b7d75-108">Кроме того, можно загрузить WinRM 2,0 для Windows Server 2008 с пакетом обновления 2 (SP2) и Windows Vista с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="b7d75-108">You can also download WinRM 2.0 for Windows Server 2008 with Service Pack 2 (SP2) and Windows Vista with Service Pack 2 (SP2).</span></span> <span data-ttu-id="b7d75-109">Сведения о скачивании WinRM 2,0 см. в разделе [KB968929](https://support.microsoft.com/kb/968929).</span><span class="sxs-lookup"><span data-stu-id="b7d75-109">For information about downloading WinRM 2.0, see [KB968929](https://support.microsoft.com/kb/968929).</span></span>

<span data-ttu-id="b7d75-110">В следующей таблице приведена документация по WinRM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7d75-110">The following table lists the documentation for WinRM 2.0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7d75-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="b7d75-111">Topic</span></span></th>
<th><span data-ttu-id="b7d75-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b7d75-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7d75-113"><a href="client-shell-api.md">API оболочки клиента WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-113"><a href="client-shell-api.md">WinRM Client Shell API</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-114">Интерфейс прикладного программирования (API) оболочки клиента WinRM предоставляет функциональные возможности для создания оболочек, команд и потоков данных на удаленных компьютерах и управления ими.</span><span class="sxs-lookup"><span data-stu-id="b7d75-114">The WinRM Client Shell application programming interface (API) provides functionality to create and manage shells and shell operations, commands, and data streams on remote computers.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7d75-115"><a href="winrm-plugin-api.md">API подключаемого модуля WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-115"><a href="winrm-plugin-api.md">WinRM Plugin API</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-116">Интерфейс API подключаемого модуля WinRM предоставляет функциональные возможности, позволяющие пользователю создавать подключаемые модули, реализуя определенные API для поддерживаемых URI и операций с <a href="windows-remote-management-glossary.md"><em>ресурсами</em></a> .</span><span class="sxs-lookup"><span data-stu-id="b7d75-116">The WinRM Plug-in API provides functionality that enables a user to write plug-ins by implementing certain APIs for supported <a href="windows-remote-management-glossary.md"><em>resource URIs</em></a> and operations.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7d75-117"><a href="winrm-application-hosting.md">Инфраструктура для управления размещенными службами</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-117"><a href="winrm-application-hosting.md">Infrastructure for Managing Hosted Services</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-118">В WinRM 2,0 введена платформа размещения.</span><span class="sxs-lookup"><span data-stu-id="b7d75-118">WinRM 2.0 introduces a hosting framework.</span></span> <span data-ttu-id="b7d75-119">Поддерживаются две модели размещения.</span><span class="sxs-lookup"><span data-stu-id="b7d75-119">Two hosting models are supported.</span></span> <span data-ttu-id="b7d75-120">Одна из них — служба IIS, а другая — WinRM — на основе службы.</span><span class="sxs-lookup"><span data-stu-id="b7d75-120">One is Internet Information Service (IIS)–based and the other is WinRM–service based.</span></span> <br/> <span data-ttu-id="b7d75-121">Дополнительные сведения о конфигурации узла см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b7d75-121">For more information about the host configuration, see the following topics:</span></span><br/>
<ul>
<li><span data-ttu-id="b7d75-122"><a href="iis-host-plug-in-configuration.md">Конфигурация подключаемого модуля узла IIS</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-122"><a href="iis-host-plug-in-configuration.md">IIS Host Plug-in Configuration</a></span></span></li>
<li><span data-ttu-id="b7d75-123"><a href="wsman-service-plug-in-configuration.md">Конфигурация подключаемого модуля службы WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-123"><a href="wsman-service-plug-in-configuration.md">WinRM Service Plug-in Configuration</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7d75-124"><a href="dmtf-association-traversal.md">Обнаружение профиля DMTF с помощью обхода взаимосвязей</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-124"><a href="dmtf-association-traversal.md">DMTF Profile Discovery through Association Traversal</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-125">Обход ассоциации позволяет пользователю извлекать экземпляры классов взаимосвязей с помощью стандартного механизма фильтрации.</span><span class="sxs-lookup"><span data-stu-id="b7d75-125">Association traversal enables a user to retrieve instances of Association classes by using a standard filtering mechanism.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7d75-126"><a href="remote-shell-infrastructure-improvements.md">Усовершенствования инфраструктуры удаленной оболочки</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-126"><a href="remote-shell-infrastructure-improvements.md">Remote Shell infrastructure improvements</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-127">Этот раздел содержит сведения об улучшениях удаленной инфраструктуры для WinRM.</span><span class="sxs-lookup"><span data-stu-id="b7d75-127">This topic includes information about the remote infrastructure improvements for WinRM.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7d75-128"><a href="multi-hop-support.md">Поддержка нескольких прыжков</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-128"><a href="multi-hop-support.md">Multi-hop Support</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-129">В WinRM 2,0 добавлена функция, которая поддерживает делегирование учетных данных пользователя на нескольких удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="b7d75-129">Functionality was added to WinRM 2.0 that supports delegating user credentials across multiple remote computers.</span></span> <br/> <span data-ttu-id="b7d75-130">В разделе <a href="authentication-constants.md"><strong>константы проверки подлинности</strong></a> добавлена следующая константа: <strong>всманфлагусекредссп</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7d75-130">The <a href="authentication-constants.md"><strong>Authentication Constants</strong></a> topic was updated to add the following constant: <strong>WSManFlagUseCredSsp</strong>.</span></span><br/> <span data-ttu-id="b7d75-131">Следующий API C++ был добавлен для обеспечения поддержки нескольких прыжков: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7d75-131">The following C++ API was added to provide multi-hop support: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.</span></span><br/> <span data-ttu-id="b7d75-132">Добавлен следующий API скриптов для обеспечения поддержки нескольких прыжков: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. сессионфлагусекредссп</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7d75-132">The following scripting API was added to provide multi-hop support: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7d75-133"><a href="quotas.md">Управление квотами для удаленных оболочек</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-133"><a href="quotas.md">Quota Management for Remote Shells</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-134">В этом разделе содержатся сведения о настройке квот для управления удаленной оболочкой.</span><span class="sxs-lookup"><span data-stu-id="b7d75-134">This topic includes information about quota configuration for remote shell management.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7d75-135"><a href="winrm-powershell-commandlets.md">Управляемый Справочник по командам PowerShell WS-Management</a></span><span class="sxs-lookup"><span data-stu-id="b7d75-135"><a href="winrm-powershell-commandlets.md">Managed Reference for WS-Management PowerShell Commands</a></span></span><br/></td>
<td><span data-ttu-id="b7d75-136">Пользователи WinRM 2,0 могут использовать командлеты Windows PowerShell для управления системой.</span><span class="sxs-lookup"><span data-stu-id="b7d75-136">Users of WinRM 2.0 can use Windows PowerShell cmdlets for system management.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





