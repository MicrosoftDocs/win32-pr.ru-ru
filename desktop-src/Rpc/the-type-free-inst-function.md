---
title: Функция type_free_inst
description: Заглушки вызывают \_ функцию Free inst типа, \_ чтобы освободить память, связанную с представленным типом.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888400"
---
# <a name="the-type_free_inst-function"></a><span data-ttu-id="62f9b-104">Функция типа \_ Free \_ inst</span><span class="sxs-lookup"><span data-stu-id="62f9b-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="62f9b-105">Заглушки вызывают функцию **\_ Free \_ inst типа** , чтобы освободить память, связанную с представленным типом.</span><span class="sxs-lookup"><span data-stu-id="62f9b-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="62f9b-106">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="62f9b-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="62f9b-107">Параметр указывает на представленный экземпляр типа.</span><span class="sxs-lookup"><span data-stu-id="62f9b-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="62f9b-108">Этот объект не должен освобождаться.</span><span class="sxs-lookup"><span data-stu-id="62f9b-108">This object should not be freed.</span></span> <span data-ttu-id="62f9b-109">Обсуждение того, когда следует вызывать функцию, см. [в описании \_ атрибута «передать как](the-transmit-as-attribute.md)».</span><span class="sxs-lookup"><span data-stu-id="62f9b-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="62f9b-110">В следующем примере список с двойным связыванием освобождается путем прохода по списку к его концу, а затем создается резервная копия и освобождается каждый элемент списка.</span><span class="sxs-lookup"><span data-stu-id="62f9b-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




