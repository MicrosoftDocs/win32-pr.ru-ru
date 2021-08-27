---
title: Использование списка маршрутов Client-Specific
description: В следующих процедурах описаны действия по использованию списков маршрутов, зависящих от клиента. В приведенном ниже образце кода показано, как реализовать процедуру.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca4b1036115c49c2045121d16f09c55a3fa611153a9b1337a0437c9e2196800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025304"
---
# <a name="use-a-client-specific-route-list"></a>Использование списка маршрутов Client-Specific

В следующих процедурах описаны действия по использованию списков маршрутов, зависящих от клиента. В приведенном ниже образце кода показано, как реализовать процедуру.

**Чтобы использовать эту функцию, клиент должен выполнить следующие действия.**

1.  Вызовите [**ртмкреатераутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) , чтобы получить маркер диспетчера таблиц маршрутизации.
2.  Вызывайте [**ртминсертинраутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) , когда клиент должен добавить маршрут к этому списку.
3.  Если клиенту больше не требуется этот список, он должен вызвать [**ртмделетераутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) для удаления списка.

**Если клиент должен перечислить маршруты в списке, клиент должен выполнить следующие действия.**

1.  Вызовите [**ртмкреатераутелистенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) , чтобы получить маркер перечисления из диспетчера таблиц маршрутизации.
2.  Вызовите [**ртмжетлистенумраутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) , чтобы получить дескрипторы маршрутов в списке.
3.  Вызовите [**ртмрелеасераутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) , чтобы освободить дескрипторы, когда они больше не требуются.

В следующем примере кода показано, как создать и использовать список маршрутов для конкретного клиента.


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




