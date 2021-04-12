---
title: Рестартонфаилуре (Сеттингстипе), элемент
description: Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- планировщик задач элемента Рестартонфаилуре
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262227"
---
# <a name="restartonfailure-settingstype-element"></a>Рестартонфаилуре (Сеттингстипе), элемент

Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

Элемент **рестартонфаилуре** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип         | Описание                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Расчета**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.<br/> |
| [**Пределах**](taskschedulerschema-interval-restarttype-element.md) | длительность     | Указывает, как долго планировщик задач будет пытаться перезапустить задачу.<br/>                 |



## <a name="remarks"></a>Комментарии

Если приложение задает параметры задачи, доступ к этим данным осуществляется через свойства [**рестарткаунт**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) и [**рестартинтервал**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) интерфейса [**итасксеттингс**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . Для создания скриптов эти сведения доступны через свойства [**тасксеттингс. рестарткаунт**](tasksettings-restartcount.md) и [**тасксеттингс. рестартинтервал**](tasksettings-restartinterval.md) .

Оба дочерних элемента должны быть заданы, чтобы указать, как планировщик задач перезапускает задачу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





