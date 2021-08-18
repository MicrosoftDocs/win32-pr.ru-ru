---
title: Функция named_type_free_local
description: Заглушки вызывают \_ свободную \_ локальную функцию типа, чтобы освободить память, выделенную вызовом именованного \_ типа, \_ в \_ локальную подпрограммы.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924084"
---
# <a name="the-named_type_free_local-function"></a>Локальная функция с именованным \_ типом \_ Free \_

Заглушки вызывают **\_ свободную \_ локальную функцию типа** , чтобы освободить память, выделенную вызовом [именованного \_ типа, \_ в \_ локальную](the-named-type-to-local-function.md) подпрограммы. Память, выделенная заглушкой, не освобождается. Прототип функции определяется следующим образом:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Параметр является указателем на память, выделенную с помощью **именованного \_ типа, \_ в \_ локальную**.

 

 




