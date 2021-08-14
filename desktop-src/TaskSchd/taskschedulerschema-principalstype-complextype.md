---
title: Сложный тип ПринЦипалстипе
description: Определяет дочерний элемент для Principal-элемента.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- планировщик задач сложного типа ПринЦипалстипе
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa2aecd8ea71769b51792fcc5bd26ceca11309f43697037964a900d45c0d8254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131745"
---
# <a name="principalstype-complex-type"></a>Сложный тип ПринЦипалстипе

Определяет дочерний элемент для [**Principal**](taskschedulerschema-principals-tasktype-element.md) -элемента.

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                  | Тип                                                                   | Описание                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Основной**](taskschedulerschema-principal-principaltype-element.md) | [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





