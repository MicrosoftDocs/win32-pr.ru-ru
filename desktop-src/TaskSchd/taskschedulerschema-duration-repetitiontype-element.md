---
title: Duration (Репетитионтипе), элемент
description: Указывает, как долго шаблон повторяется.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Элемент Duration планировщик задач
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341325"
---
# <a name="duration-repetitiontype-element"></a>Duration (Репетитионтипе), элемент

Указывает, как долго шаблон повторяется. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> . Если для длительности не указано значение, шаблон повторяется бесконечно. Минимальное значение — одна минута.

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                      | Унаследован от                                                             | Описание                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Повторение**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/> |



## <a name="remarks"></a>Комментарии

Для приложений со скриптами длительность шаблона указывается с помощью свойства [**репетитионпаттерн. Duration**](repetitionpattern-duration.md) .

Для приложений C++ длительность шаблона указывается с помощью свойства [**ирепетитионпаттерн::D фигурации**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет шаблон повторения для триггера.


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
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

 

 





