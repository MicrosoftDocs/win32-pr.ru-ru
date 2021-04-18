---
title: Сложный тип DataType (журнал событий Windows)
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
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341055"
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



## <a name="remarks"></a>Комментарии

Элемент данных может быть элементом данных верхнего уровня или элементом данных в структуре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





