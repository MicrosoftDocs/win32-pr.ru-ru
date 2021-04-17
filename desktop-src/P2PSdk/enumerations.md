---
title: Перечисления (одноранговая инфраструктура)
description: С помощью перечислений можно получить список всех конкретных одноранговых сущностей, соответствующих Вашим критериям.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663346"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="1a323-103">Перечисления (одноранговая инфраструктура)</span><span class="sxs-lookup"><span data-stu-id="1a323-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="1a323-104">С помощью перечислений можно получить список всех конкретных одноранговых сущностей, соответствующих Вашим критериям.</span><span class="sxs-lookup"><span data-stu-id="1a323-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="1a323-105">**Получение перечисления и получение результатов**</span><span class="sxs-lookup"><span data-stu-id="1a323-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="1a323-106">Получите маркер перечисления.</span><span class="sxs-lookup"><span data-stu-id="1a323-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="1a323-107">Вызовите функцию **пиренум** , например, вызовите функцию одноранговых диаграмм [**пирграфенумрекордс**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) .</span><span class="sxs-lookup"><span data-stu-id="1a323-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="1a323-108">Функции **пиренум** создают перечисление и возвращают в вызывающее приложение маркер этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="1a323-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="1a323-109">Этот обработчик необходимо использовать для получения результатов.</span><span class="sxs-lookup"><span data-stu-id="1a323-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="1a323-110">При необходимости получите количество сущностей в перечислении.</span><span class="sxs-lookup"><span data-stu-id="1a323-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="1a323-111">Вызовите функцию **GetItemCount** , например Call [**пирграфжетитемкаунт**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) или [**пиржетитемкаунт**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span><span class="sxs-lookup"><span data-stu-id="1a323-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a323-112">Можно использовать значение, возвращаемое функцией **GetItemCount** , чтобы определить количество элементов, доступных для извлечения.</span><span class="sxs-lookup"><span data-stu-id="1a323-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="1a323-113">Получение группы результатов.</span><span class="sxs-lookup"><span data-stu-id="1a323-113">Retrieve a group of results.</span></span> <span data-ttu-id="1a323-114">Вызовите функцию **жетнекститем** , например, вызовите [**пирграфжетнекститем**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span><span class="sxs-lookup"><span data-stu-id="1a323-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a323-115">Когда приложение вызывает функцию **жетнекститем** , оно указывает количество возвращаемых сущностей, а затем функция возвращает указатель на массив указателей на сущности и количество сущностей, которые всегда меньше или равны указанному числу.</span><span class="sxs-lookup"><span data-stu-id="1a323-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="1a323-116">Приложению может потребоваться несколько раз вызывать эту функцию, пока количество возвращаемых сущностей не станет меньше запрошенного числа.</span><span class="sxs-lookup"><span data-stu-id="1a323-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="1a323-117">После того как данные не понадобятся, освободите указатель на данные.</span><span class="sxs-lookup"><span data-stu-id="1a323-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="1a323-118">Вызовите функцию **фридата** , например Call [**пирграффридата**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) или [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="1a323-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a323-119">Дополнительные сведения см. в разделе [освобождение данных однорангового узла](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="1a323-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="1a323-120">После того как приложению не требуется обработчик для перечисления, освободите его.</span><span class="sxs-lookup"><span data-stu-id="1a323-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="1a323-121">Вызовите функцию **EndEnumeration** , например Call [**пиренденумератион**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) или [**пирграфенденумератион**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span><span class="sxs-lookup"><span data-stu-id="1a323-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="1a323-122">Пример перечисления</span><span class="sxs-lookup"><span data-stu-id="1a323-122">Example of an Enumeration</span></span>

<span data-ttu-id="1a323-123">В следующем фрагменте кода показано, как перечислить через доступные удостоверения.</span><span class="sxs-lookup"><span data-stu-id="1a323-123">The following code snippet shows you how to enumerate through available identities.</span></span>


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



 

 



