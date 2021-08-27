---
title: Элемент Interval (Репетитионтипе)
description: Задает интервал времени между перезапусками задачи.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Элемент Interval планировщик задач
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec6f2724f4374ed94fff47e6577a2887ca953cae0af66de9c64971cd80aa2050
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100004"
---
# <a name="interval-repetitiontype-element"></a>Элемент Interval (Репетитионтипе)

Задает интервал времени между перезапусками задачи. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
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



## <a name="remarks"></a>Remarks

Для разработки сценариев интервал шаблона повторения указывается с помощью свойства [**репетитионпаттерн. Interval**](repetitionpattern-interval.md) .

Для разработки на C++ интервал создания шаблона повторения указывается с помощью свойства [**ирепетитионпаттерн:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, в которой используется интервал повторения, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).

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

 

 





