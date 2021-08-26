---
title: Добавление и обновление маршрутов с помощью Ртмаддраутетодест
description: Функция Ртмаддраутетодест используется для добавления новых маршрутов и обновления существующих маршрутов для назначения. В обоих случаях описаны следующие процедуры. В приведенном ниже образце кода показано, как реализовать первую процедуру.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030604"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Добавление и обновление маршрутов с помощью Ртмаддраутетодест

Функция [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) используется для добавления новых маршрутов и обновления существующих маршрутов для назначения. В обоих случаях описаны следующие процедуры. В приведенном ниже образце кода показано, как реализовать первую процедуру.

**Чтобы добавить маршрут, клиент должен выполнить следующие действия.**

1.  Если клиент уже кэширует обработчик следующего прыжка, перейдите к шагу 4.
2.  Создайте структуру [**\_ \_ сведений о NEXTHOP в RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) и заполните ее соответствующей информацией.
3.  Добавьте следующий прыжок в таблицу маршрутизации, вызвав [**ртмадднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Диспетчер таблиц маршрутизации возвращает маркер следующего прыжка. Если следующий прыжок уже существует, таблица маршрутизации не добавляет следующий прыжок; Вместо этого он возвращает маркер следующему прыжку.
4.  Создайте структуру [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) и заполните ее соответствующей информацией, включая маркер следующего прыжка, возвращенный диспетчером таблиц маршрутизации.
5.  Добавьте маршрут в таблицу маршрутизации, вызвав [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest). Диспетчер таблиц маршрутизации сравнивает новый маршрут с маршрутами, которые уже находятся в таблице маршрутизации. Два маршрута равны, если выполняются все перечисленные ниже условия.

    -   Маршрут добавляется в то же место назначения.
    -   Маршрут добавляется тем же клиентом, который указан членом **owner** структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .
    -   Маршрут объявляется тем же соседом, который указан в **соседнем** элементе структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .

    Если маршрут существует, диспетчер таблиц маршрутизации возвращает маркер существующего маршрута. В противном случае диспетчер таблиц маршрутизации добавляет маршрут и возвращает его в новый маршрут.

    Клиент может присвоить параметру *Change \_ flags* значение RTM \_ \_ Change маршрута \_ New, чтобы диспетчер таблиц маршрутизации мог добавить новый маршрут в место назначения, даже если существует другой маршрут с теми же полями владельца и соседей.

    Клиент может присвоить параметру *Change \_ flags* значение RTM Change, чтобы \_ \_ \_ сообщить диспетчеру таблиц маршрутизации, что необходимо обновить первый маршрут в месте назначения, принадлежащем клиенту. Это обновление можно выполнить, если такой маршрут существует, даже если поле соседа не совпадает. Этот флаг используется клиентами, которые поддерживают один маршрут для каждого места назначения.

**Чтобы обновить маршрут, клиент должен выполнить следующие действия.**

1.  Вызовите [**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) с помощью маркера маршрута. Этот обработчик был либо ранее кэшированным клиентом, либо возвращенный диспетчером таблиц маршрутизации из вызова, возвращающего маркер маршрута, такой как **ртмжетраутеинфо**.
2.  Внесите изменения в структуру [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) , которая возвращается диспетчером таблиц маршрутизации.
3.  Вызовите [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) с помощью маркера маршрута и измененной [**структуры \_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .

В следующем примере кода показано, как добавить маршрут к назначению с помощью диспетчера таблиц маршрутизации в качестве посредника.


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




