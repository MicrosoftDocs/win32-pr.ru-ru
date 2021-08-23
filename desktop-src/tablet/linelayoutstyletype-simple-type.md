---
description: Определяет допустимые значения для атрибута Style элемента Линелайаут.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Простой тип Линелайаутстилетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031842"
---
# <a name="linelayoutstyletype-simple-type"></a>Простой тип Линелайаутстилетипе

Определяет допустимые значения для атрибута **Style** [элемента линелайаут](linelayout-element.md).

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **линелайаутстилетипе** — это строка, которая ограничена следующим шаблоном:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Remarks

Допустимые значения атрибута **Style** [элемента линелайаут](linelayout-element.md) :

-   Нет
-   Сплошная
-   Штрих
-   Точки
-   DashDot
-   DashDotDot
-   Тип Double

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




