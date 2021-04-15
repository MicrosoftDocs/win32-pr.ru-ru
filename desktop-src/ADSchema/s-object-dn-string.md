---
title: Синтаксис объекта (DN-String)
description: Строка октета, которая содержит строковое значение и различающееся имя.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса объекта (DN-строки)
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654777"
---
# <a name="objectdn-string-syntax"></a>Синтаксис объекта (DN-String)

Строка октета, которая содержит строковое значение и различающееся имя.



| Ввод | Значение |
|--------------|------------------------------------------------------------------------------------|
| Имя         | Object(строка_DN)                                                                  |
| Идентификатор синтаксиса    | 2.5.5.14                                                                           |
| ИДЕНТИФИКАТОР OM        | 127                                                                                |
| Тип MAPI    | \-                                                                                 |
| Тип ADS     | АДСТИПЕ \_ DN \_ со \_ строкой                                                          |
| Тип варианта | \_Диспетчер VT                                                                       |
| Тип SDS     | COM-объект, который можно привести к [**иадсднвисстринг**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Комментарии

Значение с этим синтаксисом имеет следующий формат:

``` syntax
S:<char count>:<string value>:<object DN>
```

где " &lt; число &gt; символов" — это число знаков в &lt; строке "строковое значение" &gt; , а " &lt; Object DN &gt; " — это различающееся имя объекта в Active Directory. Active Directory обновляет DN, если объект, на который он ссылается, перемещается или переименовывается.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
