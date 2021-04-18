---
title: Сложный тип Типелисттипе
description: Определяет типы, используемые в манифесте.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Журнал событий сложных типов Типелисттипе
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691899"
---
# <a name="typelisttype-complex-type"></a>Сложный тип Типелисттипе

Определяет типы, используемые в манифесте.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип                                                                           | Описание                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**нетипизированные типы**](eventmanifestschema-intypes-typelisttype-element.md)   | [**инпуттипелисттипе**](eventmanifestschema-inputtypelisttype-complextype.md) | Определяет список входных типов данных.<br/>                                                              |
| [**ксмлтипес**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**ксмлтипелисттипе**](eventmanifestschema-xmltypelisttype-complextype.md)     | Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





