---
title: Ноябрь (Монсстипе), элемент
description: Указывает, что задача выполняется в ноябре.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Ноябрьский элемент планировщик задач
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 170fa1cef23fb992b651ab4675fb3f782df10a347fcff52c865b7774039cac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758410"
---
# <a name="november-monthstype-element"></a>Ноябрь (Монсстипе), элемент

Указывает, что задача выполняется в ноябре.

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

Элемент **Ноябрь** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                          | Унаследован от                                                     | Описание                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Месяцы (Монслидайофвиксчедулетипе)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.<br/> |
| [**Месяцы (Монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.<br/>             |



## <a name="examples"></a>Примеры

Следующий XML-код определяет календарь месяцев, который запускает задачу в ноябре.


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





