---
title: Элемент Interval (Рестарттипе)
description: Указывает, как долго планировщик задач будет пытаться перезапустить задачу.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Элемент Interval планировщик задач
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988294"
---
# <a name="interval-restarttype-element"></a>Элемент Interval (Рестарттипе)

Указывает, как долго планировщик задач будет пытаться перезапустить задачу. Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент определяется сложным типом [**рестарттипе**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                               | Унаследован от                                                       | Описание                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**рестартонфаилуре**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**рестарттипе**](taskschedulerschema-restarttype-complextype.md) | Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.<br/> |



## <a name="remarks"></a>Комментарии

Если этот элемент указан, необходимо также указать элемент [**Count**](taskschedulerschema-count-restarttype-element.md) , чтобы сообщить планировщик задач, сколько раз оно должно попытаться перезапустить задачу.

Сведения о разработке на языке C++ см. в разделе [**свойство рестартинтервал объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. рестартинтервал**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





