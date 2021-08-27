---
title: Перечисление всех маршрутов
description: Следующая процедура описывает шаги, используемые для перечисления всех сущностей, используемых API RTMv2. В приведенном ниже образце кода показано, как перечислить все маршруты.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f8707c7cf78f274fedaca3fb4882ae36dbd569ab5fa1260ec3b6cb663aced3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101854"
---
# <a name="enumerate-all-routes"></a>Перечисление всех маршрутов

Следующая процедура описывает шаги, используемые для перечисления всех сущностей, используемых API RTMv2. В приведенном ниже образце кода показано, как перечислить все маршруты.

**Базовый процесс для каждого перечисления выглядит следующим образом.**

1.  Запустите перечисление, получая маркер из диспетчера таблиц маршрутизации. Вызовите [**ртмкреатедестенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**ртмкреатераутинум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) и [**ртмкреатенекссопенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) , чтобы указать критерии, указывающие тип данных для перечисления. Этот критерий включает, но не ограничивается диапазоном назначений, определенным интерфейсом и представлениями, в которых находятся эти сведения.
2.  Вызовите [**ртмжетенумдестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**ртмжетенумраутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) и [**ртмжетенумнекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) один или несколько раз, чтобы получить данные, пока диспетчер таблиц маршрутизации не вернет ошибку больше \_ \_ \_ элементов. Данные маршрута, назначения и следующего прыжка возвращаются в порядке получения сведений об адресе (а также значения предпочтений и метрик, если перечисляются маршруты).
3.  Вызывайте [**ртмрелеаседестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**ртмрелеасераутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) и [**ртмрелеасенекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , когда дескрипторы или информационные структуры, связанные с перечислением, больше не требуются.
4.  Вызовите [**ртмделетинумхандле**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) , чтобы освободить маркер перечисления, который был возвращен при создании перечисления. Эта функция используется для освобождения обработчика для всех типов перечислений.

> [!Note]  
> Маршруты, наявляющиеся в состоянии удержания, перечисляются только тогда, когда клиент запрашивает данные из всех представлений, использующих параметр RTM- \_ \_ Маска представления \_ ANY.

 

В следующем примере кода показано, как перечислить все маршруты в таблице маршрутизации.


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



 

 




