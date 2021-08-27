---
title: Сессионстатечанжетригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- планировщик задач элемента Сессионстатечанжетригжер
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099824"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Сессионстатечанжетригжер (Тригжерграуп), элемент

Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

Элемент **сессионстатечанжетригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**План**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                      | Тип                                                                                    | Описание                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | длительность                                                                                | Задает значение, указывающее длину задержки перед запуском задачи при обнаружении изменения состояния сеанса сервера терминалов.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**сессионстатечанжетипе**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Указывает тип изменения сеанса сервера терминалов, запускающего запуск задачи.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)                 | Указывает пользователя для сеанса сервера терминалов. При обнаружении изменения состояния сеанса для этого пользователя запускается задача.<br/>              |



## <a name="remarks"></a>Remarks

Для разработки сценариев триггер изменения состояния сеанса указывается с помощью объекта [**сессионстатечанжетригжер**](sessionstatechangetrigger.md) .

Для разработки на C++ триггер изменения состояния сеанса указывается с помощью интерфейса [**исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





