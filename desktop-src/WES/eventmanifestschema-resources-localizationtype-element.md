---
title: Resources (Локализатионтипе), элемент
description: Определяет группу строковых таблиц, содержащих локализованные строки, на которые ссылается манифест.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Журнал событий элемента Resources
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120581"
---
# <a name="resources-localizationtype-element"></a>Resources (Локализатионтипе), элемент

Определяет группу строковых таблиц, содержащих локализованные строки, на которые ссылается манифест.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Элемент **Resources** определяется сложным типом [**локализатионтипе**](eventmanifestschema-localizationtype-complextype.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                  | Тип                                                                       | Описание                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**stringTable**](eventmanifestschema-stringtable-resources-element.md) | [**стрингтаблетипе**](eventmanifestschema-stringtabletype-complextype.md) | Определяет список локализованных строк, на которые можно ссылаться в манифесте.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип   | Описание                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | строка | Имя языка, определяющее язык и региональные параметры локализованных строк в таблице строк. Например, "en-US" для английского языка (США).<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Локализация (Инструментатионманифест)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





