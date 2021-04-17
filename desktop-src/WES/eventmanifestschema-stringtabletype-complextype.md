---
title: Сложный тип Стрингтаблетипе
description: Определяет список локализованных строк, на которые можно ссылаться в манифесте. | Сложный тип Стрингтаблетипе
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Журнал событий сложных типов Стрингтаблетипе
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694017"
---
# <a name="stringtabletype-complex-type"></a>Сложный тип Стрингтаблетипе

Определяет список локализованных строк, на которые можно ссылаться в манифесте.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип | Описание                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**Строка**](eventmanifestschema-string-stringtabletype-element.md) |      | Определяет локализованную строку.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя       | Тип   | Описание                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| идентификатор         | строка | Идентификатор, однозначно определяющий строку в таблице строк. Например, «Printer. Connection».<br/> |
| стрингтипе | строка | Не используется.<br/>                                                                                                     |
| value      | строка | Локализованная строка.<br/>                                                                                         |



## <a name="remarks"></a>Комментарии

Можно ссылаться на строки из любого типа манифеста, содержащего атрибут Message. Чтобы сослаться на строку с Стрингтипе строки и идентификатором "Printer. Connection", используйте $ (String. Printer. Connection) в качестве значения атрибута Message.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





