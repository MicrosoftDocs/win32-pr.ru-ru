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
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693662"
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

## <a name="remarks"></a>Комментарии

Допустимые значения атрибута **Style** [элемента линелайаут](linelayout-element.md) :

-   Нет
-   Сплошная
-   Штрих
-   Точки
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




