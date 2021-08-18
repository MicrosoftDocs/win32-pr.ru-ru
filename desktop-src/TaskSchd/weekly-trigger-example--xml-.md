---
title: Пример еженедельного триггера (XML)
description: в этом примере XML определяет задачу, которая начинается Блокнот раз в неделю.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c038c21db137ce9180d76cecf4c2885274f7cdd72720b12b919f9a39e98e575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001817"
---
# <a name="weekly-trigger-example-xml"></a>Пример еженедельного триггера (XML)

в этом примере XML определяет задачу, которая начинается Блокнот раз в неделю.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. при использовании средства Schtasks.exe (расположенного в каталоге C: \\ Windows \\ System32) можно зарегистрировать задачу с помощью следующей команды: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>определение задачи для запуска Блокнот каждую неделю в понедельник в 8:00 AM

в следующем примере XML показано, как определить задачу с одним действием выполнения (начиная Блокнот), одним триггером календаря (запускает задачу каждую неделю в понедельник в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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

    Определяет триггер еженедельного календаря. В этом случае используются только четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, еженедельное расписание и дни недели, в которых будет выполняться задача. Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.

-   [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Определяет еженедельное расписание. В этом случае интервал задается для выполнения задачи каждую неделю в понедельник.

-   [**Основной**](taskschedulerschema-principal-principaltype-element.md)

    Определяет контекст безопасности, в котором выполняется задача.

-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md)

    Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.

-   [**Actions**](taskschedulerschema-actions-tasktype-element.md)

    определяет действия, выполняемые задачей (в данном случае выполняется Блокнот).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




