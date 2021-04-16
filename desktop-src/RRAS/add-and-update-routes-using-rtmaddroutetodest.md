---
title: Добавление и обновление маршрутов с помощью Ртмаддраутетодест
description: Функция Ртмаддраутетодест используется для добавления новых маршрутов и обновления существующих маршрутов для назначения. В обоих случаях описаны следующие процедуры. В приведенном ниже образце кода показано, как реализовать первую процедуру.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672094"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="dffe8-105">Добавление и обновление маршрутов с помощью Ртмаддраутетодест</span><span class="sxs-lookup"><span data-stu-id="dffe8-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="dffe8-106">Функция [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) используется для добавления новых маршрутов и обновления существующих маршрутов для назначения.</span><span class="sxs-lookup"><span data-stu-id="dffe8-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="dffe8-107">В обоих случаях описаны следующие процедуры.</span><span class="sxs-lookup"><span data-stu-id="dffe8-107">The following procedures explain both cases.</span></span> <span data-ttu-id="dffe8-108">В приведенном ниже образце кода показано, как реализовать первую процедуру.</span><span class="sxs-lookup"><span data-stu-id="dffe8-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="dffe8-109">**Чтобы добавить маршрут, клиент должен выполнить следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="dffe8-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="dffe8-110">Если клиент уже кэширует обработчик следующего прыжка, перейдите к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="dffe8-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="dffe8-111">Создайте структуру [**\_ \_ сведений о NEXTHOP в RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) и заполните ее соответствующей информацией.</span><span class="sxs-lookup"><span data-stu-id="dffe8-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="dffe8-112">Добавьте следующий прыжок в таблицу маршрутизации, вызвав [**ртмадднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="dffe8-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="dffe8-113">Диспетчер таблиц маршрутизации возвращает маркер следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="dffe8-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="dffe8-114">Если следующий прыжок уже существует, таблица маршрутизации не добавляет следующий прыжок; Вместо этого он возвращает маркер следующему прыжку.</span><span class="sxs-lookup"><span data-stu-id="dffe8-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="dffe8-115">Создайте структуру [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) и заполните ее соответствующей информацией, включая маркер следующего прыжка, возвращенный диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dffe8-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="dffe8-116">Добавьте маршрут в таблицу маршрутизации, вызвав [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span><span class="sxs-lookup"><span data-stu-id="dffe8-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="dffe8-117">Диспетчер таблиц маршрутизации сравнивает новый маршрут с маршрутами, которые уже находятся в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dffe8-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="dffe8-118">Два маршрута равны, если выполняются все перечисленные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="dffe8-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="dffe8-119">Маршрут добавляется в то же место назначения.</span><span class="sxs-lookup"><span data-stu-id="dffe8-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="dffe8-120">Маршрут добавляется тем же клиентом, который указан членом **owner** структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="dffe8-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="dffe8-121">Маршрут объявляется тем же соседом, который указан в **соседнем** элементе структуры [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="dffe8-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="dffe8-122">Если маршрут существует, диспетчер таблиц маршрутизации возвращает маркер существующего маршрута.</span><span class="sxs-lookup"><span data-stu-id="dffe8-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="dffe8-123">В противном случае диспетчер таблиц маршрутизации добавляет маршрут и возвращает его в новый маршрут.</span><span class="sxs-lookup"><span data-stu-id="dffe8-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="dffe8-124">Клиент может присвоить параметру *Change \_ flags* значение RTM \_ \_ Change маршрута \_ New, чтобы диспетчер таблиц маршрутизации мог добавить новый маршрут в место назначения, даже если существует другой маршрут с теми же полями владельца и соседей.</span><span class="sxs-lookup"><span data-stu-id="dffe8-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="dffe8-125">Клиент может присвоить параметру *Change \_ flags* значение RTM Change, чтобы \_ \_ \_ сообщить диспетчеру таблиц маршрутизации, что необходимо обновить первый маршрут в месте назначения, принадлежащем клиенту.</span><span class="sxs-lookup"><span data-stu-id="dffe8-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="dffe8-126">Это обновление можно выполнить, если такой маршрут существует, даже если поле соседа не совпадает.</span><span class="sxs-lookup"><span data-stu-id="dffe8-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="dffe8-127">Этот флаг используется клиентами, которые поддерживают один маршрут для каждого места назначения.</span><span class="sxs-lookup"><span data-stu-id="dffe8-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="dffe8-128">**Чтобы обновить маршрут, клиент должен выполнить следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="dffe8-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="dffe8-129">Вызовите [**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) с помощью маркера маршрута.</span><span class="sxs-lookup"><span data-stu-id="dffe8-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="dffe8-130">Этот обработчик был либо ранее кэшированным клиентом, либо возвращенный диспетчером таблиц маршрутизации из вызова, возвращающего маркер маршрута, такой как **ртмжетраутеинфо**.</span><span class="sxs-lookup"><span data-stu-id="dffe8-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="dffe8-131">Внесите изменения в структуру [**\_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) , которая возвращается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dffe8-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="dffe8-132">Вызовите [**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) с помощью маркера маршрута и измененной [**структуры \_ \_ сведений о маршруте RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="dffe8-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="dffe8-133">В следующем примере кода показано, как добавить маршрут к назначению с помощью диспетчера таблиц маршрутизации в качестве посредника.</span><span class="sxs-lookup"><span data-stu-id="dffe8-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


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



 

 




