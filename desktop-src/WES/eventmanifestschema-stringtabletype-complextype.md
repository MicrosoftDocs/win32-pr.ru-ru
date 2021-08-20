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
ms.openlocfilehash: f5d52f19ca01a926c82fcc1e13cc7191866722ba5e0e6eef81e916e244744783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342988"
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



## <a name="remarks"></a>Remarks

Можно ссылаться на строки из любого типа манифеста, содержащего атрибут Message. Чтобы сослаться на строку с Стрингтипе строки и идентификатором "Printer. Connection", используйте $ (String. Printer. Connection) в качестве значения атрибута Message.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





