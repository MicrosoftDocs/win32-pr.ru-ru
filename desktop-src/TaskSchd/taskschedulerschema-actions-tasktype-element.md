---
title: Actions (taskType), элемент
description: Содержит действия, выполняемые задачей.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Actions (taskType), элемент планировщик задач
- планировщик задач действий, XML
- Элемент Actions планировщик задач
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415100"
---
# <a name="actions-tasktype-element"></a>Actions (taskType), элемент

Содержит действия, выполняемые задачей.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

Элемент **Actions** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Описывает задачу, выполняемую службой планировщик задач.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                    | Тип                                                                       | Описание                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md)   | Указывает действие, которое вызывает обработчик.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**ексектипе**](taskschedulerschema-exectype-complextype.md)               | Указывает действие, выполняющее операцию командной строки.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md)     | Указывает действие, которое отправляет сообщение электронной почты.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) | Указывает действие, которое отображает окно сообщения.<br/>               |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип | Описание                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Контекст |      | Идентификатор субъекта пользователя, который является контекстом безопасности для действий задачи.<br/> |



## <a name="remarks"></a>Комментарии

Дочерние элементы, перечисленные ранее (максимум 32), определяются группой [**actionGroup**](taskschedulerschema-actiongroup-group.md) . Эти элементы можно добавлять в любом порядке.

Для разработки на C++ действия задачи определяются в интерфейсе [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .

Для разработки скриптов действия задачи определяются в объекте [**ActionCollection**](actioncollection.md) .

## <a name="examples"></a>Примеры

Дополнительные сведения и полный пример XML-кода для задачи, содержащей одно действие выполнения, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





