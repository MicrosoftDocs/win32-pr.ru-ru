---
title: Комхандлер (actionGroup), элемент
description: Указывает действие, которое вызывает обработчик.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- планировщик задач элемента Комхандлер
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aba73244c3dc5217bcfe7350462200cd3226f0607c6d68ce5c6bcb8f5574b7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943241"
---
# <a name="comhandler-actiongroup-element"></a>Комхандлер (actionGroup), элемент

Указывает действие, которое вызывает обработчик.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

Элемент **комхандлер** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                         | Унаследован от                                                       | Описание                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Действия**](taskschedulerschema-actions-tasktype-element.md) | [**актионстипе**](taskschedulerschema-actionstype-complextype.md) | Содержит действия, выполняемые задачей.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип                                                         | Описание                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Класса**](taskschedulerschema-classid-comhandlertype-element.md) | [**гуидтипе**](taskschedulerschema-guidtype-simpletype.md)  | Задает идентификатор класса обработчика.<br/>         |
| [**Данные**](taskschedulerschema-data-comhandlertype-element.md)       | [**Заданий**](taskschedulerschema-datatype-complextype.md) | Указывает дополнительные данные, связанные с обработчиком.<br/> |



## <a name="remarks"></a>Remarks

Приложения определяют действие обработчика COM с помощью интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

### <a name="attributes"></a>Атрибуты

Следующий атрибут определяется сложным типом [**актионбасетипе**](taskschedulerschema-actionbasetype-complextype.md) .

-   Идентификатор: идентификатор действия, выполняемого задачей.

## <a name="examples"></a>Примеры

Следующий XML-код определяет действие обработчика COM.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





