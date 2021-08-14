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
ms.openlocfilehash: 876d798acdf1f8684fc4f2cecac8e77bceb73dddd0036f2117d4bb55a77a71ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757991"
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
| [**Дней**](taskschedulerschema-week-weekstype-element.md) | [**виктипе**](taskschedulerschema-weektype-simpletype.md) | Указывает неделю, в которой выполняется задача.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





