---
title: Пример триггера LOGON (скрипт)
description: В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253049"
---
# <a name="logon-trigger-example-scripting"></a>Пример триггера LOGON (скрипт)

В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему. Задача содержит триггер входа, указывающий начальную границу задачи для запуска, и идентификатор пользователя, указывающий пользователя. Задача регистрируется с помощью группы администраторов в качестве контекста безопасности для выполнения задачи.

Следующая процедура описывает, как запланировать запуск исполняемого файла, например Блокнота, при входе указанного пользователя в систему.

**Планирование запуска программы «Блокнот» при входе пользователя**

1.  Создайте объект [**TaskService**](taskservice.md) . Этот объект позволяет создать задачу в указанной папке.
2.  Получение папки задачи и создание задачи. Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.
3.  Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) . Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.
4.  Создайте триггер входа с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) . Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) . Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера входа. При создании триггера задайте начальную и конечную границы триггера, чтобы активировать и деактивировать триггер. Необходимо задать свойство [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) для триггера, чтобы запланированные действия задачи выполнялись, когда указанный пользователь входит в систему после начальной границы.
5.  Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) . Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) . Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать. В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.
6.  Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) . В этом примере выполняется регистрация задачи, чтобы она использовала группу "Администраторы" в качестве контекста безопасности для выполнения задачи.

В следующем примере на языке VBScript показано, как запланировать задачу для выполнения в блокноте при входе пользователя в систему.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   

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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




