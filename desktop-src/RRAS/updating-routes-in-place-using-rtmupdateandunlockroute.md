---
title: Обновление маршрутов на месте с помощью Ртмупдатеандунлоккрауте
description: Обновление на месте, как правило, более эффективно, чем обновление таблицы маршрутизации с помощью косвенного метода, такого как, который используется функцией Ртмаддраутетодест.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068133"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="ea42b-103">Обновление маршрутов на месте с помощью Ртмупдатеандунлоккрауте</span><span class="sxs-lookup"><span data-stu-id="ea42b-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="ea42b-104">Обновление на месте, как правило, более эффективно, чем обновление таблицы маршрутизации с помощью косвенного метода, такого как, который используется функцией [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) .</span><span class="sxs-lookup"><span data-stu-id="ea42b-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="ea42b-105">Этот метод более эффективен, поскольку клиенту не требуется получение маркера или передача структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) в диспетчер таблиц маршрутизации и из него.</span><span class="sxs-lookup"><span data-stu-id="ea42b-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="ea42b-106">Этот метод также занимает меньше времени.</span><span class="sxs-lookup"><span data-stu-id="ea42b-106">This method also takes less time.</span></span> <span data-ttu-id="ea42b-107">Однако непосредственное обновление таблицы маршрутизации может быть рискованным, так как диспетчер таблиц маршрутизации не функционирует как посредник.</span><span class="sxs-lookup"><span data-stu-id="ea42b-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="ea42b-108">Пример кода, демонстрирующий использование этих функций, см. [в разделе Обновление маршрута на месте с помощью ртмупдатеандунлоккрауте](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="ea42b-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




