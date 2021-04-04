---
title: Синтаксис объекта (DN-Binary)
description: Строка октета, которая содержит двоичное значение и различающееся имя (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса объекта (DN-Binary)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104137914"
---
# <a name="objectdn-binary-syntax"></a>Синтаксис объекта (DN-Binary)

Строка октета, которая содержит двоичное значение и различающееся имя (DN).



| Ввод | Значение |
|--------------|------------------------------------------------------------------------------------|
| Имя         | Object(двоичный_DN)                                                                  |
| Идентификатор синтаксиса    | 2.5.5.7                                                                            |
| ИДЕНТИФИКАТОР OM        | 127                                                                                |
| Тип MAPI    | тстринг                                                                            |
| Тип ADS     | АДСТИПЕ \_ DN \_ с \_ двоичными данными                                                          |
| Тип варианта | \_Диспетчер VT                                                                       |
| Тип SDS     | COM-объект, который можно привести к [**иадсднвисбинари**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Комментарии

Значение с этим синтаксисом имеет следующий формат:

``` syntax
B:<char count>:<binary value>:<object DN>
```

где " &lt; число символов &gt; " — это число шестнадцатеричных цифр в " &lt; двоичное значение" &gt; , " &lt; двоичное значение &gt; " — шестнадцатеричное представление двоичного значения, а " &lt; объект DN &gt; " — различающееся имя. Active Directory автоматически обновляет DN, если объект, на который он ссылается, перемещается или переименовывается. Дополнительные сведения и пример кода, в котором используется этот синтаксис, см. в разделе [Включение безопасного переименования с помощью свойства otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
