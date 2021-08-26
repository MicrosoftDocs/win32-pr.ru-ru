---
title: Элемент Октябрь (Монсстипе)
description: Указывает, что задача выполняется в октябре.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- планировщик задач элемента Октябрь
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65f14f0ccaa2831bc4aae24ce45a520f746a57b2e9d03d70b64714bafa69e25b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125734"
---
# <a name="october-monthstype-element"></a>Элемент Октябрь (Монсстипе)

Указывает, что задача выполняется в октябре.

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

Элемент **Октябрь** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                          | Унаследован от                                                     | Описание                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Месяцы (Монслидайофвиксчедулетипе)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.<br/> |
| [**Месяцы (Монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.<br/>             |



## <a name="examples"></a>Примеры

Следующий XML-код определяет календарь месяцев, в котором выполняется задача в октябре.


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





