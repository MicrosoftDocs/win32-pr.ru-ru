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
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988420"
---
# <a name="interval-repetitiontype-element"></a>Элемент Interval (Репетитионтипе)

Задает интервал времени между перезапусками задачи. Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

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



## <a name="remarks"></a>Комментарии

Для разработки сценариев интервал шаблона повторения указывается с помощью свойства [**репетитионпаттерн. Interval**](repetitionpattern-interval.md) .

Для разработки на C++ интервал создания шаблона повторения указывается с помощью свойства [**ирепетитионпаттерн:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, в которой используется интервал повторения, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).

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

 

 





