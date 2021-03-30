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
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Обновление маршрута с помощью Ртмупдатеандунлоккрауте

Следующая процедура описывает шаги, используемые для обновления маршрута. В приведенном ниже образце кода показано, как реализовать процедуру.

**Чтобы обновить маршрут на месте, клиент должен выполнить следующие действия.**

1.  Блокировка маршрута путем вызова [**ртмлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute). В настоящее время эта функция фактически блокирует назначение маршрута. Диспетчер таблиц маршрутизации возвращает указатель на маршрут.
2.  Чтобы внести необходимые изменения в маршрут, используйте указатель [**на \_ \_ информационную**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) структуру диспетчера таблиц маршрутизации RTM, полученную на шаге 1. При обновлении на месте можно изменять только определенные члены структуры **\_ \_ сведений о маршруте RTM** . Эти элементы: **сосед**, **префинфо**, **ентитиспеЦифиЦинфо**, **белонгстовиевс** и **некссопслист**.
    > [!Note]  
    > Если клиент добавляет сведения либо к членам **соседа** , либо **некссопслист** , клиент должен вызвать [**ртмреференцехандлес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) , чтобы явно увеличить число ссылок, которое диспетчер таблиц маршрутизации хранит на объекте следующего прыжка. Аналогичным образом, если клиент удаляет данные из члена **некссопслист** , клиент должен вызвать [**ртмрелеасенекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , чтобы уменьшить число ссылок.

     

3.  Вызовите [**ртмупдатеандунлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) , чтобы уведомить диспетчер таблиц маршрутизации о том, что было выполнено изменение. Диспетчер таблиц маршрутизации фиксирует изменения, обновляет назначение, отражая новые сведения, а затем разблокирует маршрут.

В следующем примере кода показано, как обновить маршрут напрямую, используя указатель на фактические сведения о маршруте в таблице маршрутизации.


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



 

 




