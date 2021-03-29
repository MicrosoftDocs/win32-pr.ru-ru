---
title: Функция named_type_free_local
description: Заглушки вызывают \_ свободную \_ локальную функцию типа, чтобы освободить память, выделенную вызовом именованного \_ типа, \_ в \_ локальную подпрограммы.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774624"
---
# <a name="the-named_type_free_local-function"></a>Локальная функция с именованным \_ типом \_ Free \_

Заглушки вызывают **\_ свободную \_ локальную функцию типа** , чтобы освободить память, выделенную вызовом [именованного \_ типа, \_ в \_ локальную](the-named-type-to-local-function.md) подпрограммы. Память, выделенная заглушкой, не освобождается. Прототип функции определяется следующим образом:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Параметр является указателем на память, выделенную с помощью **именованного \_ типа, \_ в \_ локальную**.

 

 




