---
title: Обновление маршрутов с помощью Ртмаддраутетодест
description: Если клиент не требует повышения эффективности при добавлении маршрута, он должен использовать следующий метод обновления маршрутов.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986755"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="c930d-103">Обновление маршрутов с помощью Ртмаддраутетодест</span><span class="sxs-lookup"><span data-stu-id="c930d-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="c930d-104">Если клиент не требует повышения эффективности при добавлении маршрута, он должен использовать следующий метод обновления маршрутов.</span><span class="sxs-lookup"><span data-stu-id="c930d-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="c930d-105">Этот метод менее эффективен, так как он требует получения маркера маршрута и передачи структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) в диспетчер таблиц маршрутизации и обратно.</span><span class="sxs-lookup"><span data-stu-id="c930d-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="c930d-106">Этот метод также занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="c930d-106">This method also takes more time.</span></span> <span data-ttu-id="c930d-107">Так как [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) не манипулирует таблицей маршрутизации напрямую, использование этого метода экономично для простоты.</span><span class="sxs-lookup"><span data-stu-id="c930d-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="c930d-108">Пример кода, демонстрирующий использование этих функций, см. в разделе [Добавление и обновление маршрутов с помощью ртмаддраутетодест](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="c930d-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




