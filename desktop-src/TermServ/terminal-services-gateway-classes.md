---
title: Классы шлюзов удаленный рабочий стол
description: Поставщик WMI шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) предоставляет следующие классы.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778827"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="cb9e6-103">Классы шлюзов удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="cb9e6-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="cb9e6-104">Поставщик WMI шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) предоставляет следующие классы.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb9e6-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="cb9e6-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cb9e6-106">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="cb9e6-107">Представляет подключение от клиентского компьютера к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-108">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="cb9e6-109">Описание политики авторизации подключений удаленный рабочий стол (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="cb9e6-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="cb9e6-110">С помощью RD CAP можно определить, разрешено ли пользователю подключаться к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-111">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="cb9e6-112">Описывает набор серверов балансировки нагрузки шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="cb9e6-113">Они используются для балансировки нагрузки подключений к шлюзу удаленных рабочих столов на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-114">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="cb9e6-115">Описывает сервер протокол RADIUS (RADIUS) с набором политик авторизации подключений (RD CAP) службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-116">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="cb9e6-117">Описание политики авторизации ресурсов (RD RAP) удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="cb9e6-118">Политика авторизации ресурсов удаленных рабочих столов используется для принятия решения о том, разрешено ли пользователю подключаться к указанному ресурсу через шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-119">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="cb9e6-120">Описывает группу ресурсов, которая сопоставляет набор ресурсов (имен компьютеров) с одной сущностью.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-121">**\_Тсгатевайсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="cb9e6-122">Используется для операций, связанных с сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="cb9e6-123">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="cb9e6-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="cb9e6-124">Предоставляет методы и свойства для просмотра и настройки параметров сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cb9e6-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




