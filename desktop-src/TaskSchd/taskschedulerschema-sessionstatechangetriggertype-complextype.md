---
title: Сложный тип Сессионстатечанжетригжертипе
description: Определяет элементы, используемые для создания триггера задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- планировщик задач сложного типа Сессионстатечанжетригжертипе
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341300"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Сложный тип Сессионстатечанжетригжертипе

Определяет элементы, используемые для создания триггера задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                      | Тип                                                                                    | Описание                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | длительность                                                                                | Задает значение, указывающее длину задержки перед запуском задачи при обнаружении изменения состояния сеанса сервера терминалов.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**сессионстатечанжетипе**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Указывает тип изменения сеанса сервера терминалов, запускающего запуск задачи.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)                 | Указывает пользователя для сеанса сервера терминалов. При обнаружении изменения состояния сеанса для этого пользователя запускается задача.<br/>              |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





