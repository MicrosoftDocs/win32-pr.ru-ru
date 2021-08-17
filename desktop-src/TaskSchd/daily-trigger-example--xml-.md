---
title: Пример ежедневного триггера (XML)
description: в этом примере XML-код определяет задачу, которая начинается Блокнот в 8 00 AM каждый день.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd98ada9a69f694d59262682317b7e5be91509b4862f8b896e22b7b0deac2167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139507"
---
# <a name="daily-trigger-example-xml"></a>Пример ежедневного триггера (XML)

в этом примере XML-код определяет задачу, которая начинается Блокнот в 8:00 AM каждый день. В примере также показано, как задать шаблон повторения для триггера, чтобы повторить задачу.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. при использовании средства Schtasks.exe (расположенного в каталоге C: \\ Windows \\ System32) можно зарегистрировать задачу с помощью следующей команды: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>определение задачи для запуска Блокнот каждый день в 8:00 AM

в следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнот), одним триггером календаря (начинается выполнение задачи каждый день в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.


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

-   [**План**](taskschedulerschema-triggers-tasktype-element.md)

    Определяет триггер, который запускает задачу.

-   [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Определяет триггер ежедневного календаря. В этом случае используются четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, ежедневное расписание и шаблон повторения для задачи. Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.

-   [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Определяет ежедневное расписание. В этом случае интервал установлен для выполнения задачи каждый день.

-   [**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.
-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md)

    Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.

-   [**Действия**](taskschedulerschema-actions-tasktype-element.md)

    определяет действия, выполняемые задачей (в данном случае выполняется Блокнот).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




