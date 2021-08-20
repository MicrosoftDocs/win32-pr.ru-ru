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
ms.openlocfilehash: e35df4f102801f7d52faeb384f9a1113e00abbf034026d19b5b7b6e7b4c90ed7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621104"
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



## <a name="remarks"></a>Remarks

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

 

 





