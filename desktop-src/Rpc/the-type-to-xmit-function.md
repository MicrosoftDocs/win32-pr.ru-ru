---
title: Функция type_to_xmit
description: Заглушки вызывают тип \_ \_ функции xmit для преобразования типа, представленного приложением, в передаваемый тип.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986694"
---
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="09e87-104">Тип \_ для \_ функции xmit</span><span class="sxs-lookup"><span data-stu-id="09e87-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="09e87-105">Заглушки вызывают **тип функции \_ \_ xmit** для преобразования типа, представленного приложением, в передаваемый тип.</span><span class="sxs-lookup"><span data-stu-id="09e87-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="09e87-106">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09e87-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="09e87-107">Первый параметр — это указатель на данные приложения.</span><span class="sxs-lookup"><span data-stu-id="09e87-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="09e87-108">Второй параметр задается функцией для указания передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="09e87-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="09e87-109">Функция должна выделить память для переданного типа.</span><span class="sxs-lookup"><span data-stu-id="09e87-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="09e87-110">В следующем примере клиент вызывает удаленную процедуру с **\[ входным \]** параметром in типа Double \_ Link \_ Type.</span><span class="sxs-lookup"><span data-stu-id="09e87-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="09e87-111">Клиентская заглушка вызывает **тип \_ функции \_ XMIT** с именем Double \_ Link \_ Type \_ to \_ xmit, чтобы преобразовать данные списка с двойным связыванием в массив размеров.</span><span class="sxs-lookup"><span data-stu-id="09e87-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="09e87-112">Функция определяет количество элементов в списке, выделяет массив, достаточно большой для хранения этих элементов, а затем копирует элементы списка в массив.</span><span class="sxs-lookup"><span data-stu-id="09e87-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="09e87-113">Перед возвратом функции второй параметр, *ппаррай*, устанавливается в значение, указывающий на только что выделенную структуру данных.</span><span class="sxs-lookup"><span data-stu-id="09e87-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




