---
title: Элемент Data (Комхандлертипе)
description: Указывает дополнительные данные, связанные с обработчиком.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
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
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989109"
---
# <a name="data-comhandlertype-element"></a>Элемент Data (Комхандлертипе)

Указывает дополнительные данные, связанные с обработчиком.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

Элемент **Data** определяется сложным типом [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                  | Унаследован от                                                             | Описание                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md) | [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) | Указывает действие, которое вызывает обработчик.<br/> |



## <a name="remarks"></a>Комментарии

Приложения определяют данные обработчика с помощью свойства [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





