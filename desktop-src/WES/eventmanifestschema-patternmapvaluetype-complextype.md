---
title: Сложный тип Паттернмапвалуетипе
description: Не используется. Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Журнал событий сложных типов Паттернмапвалуетипе
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136167"
---
# <a name="patternmapvaluetype-complex-type"></a>Сложный тип Паттернмапвалуетипе

Не используется. Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя  | Тип   | Описание                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | строка | Регулярное выражение, используемое для поиска соответствующей строки в строке сообщения.<br/>                   |
| value | строка | Регулярное выражение, используемое для изменения соответствующей строки, найденной в строке сообщения.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





