---
title: Months (Монслисчедулетипе), элемент
description: Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Элемент months планировщик задач
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b655b47fc3135006f8629246d63350d36a4b32e92398a00f40ae86fe3f70d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796504"
---
# <a name="months-monthlyscheduletype-element"></a>Months (Монслисчедулетипе), элемент

Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Элемент **months** определяется сложным типом [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                    | Унаследован от                                                                       | Описание                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**счедулебимонс**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) | Указывает ежемесячное расписание. <br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип | Описание                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Апрель (Монсстипе)**](taskschedulerschema-april-monthstype-element.md)         |      | Указывает, что задача выполняется в апреле.<br/>     |
| [**Август (Монсстипе)**](taskschedulerschema-august-monthstype-element.md)       |      | Указывает, что задача выполняется в августе.<br/>    |
| [**Декабрь (Монсстипе)**](taskschedulerschema-december-monthstype-element.md)   |      | Указывает, что задача выполняется в декабре.<br/>  |
| [**Февраль (Монсстипе)**](taskschedulerschema-february-monthstype-element.md)   |      | Указывает, что задача выполняется в феврале.<br/>  |
| [**Январь (Монсстипе)**](taskschedulerschema-january-monthstype-element.md)     |      | Указывает, что задача выполняется в январе.<br/>   |
| [**Июль (Монсстипе)**](taskschedulerschema-july-monthstype-element.md)           |      | Указывает, что задача выполняется в июле.<br/>      |
| [**Июнь (Монсстипе)**](taskschedulerschema-june-monthstype-element.md)           |      | Указывает, что задача выполняется в июне.<br/>      |
| [**Март (Монсстипе)**](taskschedulerschema-march-monthstype-element.md)         |      | Указывает, что задача выполняется в марте.<br/>     |
| [**Май (Монсстипе)**](taskschedulerschema-may-monthstype-element.md)             |      | Указывает, что задача выполняется в Май.<br/>       |
| [**Ноябрь (Монсстипе)**](taskschedulerschema-november-monthstype-element.md)   |      | Указывает, что задача выполняется в ноябре.<br/>  |
| [**Октябрь (Монсстипе)**](taskschedulerschema-october-monthstype-element.md)     |      | Указывает, что задача выполняется в октябре.<br/>   |
| [**Сентябрь (Монсстипе)**](taskschedulerschema-september-monthstype-element.md) |      | Указывает, что задача выполняется в сентябре.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев месяцы расписания задаются с помощью свойства [**монслитригжер. монссофеар**](monthlytrigger-monthsofyear.md) .

Для разработки на C++ месяцы расписания указываются с помощью свойства [**имонслитригжер:: монссофеар**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет месячный календарь, который запускает задачу в первый и 15-й день каждого месяца года.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a>Requirements (Требования)



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

 

 





