---
title: StateChange (Сессионстатечанжетригжертипе), элемент
description: Содержит тип изменения сеанса сервера терминалов, запускающего запуск задачи.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- планировщик задач элемента StateChange
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356336"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>StateChange (Сессионстатечанжетригжертипе), элемент

Содержит тип изменения сеанса сервера терминалов, запускающего запуск задачи.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

Элемент **StateChange** определяется сложным типом [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                       | Унаследован от                                                                                           | Описание                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **сессионстатечанжетригжер** | [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство StateChange объекта исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Сведения о разработке сценариев см. в разделе [**сессионстатечанжетригжер. StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





