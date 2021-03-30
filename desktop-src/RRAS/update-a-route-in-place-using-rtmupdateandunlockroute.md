---
title: Обновление маршрута с помощью Ртмупдатеандунлоккрауте
description: Следующая процедура описывает шаги, используемые для обновления маршрута. В приведенном ниже образце кода показано, как реализовать процедуру.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411117"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="dfcd6-104">Обновление маршрута с помощью Ртмупдатеандунлоккрауте</span><span class="sxs-lookup"><span data-stu-id="dfcd6-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="dfcd6-105">Следующая процедура описывает шаги, используемые для обновления маршрута.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="dfcd6-106">В приведенном ниже образце кода показано, как реализовать процедуру.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="dfcd6-107">**Чтобы обновить маршрут на месте, клиент должен выполнить следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="dfcd6-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="dfcd6-108">Блокировка маршрута путем вызова [**ртмлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="dfcd6-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="dfcd6-109">В настоящее время эта функция фактически блокирует назначение маршрута.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="dfcd6-110">Диспетчер таблиц маршрутизации возвращает указатель на маршрут.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="dfcd6-111">Чтобы внести необходимые изменения в маршрут, используйте указатель [**на \_ \_ информационную**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) структуру диспетчера таблиц маршрутизации RTM, полученную на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="dfcd6-112">При обновлении на месте можно изменять только определенные члены структуры **\_ \_ сведений о маршруте RTM** .</span><span class="sxs-lookup"><span data-stu-id="dfcd6-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="dfcd6-113">Эти элементы: **сосед**, **префинфо**, **ентитиспеЦифиЦинфо**, **белонгстовиевс** и **некссопслист**.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="dfcd6-114">Если клиент добавляет сведения либо к членам **соседа** , либо **некссопслист** , клиент должен вызвать [**ртмреференцехандлес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) , чтобы явно увеличить число ссылок, которое диспетчер таблиц маршрутизации хранит на объекте следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="dfcd6-115">Аналогичным образом, если клиент удаляет данные из члена **некссопслист** , клиент должен вызвать [**ртмрелеасенекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , чтобы уменьшить число ссылок.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="dfcd6-116">Вызовите [**ртмупдатеандунлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) , чтобы уведомить диспетчер таблиц маршрутизации о том, что было выполнено изменение.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="dfcd6-117">Диспетчер таблиц маршрутизации фиксирует изменения, обновляет назначение, отражая новые сведения, а затем разблокирует маршрут.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="dfcd6-118">В следующем примере кода показано, как обновить маршрут напрямую, используя указатель на фактические сведения о маршруте в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dfcd6-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




