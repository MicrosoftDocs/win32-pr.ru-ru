---
title: Стартбаундари (Тригжербасетипе), элемент
description: Указывает дату и время активации триггера.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- планировщик задач элемента Стартбаундари
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46584659fbd14bc26981e220798a91c03e960e1f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886414"
---
# <a name="startboundary-triggerbasetype-element"></a>Стартбаундари (Тригжербасетипе), элемент

Указывает дату и время активации триггера.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

Элемент **стартбаундари** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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



## <a name="remarks"></a>Комментарии

Элемент **&lt; стартбаундари &gt;** является обязательным элементом для триггеров времени и календаря ([**&lt; тиметригжер &gt;**](taskschedulerschema-timetrigger-triggergroup-element.md) и [**&lt; календартригжер &gt;**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Для разработки сценариев конечная граница указывается с помощью свойства [**Trigger. стартбаундари**](trigger-startboundary.md) , наследуемого всеми объектами триггера.

Для разработки на C++ конечная граница указывается с помощью свойства [**итригжер:: стартбаундари**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) , которое наследуется интерфейсами триггера ALL.

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент триггера загрузки, который определяет начальную границу 1 января 2005:8:00 AM.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
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

 

 





