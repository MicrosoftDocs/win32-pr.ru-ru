---
title: Объект Action
description: Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами Action.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- планировщик задач объекта действия
- Объект Action планировщик задач, описание
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739044"
---
# <a name="action-object"></a>Объект Action

Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами Action. Объект действия создается методом [**ActionCollection. Create**](actioncollection-create.md) .

## <a name="members"></a>Элементы

Объект **Action** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **Action** имеет следующие свойства.



| Свойство                               | Тип доступа           | Описание                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Удостоверения**](action-id.md)<br/>     | Чтение/запись<br/> | Возвращает или задает идентификатор действия.<br/> |
| [**Тип**](action-type.md)<br/> | Только для чтения<br/>  | Возвращает тип действия.<br/>               |



 

## <a name="remarks"></a>Remarks

Сведения о совместной работе действий и задач см. в разделе [действия задач](task-actions.md). В следующей таблице содержатся объекты скрипта, представляющие действия, которые могут быть выполнены.



| API                                            | Описание                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**комхандлерактион**](comhandleraction.md)   | Представляет действие, которое вызывает обработчик.                   |
| [**ексекактион**](execaction.md)               | Представляет действие, выполняющее операцию командной строки. |
| [**емаилактион**](emailaction.md)             | Представляет действие, которое отправляет сообщение электронной почты.            |
| [**шовмессажеактион**](showmessageaction.md) | Представляет действие, показывающее окно сообщения.               |



 

При чтении или записи XML действия задачи указываются в элементе [**Actions**](taskschedulerschema-actions-tasktype-element.md) схемы планировщик задач.

## <a name="examples"></a>Примеры

Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии](time-trigger-example--scripting-.md) ), пример триггера [события (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))сценарии) [, пример ежедневного триггера](daily-trigger-example--scripting-.md)(сценарии), пример триггера [регистрации](registration-trigger-example--scripting-.md)(сценарии) [, пример](weekly-trigger-example--scripting-.md)триггера [входа](logon-trigger-example--scripting-.md)(скрипт), пример триггера [загрузки](boot-trigger-example--scripting-.md)(скрипт).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач объектов скрипта](task-scheduler-objects.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





