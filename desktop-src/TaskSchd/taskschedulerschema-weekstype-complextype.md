---
title: Сложный тип Викстипе
description: Определяет дочерний элемент и сведения о последовательности для элемента Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- планировщик задач сложного типа Викстипе
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137011"
---
# <a name="weekstype-complex-type"></a>Сложный тип Викстипе

Определяет дочерний элемент и сведения о последовательности для элемента [**Week**](taskschedulerschema-week-weekstype-element.md) .

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                    | Тип                                                        | Описание                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Неделя**](taskschedulerschema-week-weekstype-element.md) | [**виктипе**](taskschedulerschema-weektype-simpletype.md) | Указывает неделю, в которой выполняется задача.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





