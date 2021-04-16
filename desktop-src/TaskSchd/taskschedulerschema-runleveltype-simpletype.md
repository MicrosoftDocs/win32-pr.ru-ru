---
title: Простой тип Рунлевелтипе
description: Определяет возможные значения для элемента RunLevel (ПринЦипалтипе).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- планировщик задач простого типа Рунлевелтипе
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672783"
---
# <a name="runleveltype-simple-type"></a>Простой тип Рунлевелтипе

Определяет возможные значения для элемента [**runlevel (принЦипалтипе)**](taskschedulerschema-runlevel-principaltype-element.md) .

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **рунлевелтипе** определяет следующие значения.



| Значение            | Описание                                               |
|------------------|-----------------------------------------------------------|
| леастпривилеже   | Задачи выполняются с наименьшими привилегиями (LUA).<br/> |
| HighestAvailable | Задачи выполняются с самыми высокими привилегиями.<br/>     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





