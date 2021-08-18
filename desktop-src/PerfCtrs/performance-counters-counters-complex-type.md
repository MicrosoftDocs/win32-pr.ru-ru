---
description: Определяет раздел манифеста инструментирования, который определяет поставщик и счетчики, которые они предоставляют.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Сложный тип счетчиков
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143967"
---
# <a name="counters-complex-type"></a>Сложный тип счетчиков

Определяет раздел манифеста инструментирования, который определяет поставщик и счетчики, которые они предоставляют.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент      | Тип                                                               | Описание                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **поставщики** | [**мужчина: поставщик**](performance-counters-provider-complex-type.md) | Определяет поставщик, предоставляющий счетчики.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя          | Тип | Описание                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Версия схемы, используемой для записи манифеста.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инструментирования**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

