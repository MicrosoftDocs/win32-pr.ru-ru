---
title: Функция type_to_xmit
description: Заглушки вызывают тип \_ \_ функции xmit для преобразования типа, представленного приложением, в передаваемый тип.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970d4a0de9675ac7a5f1b1c1449521177ecb661a1a80fd9ef609a6dc630605a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016504"
---
# <a name="the-type_to_xmit-function"></a>Тип \_ для \_ функции xmit

Заглушки вызывают **тип функции \_ \_ xmit** для преобразования типа, представленного приложением, в передаваемый тип. Функция определяется следующим образом:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

Первый параметр — это указатель на данные приложения. Второй параметр задается функцией для указания передаваемых данных. Функция должна выделить память для переданного типа.

В следующем примере клиент вызывает удаленную процедуру с **\[ входным \]** параметром in типа Double \_ Link \_ Type. Клиентская заглушка вызывает **тип \_ функции \_ XMIT** с именем Double \_ Link \_ Type \_ to \_ xmit, чтобы преобразовать данные списка с двойным связыванием в массив размеров.

Функция определяет количество элементов в списке, выделяет массив, достаточно большой для хранения этих элементов, а затем копирует элементы списка в массив. Перед возвратом функции второй параметр, *ппаррай*, устанавливается в значение, указывающий на только что выделенную структуру данных.


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



 

 




