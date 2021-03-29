---
title: Элемент ClassId (Комхандлертипе)
description: Задает идентификатор класса обработчика.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- планировщик задач элемента ClassId
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493131"
---
# <a name="classid-comhandlertype-element"></a>Элемент ClassId (Комхандлертипе)

Задает идентификатор класса обработчика.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

Элемент **ClassID** определяется сложным типом [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                  | Унаследован от                                                             | Описание                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md) | [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) | Указывает действие, которое вызывает обработчик.<br/> |



## <a name="remarks"></a>Комментарии

Приложения определяют идентификатор класса с помощью свойства [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





