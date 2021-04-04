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
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137678"
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



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство StateChange объекта исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Сведения о разработке сценариев см. в разделе [**сессионстатечанжетригжер. StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





