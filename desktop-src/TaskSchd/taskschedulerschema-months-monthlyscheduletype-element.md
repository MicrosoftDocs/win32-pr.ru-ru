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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137026"
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



## <a name="remarks"></a>Комментарии

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

 

 





