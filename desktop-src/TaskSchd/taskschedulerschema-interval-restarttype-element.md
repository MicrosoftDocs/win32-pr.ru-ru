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
ms.openlocfilehash: 2362a5d6ec1a6a9d0d876ef0673f4775e2db3ade0a83696ad2b993e31e02a9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099994"
---
# <a name="interval-restarttype-element"></a>Элемент Interval (Рестарттипе)

Указывает, как долго планировщик задач будет пытаться перезапустить задачу. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

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



## <a name="remarks"></a>Remarks

Если этот элемент указан, необходимо также указать элемент [**Count**](taskschedulerschema-count-restarttype-element.md) , чтобы сообщить планировщик задач, сколько раз оно должно попытаться перезапустить задачу.

Сведения о разработке на языке C++ см. в разделе [**свойство рестартинтервал объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. рестартинтервал**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





