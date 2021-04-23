---
title: Сведения о диспетчере таблиц маршрутизации версии 2
description: В следующей документации описывается технология диспетчера таблиц маршрутизации версии 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 2
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 2, описание
- Диспетчер таблиц маршрутизации, служба RRAS версии 2
- Диспетчер таблиц маршрутизации, версия 2 RRAS, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068096"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="fd5c1-107">Сведения о диспетчере таблиц маршрутизации версии 2</span><span class="sxs-lookup"><span data-stu-id="fd5c1-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="fd5c1-108">В следующей документации описывается технология диспетчера таблиц маршрутизации версии 2 (RTMv2).</span><span class="sxs-lookup"><span data-stu-id="fd5c1-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="fd5c1-109">API RTMv2 — это компонент Windows 2000 и более поздних операционных систем, которые можно использовать для записи протоколов маршрутизации, взаимодействующих с диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fd5c1-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="fd5c1-110">Диспетчер таблиц маршрутизации является центральным репозиторием сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).</span><span class="sxs-lookup"><span data-stu-id="fd5c1-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="fd5c1-111">RTMv2 недоступен для Windows NT версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="fd5c1-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="fd5c1-112">Кроме того, RTMv2 нельзя использовать для протоколов IPX-маршрутизации, работающих в Windows NT 4,0 или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fd5c1-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="fd5c1-113">При использовании протокола IPX или записи протоколов маршрутизации для Windows NT 4,0 обратитесь к статье [о маршрутизации диспетчера таблиц версии 1](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="fd5c1-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="fd5c1-114">В этом обзоре описываются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="fd5c1-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="fd5c1-115">Компоненты архитектуры диспетчера таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="fd5c1-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="fd5c1-116">Регистрация в диспетчере таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="fd5c1-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="fd5c1-117">Перечисление зарегистрированных сущностей</span><span class="sxs-lookup"><span data-stu-id="fd5c1-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="fd5c1-118">Использование методов</span><span class="sxs-lookup"><span data-stu-id="fd5c1-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="fd5c1-119">Использование непрозрачных указателей</span><span class="sxs-lookup"><span data-stu-id="fd5c1-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="fd5c1-120">Маркировка маршрутов для состояния Hold-Down</span><span class="sxs-lookup"><span data-stu-id="fd5c1-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="fd5c1-121">Добавление маршрутов</span><span class="sxs-lookup"><span data-stu-id="fd5c1-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="fd5c1-122">Получение сведений о маршруте</span><span class="sxs-lookup"><span data-stu-id="fd5c1-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="fd5c1-123">Обновление маршрутов</span><span class="sxs-lookup"><span data-stu-id="fd5c1-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="fd5c1-124">Получение уведомлений об изменениях</span><span class="sxs-lookup"><span data-stu-id="fd5c1-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="fd5c1-125">Работа со следующими прыжками</span><span class="sxs-lookup"><span data-stu-id="fd5c1-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="fd5c1-126">Перечисление записей таблицы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="fd5c1-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="fd5c1-127">Поиск конкретных сведений в таблице маршрутизации</span><span class="sxs-lookup"><span data-stu-id="fd5c1-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="fd5c1-128">Обслуживание списков Client-Specific</span><span class="sxs-lookup"><span data-stu-id="fd5c1-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="fd5c1-129">Управление дескрипторами</span><span class="sxs-lookup"><span data-stu-id="fd5c1-129">Managing Handles</span></span>](managing-handles.md)

 

 




