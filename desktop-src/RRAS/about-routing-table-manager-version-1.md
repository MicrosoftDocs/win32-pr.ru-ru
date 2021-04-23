---
title: Сведения о диспетчере таблиц маршрутизации версии 1
description: Диспетчер таблиц маршрутизации — это центральное хранилище сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 1
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации версии 1, описание
- Диспетчер таблиц маршрутизации, версия 1 RRAS
- Диспетчер таблиц маршрутизации, версия 1 RRAS, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068097"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="d3923-107">Сведения о диспетчере таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="d3923-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="d3923-108">**Windows Server 2003:** Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3923-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d3923-109">Новые приложения должны использовать API диспетчера таблиц маршрутизации версии 2.</span><span class="sxs-lookup"><span data-stu-id="d3923-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="d3923-110">Диспетчер таблиц маршрутизации — это центральное хранилище сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).</span><span class="sxs-lookup"><span data-stu-id="d3923-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="d3923-111">Диспетчер таблиц маршрутизации предоставляет сведения о маршрутизации всем заинтересованным компонентам, таким как протоколы маршрутизации, агенты управления и агенты наблюдения.</span><span class="sxs-lookup"><span data-stu-id="d3923-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="d3923-112">Диспетчер таблиц маршрутизации также определяет оптимальный маршрут к каждой целевой сети, известной протоколам маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d3923-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="d3923-113">Он определяет этот маршрут на основе приоритетов протоколов маршрутизации и метрик, связанных с маршрутами.</span><span class="sxs-lookup"><span data-stu-id="d3923-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="d3923-114">Обратите внимание, что администратор может настроить приоритеты протоколов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d3923-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="d3923-115">Затем диспетчер таблиц маршрутизации передает сведения о наилучшем маршруте серверам пересылки и обратно в протоколы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d3923-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="d3923-116">Каждый протокол маршрутизации вызывает [**ртмрегистерклиент**](rtmregisterclient.md) для регистрации в диспетчере таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d3923-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="d3923-117">**Ртмрегистерклиент** возвращает маркер, используемый протоколом маршрутизации для добавления или удаления записей маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d3923-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="d3923-118">**Ртмрегистерклиент** также позволяет протоколу маршрутизации регистрировать объект события с помощью диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d3923-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="d3923-119">Диспетчер таблиц маршрутизации передает этот объект события, чтобы уведомить протокол маршрутизации об изменениях в данных наилучшего маршрута.</span><span class="sxs-lookup"><span data-stu-id="d3923-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="d3923-120">Все остальные компоненты могут получать сведения, хранящиеся в диспетчере таблиц маршрутизации через перечисление маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d3923-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




