---
title: Функция type_free_inst
description: Заглушки вызывают \_ функцию Free inst типа, \_ чтобы освободить память, связанную с представленным типом.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923713"
---
# <a name="the-type_free_inst-function"></a>Функция типа \_ Free \_ inst

Заглушки вызывают функцию **\_ Free \_ inst типа** , чтобы освободить память, связанную с представленным типом. Функция определяется следующим образом:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Параметр указывает на представленный экземпляр типа. Этот объект не должен освобождаться. Обсуждение того, когда следует вызывать функцию, см. [в описании \_ атрибута «передать как](the-transmit-as-attribute.md)».

В следующем примере список с двойным связыванием освобождается путем прохода по списку к его концу, а затем создается резервная копия и освобождается каждый элемент списка.


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



 

 




