---
title: Маркировка маршрутов для состояния Hold-Down
description: Некоторые клиенты, такие как протоколы векторов расстояний, такие как RIP и ДВМРП, потребовали, чтобы целевые объекты были объявлены как недоступные в течение определенного времени после удаления последнего маршрута к назначению.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986569"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="caae6-103">Маркировка маршрутов для состояния Hold-Down</span><span class="sxs-lookup"><span data-stu-id="caae6-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="caae6-104">Некоторые клиенты, такие как протоколы векторов расстояний, такие как RIP и ДВМРП, потребовали, чтобы целевые объекты были объявлены как недоступные в течение определенного времени после удаления последнего маршрута к назначению.</span><span class="sxs-lookup"><span data-stu-id="caae6-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="caae6-105">Последний удаленный маршрут должен быть объявлен как недостижимый, даже если новые маршруты поступают.</span><span class="sxs-lookup"><span data-stu-id="caae6-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="caae6-106">Последний удаленный маршрут помечается как *находился в состоянии удержания*.</span><span class="sxs-lookup"><span data-stu-id="caae6-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="caae6-107">Процесс удержания предотвращает образование циклов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="caae6-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="caae6-108">Циклы маршрутизации вызываются, когда протокол маршрутизации объявляет об устаревшей информации о маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="caae6-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="caae6-109">По истечении срока хранения эти протоколы возобновляют объявление с помощью нового лучшего маршрута.</span><span class="sxs-lookup"><span data-stu-id="caae6-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="caae6-110">Протокол, реализующий состояния удержания, указывает, что назначение находится в состоянии удержания с помощью функции [**ртмхолддестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) .</span><span class="sxs-lookup"><span data-stu-id="caae6-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="caae6-111">Клиент вызывает эту функцию, когда она объявляет оптимальный маршрут к этому назначению.</span><span class="sxs-lookup"><span data-stu-id="caae6-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="caae6-112">Если впоследствии все маршруты к этому назначению будут удалены, последний удаленный маршрут сохраняется в состоянии удержания в течение периода времени, указанного в предыдущем вызове **ртмхолддестинатион**.</span><span class="sxs-lookup"><span data-stu-id="caae6-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="caae6-113">Когда протокол объявляет назначение, используемые сведения о маршруте зависят от того, использует ли протокол состояния удержания, и если маршрут находится в состоянии удержания для назначения.</span><span class="sxs-lookup"><span data-stu-id="caae6-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="caae6-114">Протоколы, которые не используют состояния удержания, могут игнорировать сведения о маршруте, относящиеся к состояниям удержания для назначения, и всегда объявлять оптимальный маршрут.</span><span class="sxs-lookup"><span data-stu-id="caae6-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="caae6-115">Пример кода, демонстрирующий использование этих функций, см. [в разделе Использование состояния Hold-Down маршрута](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="caae6-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




