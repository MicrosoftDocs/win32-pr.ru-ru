---
title: Действия задач
description: Рабочие элементы, выполняемые задачей, называются действиями. Задача может иметь одно действие или не более 32 действий. Имейте в виду, что если указано несколько действий, они выполняются последовательно.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- действия планировщик задач
- действия планировщик задач, описание
- действия планировщик задач, выполнение действия
- действия планировщик задач, действие обработчика COM
- выполнить действие планировщик задач
- планировщик задач действия обработчика COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a7cc4a0e3ecbd4d55e4731379287f2cf4fd660
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470499"
---
# <a name="task-actions"></a>Действия задач

Рабочие элементы, выполняемые задачей, называются действиями. Задача может иметь одно действие или не более 32 действий. Имейте в виду, что если указано несколько действий, они выполняются последовательно.

## <a name="types-of-actions"></a>Типы действий

В следующей таблице действий описывается тип работы или действий, которые могут быть выполнены задачей.

| Тип действия      | Описание                                                             |
|---------------------|-------------------------------------------------------------------------|
| Действие Комхандлер   | Это действие запускает обработчик COM.                                        |
| Действие Exec         | это действие выполняет операцию командной строки, например запуск Блокнот. |
| Действие электронной почты       | Это действие отправляет сообщение электронной почты при активации задачи.                    |
| Отобразить действие сообщения | Это действие отображает окно сообщения с указанным сообщением и заголовком.     |



 

## <a name="specifying-actions"></a>Указание действий

Действия задачи указываются, когда задача определяется и сохраняется в коллекции действий, используемых службой планировщик задач. В следующей таблице перечислены ссылки на справочные материалы по интерфейсам API и XML-элементам, связанным с действиями.

Дополнительные сведения и примеры использования интерфейсов планировщик задач, сценариев и XML см. [в разделе использование Планировщик задач](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>API интерфейса для разработки на C++



| API                                                                    | Описание                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Свойство Actions объекта Итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Возвращает или задает действия, выполняемые задачей.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Содержит действия, выполняемые задачей.                  |
| [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Представляет действие, которое вызывает обработчик.                   |
| [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Представляет действие, выполняющее операцию командной строки. |
| [**иемаилактион**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Представляет действие, которое отправляет сообщение электронной почты.            |
| [**ишовмессажеактион**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Представляет действие, показывающее окно сообщения.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>Создание сценариев для API объектов для разработки сценариев



| API                                                      | Описание                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**Таскдефинитион. Actions**](taskdefinition-actions.md) | Возвращает или задает действия, выполняемые задачей.              |
| [**ActionCollection**](actioncollection.md)             | Содержит действия, выполняемые задачей.                  |
| [**комхандлерактион**](comhandleraction.md)             | Представляет действие, которое вызывает обработчик.                   |
| [**ексекактион**](execaction.md)                         | Представляет действие, выполняющее операцию командной строки. |
| [**емаилактион**](emailaction.md)                       | Представляет действие, которое отправляет сообщение электронной почты.            |
| [**шовмессажеактион**](showmessageaction.md)           | Представляет действие, показывающее окно сообщения.               |



 

### <a name="xml-elements"></a>Элементы XML



| Элемент                                                                    | Описание                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Действия**](taskschedulerschema-actions-tasktype-element.md)            | Определяет действия, выполняемые задачей.                   |
| [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md)   | Представляет действие, которое вызывает обработчик.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Представляет действие, выполняющее операцию командной строки. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Представляет действие, которое отправляет сообщение электронной почты.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Представляет действие, показывающее окно сообщения.               |



 

## <a name="using-variables-in-action-properties"></a>Использование переменных в свойствах действия

Некоторые свойства действий типа **BSTR** могут содержать переменные $ (Arg0), $ (arg1),..., $ (Arg32) в своих строковых значениях. Эти переменные заменяются значениями, заданными в параметре *params* методов [**Ирегистередтаск:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) и [**ирегистередтаск:: рунекс**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) или содержащимися в триггере события для задачи. В следующей таблице перечислены свойства действий, которые могут использовать переменные в своих строковых значениях.


| Действие | Свойства | 
|--------|------------|
| Действие обработчика COM | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Свойство ClassId объекта Икомхандлерактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Свойство Data объекта Икомхандлерактион</strong></a></li></ul><br /> Написание скриптов:<ul><li><a href="comhandleraction-classid.md"><strong>Комхандлерактион. ClassId</strong></a></li><li><a href="comhandleraction-data.md"><strong>Комхандлерактион. Data</strong></a></li></ul><br /> | 
| Действие электронной почты | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Свойство Body объекта Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Свойство сервера Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Свойство Subject объекта Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Для свойства Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Свойство CC объекта Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Свойство BCC объекта Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo, свойство Иемаилактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From, свойство объекта Иемаилактион</strong></a></li></ul><br /> Написание скриптов:<ul><li><a href="emailaction-body.md"><strong>Емаилактион. Body</strong></a></li><li><a href="emailaction-server.md"><strong>Емаилактион. Server</strong></a></li><li><a href="emailaction-subject.md"><strong>Емаилактион. subject</strong></a></li><li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li><li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li><li><a href="emailaction-bcc.md"><strong>Емаилактион. СК</strong></a></li><li><a href="emailaction-replyto.md"><strong>Емаилактион. ReplyTo</strong></a></li><li><a href="emailaction-from.md"><strong>Емаилактион. from</strong></a></li></ul><br /> | 
| Действие Exec | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Свойство Arguments объекта Иексекактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Свойство WorkingDirectory объекта Иексекактион</strong></a></li></ul><br /> Написание скриптов:<ul><li><a href="execaction-arguments.md"><strong>Ексекактион. Arguments</strong></a></li><li><a href="execaction-workingdirectory.md"><strong>Ексекактион. WorkingDirectory</strong></a></li></ul><br /> | 
| Отобразить действие сообщения | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Свойство Title объекта Ишовмессажеактион</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Свойство MessageBody объекта Ишовмессажеактион</strong></a></li></ul><br /> Написание скриптов:<ul><li><a href="showmessageaction-title.md"><strong>Шовмессажеактион. Title</strong></a></li><li><a href="showmessageaction-messagebody.md"><strong>Шовмессажеактион. MessageBody</strong></a></li></ul><br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения о планировщик задач](about-the-task-scheduler.md)
</dt> </dl>

 

 





