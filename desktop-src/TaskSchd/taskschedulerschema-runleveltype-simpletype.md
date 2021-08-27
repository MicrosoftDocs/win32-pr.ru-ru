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
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991074"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





