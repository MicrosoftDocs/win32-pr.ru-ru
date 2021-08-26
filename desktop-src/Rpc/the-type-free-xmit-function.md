---
title: Функция type_free_xmit
description: Заглушки вызывают \_ \_ функцию Free xmit типа, чтобы освободить память, связанную с переданными данными.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016584"
---
# <a name="the-type_free_xmit-function"></a>Функция типа \_ Free \_ xmit

Заглушки вызывают функцию **\_ Free \_ xmit типа** , чтобы освободить память, связанную с переданными данными. После того как [тип \_ из функции \_ xmit](the-type-from-xmit-function.md) преобразует передаваемые данные в представленный тип, память больше не нужна. Функция определяется следующим образом:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Параметр является указателем на память, содержащую переданный тип.

В этом примере память содержит массив, который находится в одной структуре. Функция двойной \_ связи \_ типа Double \_ \_ xmit использует предоставляемую пользователем функцию MIDL \_ \_ Free для освобождения памяти:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




