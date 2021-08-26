---
title: Ексекутионтимелимит (Тригжербасетипе), элемент
description: Указывает максимальное время, в течение которого задача может запускаться триггером.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- планировщик задач элемента Ексекутионтимелимит
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e958c6a2b873bb78e66645ce2a2ae8100e2acbc
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812525"
---
# <a name="executiontimelimit-triggerbasetype-element"></a>Ексекутионтимелимит (Тригжербасетипе), элемент

Максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

Элемент **ексекутионтимелимит** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-boottriggertype-complextype.md) .

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



## <a name="remarks"></a>Remarks

Для разработки сценариев ограничение времени выполнения указывается с помощью свойства [**Trigger.Exeкутионтимелимит**](trigger-executiontimelimit.md) , наследуемого всеми объектами триггера.

Для разработки на C++ ограничение времени выполнения задается с помощью свойства [**итригжер:: ексекутионтимелимит**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) , наследуемого всеми интерфейсами триггера.

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

 

 





