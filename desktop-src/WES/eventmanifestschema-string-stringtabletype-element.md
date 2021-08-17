---
title: String (Стрингтаблетипе), элемент
description: Определяет локализованную строку.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- Журнал событий элемента строки
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136177"
---
# <a name="string-stringtabletype-element"></a>String (Стрингтаблетипе), элемент

Определяет локализованную строку.

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

Элемент **строки** определяется сложным типом [**стрингтаблетипе**](eventmanifestschema-stringtabletype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя       | Тип   | Описание                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| идентификатор         | строка | Идентификатор, однозначно определяющий строку в таблице строк.<br/> |
| стрингтипе | строка | Не используется.<br/>                                                                  |
| value      | строка | Локализованная строка.<br/>                                                      |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**stringTable (Локализатионтипе)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





