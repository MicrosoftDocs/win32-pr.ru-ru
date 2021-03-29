---
title: Пример ежедневного триггера (XML)
description: В этом примере XML-код определяет задачу, которая запускает Блокнот в 8 00 AM каждый день.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "103785526"
---
# <a name="daily-trigger-example-xml"></a>Пример ежедневного триггера (XML)

В этом примере XML-код определяет задачу, которая запускает Блокнот в 8:00 AM каждый день. В примере также показано, как задать шаблон повторения для триггера, чтобы повторить задачу.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>Определение задачи для запуска Блокнота каждый день в 8:00 AM

В следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнота), одним триггером календаря (запускает задачу каждый день в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
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

-   [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Содержит сведения о регистрации задачи.

-   [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md)

    Определяет триггер, который запускает задачу.

-   [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Определяет триггер ежедневного календаря. В этом случае используются четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, ежедневное расписание и шаблон повторения для задачи. Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.

-   [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Определяет ежедневное расписание. В этом случае интервал установлен для выполнения задачи каждый день.

-   [**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.
-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md)

    Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.

-   [**Действия**](taskschedulerschema-actions-tasktype-element.md)

    Определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




