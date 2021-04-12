---
title: Пример триггера времени (XML)
description: В этом примере XML определяет задачу, которая запускает Блокнот в определенное время.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336025"
---
# <a name="time-trigger-example-xml"></a>Пример триггера времени (XML)

В этом примере XML определяет задачу, которая запускает Блокнот в определенное время.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>Определение задачи для запуска Блокнота в определенное время

В следующем примере XML показано, как определить задачу с одним действием выполнения (запуском блокнота), одним триггером, который запускает задачу в указанное время, и несколькими другими параметрами задач, влияющими на то, как задача обрабатывается планировщик задач.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Элементы схемы TaskScheduler

Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.

-   [**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.
-   [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.
-   [**Тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md): определяет триггер времени. В этом случае используются три дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, а также ограничение времени выполнения, указывающее максимальное время, в течение которого задача может запускаться триггером. Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени.
-   [**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.
-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.
-   [**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




