---
title: Функция named_type_from_local
description: Заглушки вызывают именованный \_ тип \_ из \_ локальной функции.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329123"
---
# <a name="the-named_type_from_local-function"></a>Именованный \_ тип \_ из \_ локальной функции

Заглушки вызывают именованный \_ тип \_ из \_ локальной функции. Он преобразует тип, используемый приложением, в тип, который будет передавать суррогаты по сети. Функция определяется следующим образом:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Первый параметр — это указатель на данные приложения. Второй параметр является указателем на указатель. Функция указывает на передаваемые данные. Функция должна выделить память для переданного типа.

 

 




