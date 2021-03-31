---
title: Апрель (Монсстипе), элемент
description: Указывает, что задача выполняется в апреле.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Элемент April планировщик задач
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137370"
---
# <a name="april-monthstype-element"></a>Апрель (Монсстипе), элемент

Указывает, что задача выполняется в апреле.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

Элемент **April** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                          | Унаследован от                                                     | Описание                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Месяцы (Монслидайофвиксчедулетипе)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.<br/>             |
| [**Месяцы (Монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**монсстипе**](taskschedulerschema-monthstype-complextype.md) | Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.<br/> |



## <a name="examples"></a>Примеры

Следующий XML-код определяет календарь месяцев, в котором выполняется задача в апреле.


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





