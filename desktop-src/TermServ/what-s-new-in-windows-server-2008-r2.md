---
title: Новые возможности Windows Server 2008 R2
description: В Windows Server 2008 R2 появились следующие новые программные элементы для службы удаленных рабочих столов.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103987150"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="dd9e9-103">Новые возможности Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd9e9-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="dd9e9-104">В Windows Server 2008 R2 появились следующие новые программные элементы для службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd9e9-105">Службы терминалов теперь службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="dd9e9-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="dd9e9-106">Службы терминалов были переименованы службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="dd9e9-107">Сервер, на котором установлена служба роли узла сеансов удаленный рабочий стол (удаленных рабочих столов), теперь называется сервером узла сеансов удаленных рабочих столов, а не сервером терминалов.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="dd9e9-108"><a href="terminal-services-is-now-remote-desktop-services.md">Службы терминалов теперь службы удаленных рабочих столов</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd9e9-109">API виртуализации удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="dd9e9-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="dd9e9-110">Удаленный рабочий стол API виртуализации предоставляет перечисления, интерфейсы и структуры, которые можно использовать для создания пользовательских подключаемых модулей, переопределяющих стандартную логику перенаправления подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="dd9e9-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="dd9e9-111">RDCB (ранее назывался посредником сеансов служб терминалов) был расширен для поддержки подключений к виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="dd9e9-112"><a href="using-the-remote-desktop-virtualization-api.md">Использование API виртуализации удаленный рабочий стол</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="dd9e9-113"><a href="terminal-services-virtualization-api-reference.md">Справочник по API виртуализации удаленный рабочий стол</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd9e9-114">Поставщик протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="dd9e9-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="dd9e9-115">API поставщика протокол удаленного рабочего стола можно использовать для создания протокола, который настраивает взаимодействие между службами службы удаленных рабочих столов и настольными клиентами.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="dd9e9-116"><a href="creating-a-custom-remote-protocol.md">Создание поставщика протокол удаленного рабочего стола</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="dd9e9-117"><a href="custom-remote-protocol-reference.md">Справочник по поставщику протокол удаленного рабочего стола</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd9e9-118">службы удаленных рабочих столов API Аудиоендпоинт</span><span class="sxs-lookup"><span data-stu-id="dd9e9-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="dd9e9-119">Службы удаленных рабочих столов API Аудиоендпоинт поддерживает перечисление, интерфейсы и структуры для регистрации конечной точки аудио и передачи данных.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="dd9e9-120"><a href="terminal-services-audioendpoint-api-reference.md">Справочник по API службы удаленных рабочих столов Аудиоендпоинт</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd9e9-121">API службы управление подключениями к удаленным рабочим столам и приложениям RemoteApp</span><span class="sxs-lookup"><span data-stu-id="dd9e9-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="dd9e9-122">API службы управление подключениями к удаленным рабочим столам и приложениям RemoteApp поддерживает интерфейсы и структуры, которые можно использовать для выполнения настраиваемой фильтрации ресурсов и обеспечения поддержки типов файлов, которые изначально не поддерживаются в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dd9e9-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="dd9e9-123"><a href="centralized-publishing-api-reference.md">Справочник по API службы управление подключениями к удаленным рабочим столам и приложениям RemoteApp</a></span><span class="sxs-lookup"><span data-stu-id="dd9e9-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





