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
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803976"
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



## <a name="remarks"></a>Комментарии

Для разработки скриптов подписка на события задается свойством [**EventTrigger. Subscription**](eventtrigger-subscription.md) .

Для разработки на C++ подписка на события задается свойством [**иевенттригжер:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

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

 

 





