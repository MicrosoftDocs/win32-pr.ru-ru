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
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758210"
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



## <a name="remarks"></a>Remarks

При указании недель месяца используйте числа 1-4 в течение первых четырех недель месяца или используйте строку Last, чтобы указать последнюю неделю месяца.

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

 

 





