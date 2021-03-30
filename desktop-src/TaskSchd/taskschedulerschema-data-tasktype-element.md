---
title: Элемент Data (taskType)
description: Определяет дополнительные данные, связанные с задачей, но в противном случае не используется службой планировщик задач.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Элемент данных планировщик задач
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801769"
---
# <a name="data-tasktype-element"></a>Элемент Data (taskType)

Определяет дополнительные данные, связанные с задачей, но в противном случае не используется службой планировщик задач.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

Элемент **Data** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Определяет задачу, выполняемую службой планировщик задач.<br/> |



## <a name="remarks"></a>Комментарии

В качестве примера данных этого типа служба журналы и оповещения производительности использует это свойство в качестве контейнера хранилища для запроса счетчика производительности, связанного с задачей.

Для разработки на C++ данные задачи указываются с помощью [**свойства Data объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

При разработке сценариев данные задачи указываются с помощью свойства [**таскдефинитион. Data**](taskdefinition-data.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





