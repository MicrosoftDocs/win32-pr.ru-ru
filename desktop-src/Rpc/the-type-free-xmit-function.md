---
title: Функция type_free_xmit
description: Заглушки вызывают \_ \_ функцию Free xmit типа, чтобы освободить память, связанную с переданными данными.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253351"
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

 

 




