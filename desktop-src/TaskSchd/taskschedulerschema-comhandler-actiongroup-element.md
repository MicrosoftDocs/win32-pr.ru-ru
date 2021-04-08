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
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989110"
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
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**Заданий**](taskschedulerschema-datatype-complextype.md) | Указывает дополнительные данные, связанные с обработчиком.<br/> |



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





