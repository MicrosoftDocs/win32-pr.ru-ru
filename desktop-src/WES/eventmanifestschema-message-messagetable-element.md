---
title: Элемент Message (Мессажетабле)
description: Содержит ссылку на строку в разделе локализации манифеста. | Элемент Message (Мессажетабле)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Журнал событий элемента сообщения
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693961"
---
# <a name="message-messagetable-element"></a>Элемент Message (Мессажетабле)

Содержит ссылку на строку в разделе локализации манифеста.

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **Message** определяется элементом [**мессажетабле**](eventmanifestschema-messagetable-instrumentationtype-element.md) .

## <a name="attributes"></a>Атрибуты



| Имя    | Тип   | Описание                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | строка | Ссылка на локализованную строку в таблице строк.<br/>                                |
| mid     | строка | Не используется.<br/>                                                                               |
| символ  | строка | Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.<br/> |
| value   | строка | Число, используемое в качестве идентификатора сообщения для данного сообщения.<br/>                           |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительские элементы**
</dt> <dt>

[**Мессажетабле (Евентстипе)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**Мессажетабле (Метадататипе)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





