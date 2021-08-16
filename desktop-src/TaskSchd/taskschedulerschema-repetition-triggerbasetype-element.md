---
title: Элемент повторения (Тригжербасетипе)
description: Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Элемент повторения планировщик задач
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dfcce3e008a9959ca279f64c83a898eb2239d007d8fc32dfb5da5942395055bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959544"
---
# <a name="repetition-triggerbasetype-element"></a>Элемент повторения (Тригжербасетипе)

Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

Элемент **повторения** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                     | Унаследован от                                                                               | Описание                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при загрузке системы.<br/>                 |
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md)         | Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md)               | Указывает триггер, который запускает задачу при возникновении системного события.<br/>                |
| [**идлетригжер**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**идлетригжертипе**](taskschedulerschema-idletriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.<br/> |
| [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md)               | Указывает триггер, который запускает задачу при входе пользователя в систему.<br/>                       |
| [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) | Указывает триггер, который запускает задачу при регистрации задачи.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**тиметригжертипе**](taskschedulerschema-timetriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при активации триггера.<br/>             |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                   | Тип     | Описание                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Длитель**](taskschedulerschema-duration-repetitiontype-element.md)                   | длительность | Указывает, как долго шаблон повторяется.<br/>                                                              |
| [**Интервал**](taskschedulerschema-interval-repetitiontype-element.md)                   | длительность | Задает интервал времени между перезапусками задачи.<br/>                                           |
| [**стопатдуратионенд**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | Логическое  | Указывает, что выполняющиеся экземпляры задачи останавливаются в конце шаблона повторения.<br/> |



## <a name="remarks"></a>Remarks

Если для задачи задана длительность повторения, необходимо также указать интервал повторения.

Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена пять раз. Пять повторений можно определить в следующем шаблоне.

1.  Задача начинается в начале первой минуты.
2.  Следующая задача начинается в конце первой минуты.
3.  Следующая задача начинается в конце второй минуты.
4.  Следующая задача начинается в конце третьей минуты.
5.  Следующая задача начинается в конце четвертой минуты.

**Windows Server 2003, Windows XP и Windows 2000:** Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена четыре раза.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 и Windows Server 2012:** Как правило, Задание длительности повтора до точно кратного интервала приводит к получению чисел, описанных выше. Однако при определенных условиях высокой нагрузки время ожидания истекло до того, как TaskScheduler может запустить конечный интервал задачи.

Для разработки сценариев шаблон повторения указывается с помощью свойства [**Trigger. повторения**](trigger-repetition.md) , наследуемого всеми объектами триггера.

Для разработки на C++ шаблон повторения указывается с помощью свойства [**итригжер:: повторение**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) , которое наследуется всеми интерфейсами триггера.

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент триггера загрузки, который указывает шаблон повторения для триггера.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



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

 

 





