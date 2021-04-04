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
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988951"
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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





