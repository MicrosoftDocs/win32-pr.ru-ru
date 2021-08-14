---
title: Элемент Subscription (Евенттригжертипе)
description: Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Элемент Subscription планировщик задач
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ec45a9c240a9dd5d30d2089f98216fc165af13fe418424f5b85feed5e022b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131559"
---
# <a name="subscription-eventtriggertype-element"></a>Элемент Subscription (Евенттригжертипе)

Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

Элемент **Subscription** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                       | Унаследован от                                                                 | Описание                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) | Указывает триггер, который запускает задачу при возникновении системного события.<br/> |



## <a name="remarks"></a>Remarks

Для разработки скриптов подписка на события задается свойством [**EventTrigger. Subscription**](eventtrigger-subscription.md) .

Для разработки на C++ подписка на события задается свойством [**иевенттригжер:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

## <a name="requirements"></a>Requirements (Требования)



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

 

 





