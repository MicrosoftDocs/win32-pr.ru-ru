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
ms.openlocfilehash: 18222343a5c10b7231d174021c8d4238ba075b66b648d99a704f4e1d1d651e2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580254"
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



## <a name="remarks"></a>Remarks

Значение с этим синтаксисом имеет следующий формат:

``` syntax
S:<char count>:<string value>:<object DN>
```

где " &lt; число &gt; символов" — это число знаков в &lt; строке "строковое значение" &gt; , а " &lt; Object DN &gt; " — это различающееся имя объекта в Active Directory. Active Directory обновляет DN, если объект, на который он ссылается, перемещается или переименовывается.

## <a name="see-also"></a>См. также

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
