---
title: Сложный тип Намедвалуе
description: Определяет имя, связанное со значением в паре "имя-значение".
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- планировщик задач сложного типа Намедвалуе
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0f92b89114dfedfbfdbc61d476aff99332191317c1f67b2163eb9416ef3a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080424"
---
# <a name="namedvalue-complex-type"></a>Сложный тип Намедвалуе

Определяет имя, связанное со значением в паре "имя-значение".

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя | Тип                                                                    | Описание                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Указывает имя, связанное со значением в паре «имя-значение». <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





