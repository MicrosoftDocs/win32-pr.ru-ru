---
title: Перечисления (одноранговая инфраструктура)
description: С помощью перечислений можно получить список всех конкретных одноранговых сущностей, соответствующих Вашим критериям.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514866001734fb0ba0d73c94d5d4d8f8b4cfc6987d121f058a6bfcb00f792c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887634"
---
# <a name="enumerations-peer-infrastructure"></a>Перечисления (одноранговая инфраструктура)

С помощью перечислений можно получить список всех конкретных одноранговых сущностей, соответствующих Вашим критериям.

**Получение перечисления и получение результатов**

1.  Получите маркер перечисления. Вызовите функцию **пиренум** , например, вызовите функцию одноранговых диаграмм [**пирграфенумрекордс**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) . Функции **пиренум** создают перечисление и возвращают в вызывающее приложение маркер этого перечисления. Этот обработчик необходимо использовать для получения результатов.
2.  При необходимости получите количество сущностей в перечислении. Вызовите функцию **GetItemCount** , например Call [**пирграфжетитемкаунт**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) или [**пиржетитемкаунт**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).
    > [!Note]  
    > Можно использовать значение, возвращаемое функцией **GetItemCount** , чтобы определить количество элементов, доступных для извлечения.

     

3.  Получение группы результатов. Вызовите функцию **жетнекститем** , например, вызовите [**пирграфжетнекститем**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Когда приложение вызывает функцию **жетнекститем** , оно указывает количество возвращаемых сущностей, а затем функция возвращает указатель на массив указателей на сущности и количество сущностей, которые всегда меньше или равны указанному числу. Приложению может потребоваться несколько раз вызывать эту функцию, пока количество возвращаемых сущностей не станет меньше запрошенного числа.

     

4.  После того как данные не понадобятся, освободите указатель на данные. Вызовите функцию **фридата** , например Call [**пирграффридата**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) или [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).
    > [!Note]  
    > Дополнительные сведения см. в разделе [освобождение данных однорангового узла](freeing-peer-data.md).

     

5.  После того как приложению не требуется обработчик для перечисления, освободите его. Вызовите функцию **EndEnumeration** , например Call [**пиренденумератион**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) или [**пирграфенденумератион**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Пример перечисления

В следующем фрагменте кода показано, как перечислить через доступные удостоверения.


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



