---
title: Перечисление всех маршрутов
description: Следующая процедура описывает шаги, используемые для перечисления всех сущностей, используемых API RTMv2. В приведенном ниже образце кода показано, как перечислить все маршруты.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776877"
---
# <a name="enumerate-all-routes"></a><span data-ttu-id="fd4a5-104">Перечисление всех маршрутов</span><span class="sxs-lookup"><span data-stu-id="fd4a5-104">Enumerate All Routes</span></span>

<span data-ttu-id="fd4a5-105">Следующая процедура описывает шаги, используемые для перечисления всех сущностей, используемых API RTMv2.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="fd4a5-106">В приведенном ниже образце кода показано, как перечислить все маршруты.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="fd4a5-107">**Базовый процесс для каждого перечисления выглядит следующим образом.**</span><span class="sxs-lookup"><span data-stu-id="fd4a5-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="fd4a5-108">Запустите перечисление, получая маркер из диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="fd4a5-109">Вызовите [**ртмкреатедестенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**ртмкреатераутинум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) и [**ртмкреатенекссопенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) , чтобы указать критерии, указывающие тип данных для перечисления.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="fd4a5-110">Этот критерий включает, но не ограничивается диапазоном назначений, определенным интерфейсом и представлениями, в которых находятся эти сведения.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="fd4a5-111">Вызовите [**ртмжетенумдестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**ртмжетенумраутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) и [**ртмжетенумнекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) один или несколько раз, чтобы получить данные, пока диспетчер таблиц маршрутизации не вернет ошибку больше \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="fd4a5-112">Данные маршрута, назначения и следующего прыжка возвращаются в порядке получения сведений об адресе (а также значения предпочтений и метрик, если перечисляются маршруты).</span><span class="sxs-lookup"><span data-stu-id="fd4a5-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="fd4a5-113">Вызывайте [**ртмрелеаседестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**ртмрелеасераутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) и [**ртмрелеасенекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , когда дескрипторы или информационные структуры, связанные с перечислением, больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="fd4a5-114">Вызовите [**ртмделетинумхандле**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) , чтобы освободить маркер перечисления, который был возвращен при создании перечисления.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="fd4a5-115">Эта функция используется для освобождения обработчика для всех типов перечислений.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="fd4a5-116">Маршруты, наявляющиеся в состоянии удержания, перечисляются только тогда, когда клиент запрашивает данные из всех представлений, использующих параметр RTM- \_ \_ Маска представления \_ ANY.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="fd4a5-117">В следующем примере кода показано, как перечислить все маршруты в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fd4a5-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




