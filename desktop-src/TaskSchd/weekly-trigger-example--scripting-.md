---
title: Пример еженедельного триггера (скрипт)
description: В этом примере сценария показано, как создать задачу, запускающую Блокнот в 8 00 утра в понедельник каждой недели.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410772"
---
# <a name="weekly-trigger-example-scripting"></a>Пример еженедельного триггера (скрипт)

В этом примере сценария показано, как создать задачу, запускающую Блокнот в 8:00 утра в понедельник каждой недели. Задача содержит ежедневный триггер, указывающий время выполнения задачи и исполняемое действие, запускающее Блокнот.

Следующая процедура описывает, как запланировать задачу запуска исполняемого файла в 8:00 утра в понедельник каждой недели.

**Чтобы запланировать запуск Блокнота в 8:00 утра в понедельник каждой недели**

1.  Создайте объект [**TaskService**](taskservice.md) . Этот объект позволяет создать задачу в указанной папке.
2.  Получение папки задачи и создание задачи. Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.
3.  Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) . Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.
4.  Создайте еженедельный триггер с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) . Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) , который используется для создания триггера.

    Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который вы хотите создать), чтобы создать еженедельный триггер.

    Задайте свойство [**виклитригжер. стартбаундари**](trigger-startboundary.md) , чтобы указать, когда активируется триггер, и время дня выполнения задачи. В этом примере триггер активируется 1 января 2005, а задача выполняется в 8:00 AM.

    Задайте свойство [**виклитригжер. ендбаундари**](trigger-endboundary.md), чтобы указать, когда активируется триггер. В этом примере триггер деактивируется 1 января 2015.

    Задайте свойство [**виклитригжер. DaysOfWeek**](weeklytrigger-daysofweek.md) , чтобы указать дни недели, в которых выполняется задача. В этом примере задача выполняется в понедельник.

    Задайте свойство [**виклитригжер. виксинтервал**](weeklytrigger-weeksinterval.md), чтобы указать интервал между неделями в расписании. В этом примере задача выполняется каждую неделю.

5.  Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) . Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) , который используется для создания действия. Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое необходимо создать. В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, выполняющее операцию командной строки.
6.  Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) . В этом примере задача запустится в блокноте в 8:00 AM в понедельник каждой недели.

В следующем примере на языке VBScript показано, как запланировать выполнение задачи в блокноте каждый день в 8:00 AM.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
' A constant that specifies an executable action.
const ActionTypeExec = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




