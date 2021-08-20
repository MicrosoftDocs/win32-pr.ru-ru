---
title: Мессажетабле (Евентстипе), элемент
description: Содержит ссылку на строку в разделе локализации манифеста. | Мессажетабле (Евентстипе), элемент
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- Журнал событий элемента Мессажетабле
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5a2bcf374e336047deaa1339ac749fde3fa7c4f27b38e046f6c9bc651c0e0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120893"
---
# <a name="messagetable-eventstype-element"></a>Мессажетабле (Евентстипе), элемент

Содержит ссылку на строку в разделе локализации манифеста.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **мессажетабле** определяется сложным типом [**евентстипе**](eventmanifestschema-eventstype-complextype.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Тип | Описание                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | Задает ссылку на строку в разделе локализации манифеста.<br/> |



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

[**Элемент Events (Инструментатионтипе)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





