---
title: Week (Викстипе), элемент
description: Указывает конкретную неделю месяца.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Элемент Week планировщик задач
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682092"
---
# <a name="week-weekstype-element"></a>Week (Викстипе), элемент

Указывает конкретную неделю месяца.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

Элемент **Week** определяется сложным типом [**викстипе**](taskschedulerschema-weekstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                        | Унаследован от                                                   | Описание                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Weeks (Монслидайофвиксчедулетипе)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**викстипе**](taskschedulerschema-weekstype-complextype.md) | Указывает недели месяца, в которых выполняется задача.<br/> |



## <a name="remarks"></a>Комментарии

При указании недель месяца используйте числа 1-4 в течение первых четырех недель месяца или используйте строку Last, чтобы указать последнюю неделю месяца.

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

 

 





