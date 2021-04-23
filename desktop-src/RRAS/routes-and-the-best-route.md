---
title: Маршруты и оптимальный маршрут
description: Маршрут — это \ 0034; сетевой путь \ 0034; к назначению, связанному с определенными затратами. Стоимость представляется с помощью административных настроек и определенной для протокола метрики. Маршруты с более низкими затратами предпочтительнее всех остальных маршрутов.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672178"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="e20b4-105">Маршруты и оптимальный маршрут</span><span class="sxs-lookup"><span data-stu-id="e20b4-105">Routes and the Best Route</span></span>

<span data-ttu-id="e20b4-106">Маршрут — это "сетевой путь" к назначению, с которым связана определенная стоимость.</span><span class="sxs-lookup"><span data-stu-id="e20b4-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="e20b4-107">Стоимость представляется с помощью административных настроек и определенной для протокола метрики.</span><span class="sxs-lookup"><span data-stu-id="e20b4-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="e20b4-108">Маршруты с более низкими затратами предпочтительнее всех остальных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e20b4-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="e20b4-109">Запись маршрута в таблице маршрутизации включает:</span><span class="sxs-lookup"><span data-stu-id="e20b4-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="e20b4-110">Маркер назначения</span><span class="sxs-lookup"><span data-stu-id="e20b4-110">A handle to the destination</span></span>
-   <span data-ttu-id="e20b4-111">Владелец маршрута</span><span class="sxs-lookup"><span data-stu-id="e20b4-111">The owner of this route</span></span>
-   <span data-ttu-id="e20b4-112">Сосед (узел), который предоставил сведения о маршруте</span><span class="sxs-lookup"><span data-stu-id="e20b4-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="e20b4-113">Флаги, связанные с состоянием маршрута</span><span class="sxs-lookup"><span data-stu-id="e20b4-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="e20b4-114">Флаги, связанные с маршрутом</span><span class="sxs-lookup"><span data-stu-id="e20b4-114">Flags associated with the route</span></span>
-   <span data-ttu-id="e20b4-115">Приоритет и метрика маршрута</span><span class="sxs-lookup"><span data-stu-id="e20b4-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="e20b4-116">Список представлений, к которым относится маршрут</span><span class="sxs-lookup"><span data-stu-id="e20b4-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="e20b4-117">Сведения, являющиеся частными для владельца маршрута</span><span class="sxs-lookup"><span data-stu-id="e20b4-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="e20b4-118">Список следующих прыжков, используемых для достижения места назначения</span><span class="sxs-lookup"><span data-stu-id="e20b4-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="e20b4-119">Следующие значения вместе однозначно определяют маршрут в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e20b4-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="e20b4-120">Целевая сеть</span><span class="sxs-lookup"><span data-stu-id="e20b4-120">The destination network</span></span>
-   <span data-ttu-id="e20b4-121">Владелец маршрута</span><span class="sxs-lookup"><span data-stu-id="e20b4-121">The owner of the route</span></span>
-   <span data-ttu-id="e20b4-122">Сосед, который указал маршрут</span><span class="sxs-lookup"><span data-stu-id="e20b4-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="e20b4-123">Метрики и предпочтения</span><span class="sxs-lookup"><span data-stu-id="e20b4-123">Metrics and Preference</span></span>

<span data-ttu-id="e20b4-124">Каждый маршрут имеет административные настройки (заданные политикой маршрутизации) и зависимую от клиента метрику.</span><span class="sxs-lookup"><span data-stu-id="e20b4-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="e20b4-125">Диспетчер таблиц маршрутизации использует эти сведения, чтобы определить, какой маршрут является лучшим маршрутом к назначению.</span><span class="sxs-lookup"><span data-stu-id="e20b4-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="e20b4-126">Маршруты с более низким приоритетом — это лучшие маршруты (один из них самый низкий и, следовательно, лучший).</span><span class="sxs-lookup"><span data-stu-id="e20b4-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="e20b4-127">Если два маршрута имеют одинаковый приоритет, лучше использовать маршрут с нижней метрикой.</span><span class="sxs-lookup"><span data-stu-id="e20b4-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="e20b4-128">Как правило, предпочтение маршрута определяется предпочтением клиента, который добавил маршрут.</span><span class="sxs-lookup"><span data-stu-id="e20b4-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="e20b4-129">Однако для всех маршрутов, добавленных с помощью средства управления Netsh.exe, значение предпочтения можно указать для каждого маршрута.</span><span class="sxs-lookup"><span data-stu-id="e20b4-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="e20b4-130">Предпочтение обычно используется для обозначения приоритета между клиентами.</span><span class="sxs-lookup"><span data-stu-id="e20b4-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="e20b4-131">Например, администратор может назначить OSPF более низкому (лучшему) приоритету по сравнению с RIP.</span><span class="sxs-lookup"><span data-stu-id="e20b4-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="e20b4-132">В этом случае OSPF-маршруты предпочтительнее RIP-маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e20b4-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




