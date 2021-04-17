---
title: Работа со следующими прыжками
description: API RTMv2 позволяет клиентам работать со списком следующих прыжков, связанных с маршрутами и назначениями.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411320"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="b6eb6-103">Работа со следующими прыжками</span><span class="sxs-lookup"><span data-stu-id="b6eb6-103">Working with Next Hops</span></span>

<span data-ttu-id="b6eb6-104">API RTMv2 позволяет клиентам работать со списком следующих прыжков, связанных с маршрутами и назначениями.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="b6eb6-105">Клиенты могут добавлять или обновлять следующий прыжок, вызывая [**ртмадднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="b6eb6-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="b6eb6-106">Клиенты могут удалить следующий прыжок с помощью [**ртмделетенекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span><span class="sxs-lookup"><span data-stu-id="b6eb6-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="b6eb6-107">Клиенты могут искать следующие прыжки, вызывая [**ртмфинднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span><span class="sxs-lookup"><span data-stu-id="b6eb6-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="b6eb6-108">Клиенты также могут напрямую обновить следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="b6eb6-109">Для этого клиент должен сначала заблокировать следующий прыжок с помощью функции [**ртмлоккнекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) .</span><span class="sxs-lookup"><span data-stu-id="b6eb6-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="b6eb6-110">Затем клиент может использовать прямой указатель на [**\_ \_ информационную структуру RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) диспетчера таблиц маршрутизации для внесения необходимых изменений.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="b6eb6-111">Наконец, клиент может разблокировать следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="b6eb6-112">Поля адреса и индекса следующего прыжка в следующем прыжке однозначно определяют следующий прыжок и не должны изменяться.</span><span class="sxs-lookup"><span data-stu-id="b6eb6-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




