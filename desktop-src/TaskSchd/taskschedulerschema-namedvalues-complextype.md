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
ms.openlocfilehash: 9d54e7c33d0b7ab2e5be3c4de6f3f648398a7e65670c0379f5621ae9e8a8bd46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513940"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





