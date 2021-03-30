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
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800947"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





