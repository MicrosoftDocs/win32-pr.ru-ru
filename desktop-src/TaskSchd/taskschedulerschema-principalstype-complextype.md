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
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988292"
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
| [**Основного**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





