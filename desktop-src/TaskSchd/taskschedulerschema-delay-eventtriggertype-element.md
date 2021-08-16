---
title: Элемент Delay (Евенттригжертипе)
description: Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- планировщик задач элемента Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c9523b450d5f1ea86bdf09afba26604ebfe8055661fc18c439b4e30c97169d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357110"
---
# <a name="delay-eventtriggertype-element"></a>Элемент Delay (Евенттригжертипе)

Указывает промежуток времени между моментом возникновения события и моментом запуска задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Элемент **delay** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                       | Унаследован от                                                                 | Описание                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) | Указывает триггер, который запускает задачу при возникновении системного события.<br/> |



## <a name="remarks"></a>Remarks

Для разработки скриптов задержка триггера события задается свойством [**EventTrigger. Delay**](eventtrigger-delay.md) .

Для разработки на C++ задержка триггера события задается свойством [**иевенттригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .

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

 

 





