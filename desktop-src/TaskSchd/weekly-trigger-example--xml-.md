---
title: Пример еженедельного триггера (XML)
description: В этом примере XML определяет задачу, запускающую блокнот на основе еженедельно.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104412372"
---
# <a name="weekly-trigger-example-xml"></a>Пример еженедельного триггера (XML)

В этом примере XML определяет задачу, запускающую блокнот на основе еженедельно.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Определение задачи запуска Блокнота каждую неделю по понедельнику в 8:00 AM

В следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнота), одним триггером календаря (запускает задачу каждую неделю в понедельник в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.


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

-   [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md)

    Определяет триггер, который запускает задачу.

-   [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Определяет триггер еженедельного календаря. В этом случае используются только четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, еженедельное расписание и дни недели, в которых будет выполняться задача. Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.

-   [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Определяет еженедельное расписание. В этом случае интервал задается для выполнения задачи каждую неделю в понедельник.

-   [**Основного**](taskschedulerschema-principal-principaltype-element.md)

    Определяет контекст безопасности, в котором выполняется задача.

-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md)

    Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.

-   [**Действия**](taskschedulerschema-actions-tasktype-element.md)

    Определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




