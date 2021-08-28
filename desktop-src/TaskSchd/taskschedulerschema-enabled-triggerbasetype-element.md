---
title: Включенный (Тригжербасетипе) элемент
description: Указывает, что триггер включен.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Включенный элемент планировщик задач
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc7ecfb58425533234637708e6c5610f3a84cdaf8e2058d088a68e3c0c707384
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072504"
---
# <a name="enabled-triggerbasetype-element"></a>Включенный (Тригжербасетипе) элемент

Указывает, что триггер включен.

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

Элемент **Enabled** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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

Для разработки сценариев эта информация доступна через свойство [**Trigger. Enabled**](trigger-enabled.md) , которое наследуется всеми объектами триггера.

Для разработки на C++ эта информация доступна через свойство [**итригжер:: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) , унаследованное интерфейсами триггера ALL.

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

 

 





