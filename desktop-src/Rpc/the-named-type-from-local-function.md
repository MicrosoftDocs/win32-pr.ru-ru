---
title: Функция named_type_from_local
description: Заглушки вызывают именованный \_ тип \_ из \_ локальной функции.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127624"
---
# <a name="the-named_type_from_local-function"></a>Именованный \_ тип \_ из \_ локальной функции

Заглушки вызывают именованный \_ тип \_ из \_ локальной функции. Он преобразует тип, используемый приложением, в тип, который будет передавать суррогаты по сети. Функция определяется следующим образом:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Первый параметр — это указатель на данные приложения. Второй параметр является указателем на указатель. Функция указывает на передаваемые данные. Функция должна выделить память для переданного типа.

 

 




