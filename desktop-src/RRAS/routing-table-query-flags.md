---
title: Флаги запроса таблицы маршрутизации
description: Используйте эти константы для запросов к таблицам маршрутизатора.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Флаги запроса таблицы маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889263"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="e0a10-104">Флаги запроса таблицы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="e0a10-104">Routing Table Query Flags</span></span>

<span data-ttu-id="e0a10-105">Используйте эти константы для запросов к таблицам маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="e0a10-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="e0a10-106">Константа</span><span class="sxs-lookup"><span data-stu-id="e0a10-106">Constant</span></span>              | <span data-ttu-id="e0a10-107">Значение</span><span class="sxs-lookup"><span data-stu-id="e0a10-107">Value</span></span>      | <span data-ttu-id="e0a10-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e0a10-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e0a10-109">\_нет соответствия \_ RTM</span><span class="sxs-lookup"><span data-stu-id="e0a10-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="e0a10-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0a10-110">0x00000000</span></span> | <span data-ttu-id="e0a10-111">Соответствует ни одному из критериев; возвращаются все маршруты для назначения.</span><span class="sxs-lookup"><span data-stu-id="e0a10-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="e0a10-112">\_владелец соответствия \_ RTM</span><span class="sxs-lookup"><span data-stu-id="e0a10-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="e0a10-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e0a10-113">0x00000001</span></span> | <span data-ttu-id="e0a10-114">Сопоставление маршрутов с одним и тем же владельцем.</span><span class="sxs-lookup"><span data-stu-id="e0a10-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="e0a10-115">\_сосед по СООТВЕТСТВИЮ RTM \_</span><span class="sxs-lookup"><span data-stu-id="e0a10-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="e0a10-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e0a10-116">0x00000002</span></span> | <span data-ttu-id="e0a10-117">Сопоставление маршрутов с тем же соседом.</span><span class="sxs-lookup"><span data-stu-id="e0a10-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="e0a10-118">\_преф совпадений RTM \_</span><span class="sxs-lookup"><span data-stu-id="e0a10-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="e0a10-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e0a10-119">0x00000004</span></span> | <span data-ttu-id="e0a10-120">Соответствует маршрутам с одинаковым предпочтением.</span><span class="sxs-lookup"><span data-stu-id="e0a10-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="e0a10-121">\_следующий прыжок для соответствия RTM \_</span><span class="sxs-lookup"><span data-stu-id="e0a10-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="e0a10-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e0a10-122">0x00000008</span></span> | <span data-ttu-id="e0a10-123">Совпадает с маршрутами, которые имеют одинаковый следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="e0a10-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="e0a10-124">\_интерфейс соответствия \_ RTM</span><span class="sxs-lookup"><span data-stu-id="e0a10-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="e0a10-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0a10-125">0x00000010</span></span> | <span data-ttu-id="e0a10-126">Соответствует маршрутам, которые находятся в одном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e0a10-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="e0a10-127">\_полное совпадение RTM \_</span><span class="sxs-lookup"><span data-stu-id="e0a10-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="e0a10-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="e0a10-128">0x0000FFFF</span></span> | <span data-ttu-id="e0a10-129">Сопоставление маршрутов со всеми критериями.</span><span class="sxs-lookup"><span data-stu-id="e0a10-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="e0a10-130">\_оптимальный \_ протокол RTM</span><span class="sxs-lookup"><span data-stu-id="e0a10-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="e0a10-131">0</span><span class="sxs-lookup"><span data-stu-id="e0a10-131">0</span></span>          | <span data-ttu-id="e0a10-132">Возвращает маршрут независимо от того, какой протокол является его владельцем.</span><span class="sxs-lookup"><span data-stu-id="e0a10-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="e0a10-133">RTM \_ этот \_ протокол</span><span class="sxs-lookup"><span data-stu-id="e0a10-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="e0a10-134">~0</span><span class="sxs-lookup"><span data-stu-id="e0a10-134">~0</span></span>         | <span data-ttu-id="e0a10-135">Возвращает оптимальный маршрут для вызывающего протокола.</span><span class="sxs-lookup"><span data-stu-id="e0a10-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




