---
title: Дайсинтервал (Даилисчедулетипе), элемент
description: Указывает интервал между днями в расписании.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- планировщик задач элемента Дайсинтервал
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988298"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Дайсинтервал (Даилисчедулетипе), элемент

Указывает интервал между днями в расписании.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент определяется сложным типом [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                | Унаследован от                                                                   | Описание                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md) | Указывает ежедневное расписание.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки скриптов интервал дней для ежедневного триггера указывается свойством [**даилитригжер. дайсинтервал**](dailytrigger-daysinterval.md) .

Для разработки на C++ интервал дней для ежедневного триггера задается свойством [**идаилитригжер::D айсинтервал**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу каждый день.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Полный пример кода XML для задачи, в котором указано ежедневное расписание, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).

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

 

 





