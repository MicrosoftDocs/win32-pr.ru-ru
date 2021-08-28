---
title: сложный тип DataType (Windows журнал событий)
description: Определяет элемент данных.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Журнал событий сложного типа DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620284"
---
# <a name="datatype-complex-type"></a>Сложный тип DataType

Определяет элемент данных.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Название | строка | Имя элемента данных, определенного в шаблоне (см. сложный тип [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |
| Тип | QName  | Не используется.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Remarks

Элемент данных может быть элементом данных верхнего уровня или элементом данных в структуре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





