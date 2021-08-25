---
title: Мессажетабле (Метадататипе), элемент
description: Содержит ссылки на строки, используемые в разделе метаданных манифеста для инструментария событий. Строки хранятся в группе элементов сообщений и идентификаторов вместе.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: f7c614210a22bc6c6d160a7c161c5b5a89aab85116285822465b43ba75e63095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865664"
---
# <a name="messagetable-metadatatype-element"></a>Мессажетабле (Метадататипе), элемент

Содержит ссылки на строки, используемые в разделе метаданных манифеста для инструментария событий. Строки хранятся в группе элементов [**сообщений**](eventmanifestschema-message-messagetable-element.md) и идентификаторов вместе.

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

Элемент **мессажетабле** определяется сложным типом [**метадататипе**](eventmanifestschema-metadatatype-complextype.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Тип | Описание                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | Задает ссылку на строку в разделе локализации манифеста.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип   | Описание                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | строка | Ссылка на локализованную строку в таблице строк.<br/>      |
| mid     | строка | Не используется.<br/>                                                     |
| символ  | строка | Символ, используемый для ссылки на сообщение.<br/>                     |
| value   | строка | Число, используемое в качестве идентификатора сообщения для данного сообщения.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**метадататипе**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**метаданные (Инструментатионманифест)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





