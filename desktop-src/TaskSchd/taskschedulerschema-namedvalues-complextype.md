---
title: Сложный тип Намедвалуес
description: Определяет пару "имя-значение", в которой имя связано со значением.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- планировщик задач сложного типа Намедвалуес
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802771"
---
# <a name="namedvalues-complex-type"></a>Сложный тип Намедвалуес

Определяет пару "имя-значение", в которой имя связано со значением.

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                        | Тип                                                | Описание                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Значение**](taskschedulerschema-value-namedvalues-element.md) | [**намедвалуе**](schema-namedvalue-complextype.md) | Указывает значение, связанное с именем в паре «имя-значение».<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





