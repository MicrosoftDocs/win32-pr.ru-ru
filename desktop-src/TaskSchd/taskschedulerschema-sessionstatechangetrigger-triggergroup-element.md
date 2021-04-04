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
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803215"
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
| [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                      | Тип                                                                                    | Описание                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | длительность                                                                                | Задает значение, указывающее длину задержки перед запуском задачи при обнаружении изменения состояния сеанса сервера терминалов.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**сессионстатечанжетипе**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Указывает тип изменения сеанса сервера терминалов, запускающего запуск задачи.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)                 | Указывает пользователя для сеанса сервера терминалов. При обнаружении изменения состояния сеанса для этого пользователя запускается задача.<br/>              |



## <a name="remarks"></a>Комментарии

Для разработки сценариев триггер изменения состояния сеанса указывается с помощью объекта [**сессионстатечанжетригжер**](sessionstatechangetrigger.md) .

Для разработки на C++ триггер изменения состояния сеанса указывается с помощью интерфейса [**исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





