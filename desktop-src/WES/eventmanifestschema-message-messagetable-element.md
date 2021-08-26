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
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865674"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Родительские элементы**
</dt> <dt>

[**Мессажетабле (Евентстипе)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**Мессажетабле (Метадататипе)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





