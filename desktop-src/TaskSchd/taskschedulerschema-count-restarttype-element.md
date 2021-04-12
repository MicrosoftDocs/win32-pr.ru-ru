---
title: Count (Рестарттипе), элемент
description: Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- планировщик задач элемента count
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489861"
---
# <a name="count-restarttype-element"></a>Count (Рестарттипе), элемент

Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
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

Если этот элемент указан, необходимо также указать элемент [**Interval**](taskschedulerschema-interval-restarttype-element.md) , чтобы сообщить планировщик задач, сколько времени попытаться перезапустить задачу.

Сведения о разработке на языке C++ см. в разделе [**свойство рестарткаунт объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. рестарткаунт**](tasksettings-restartcount.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





