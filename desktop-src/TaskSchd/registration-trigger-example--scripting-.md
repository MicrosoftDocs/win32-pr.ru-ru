---
title: Пример триггера регистрации (сценарии)
description: В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при регистрации задачи.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332520"
---
# <a name="registration-trigger-example-scripting"></a>Пример триггера регистрации (сценарии)

В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при регистрации задачи. Задача содержит триггер регистрации, указывающий начальную и конечную границы задачи. Начальная граница указывает, когда активируется триггер. Задача также содержит действие, указывающее задачу для выполнения в блокноте.

> [!Note]  
> При обновлении задачи с триггером регистрации задача будет выполнена после обновления.

 

В следующей процедуре описывается, как запланировать запуск исполняемого файла, например Блокнота, при регистрации задачи.

**Планирование запуска программы «Блокнот» при регистрации задачи**

1.  Создайте объект [**TaskService**](taskservice.md) . Этот объект позволяет создать задачу в указанной папке.
2.  Получение папки задачи и создание задачи. Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.
3.  Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) . Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.
4.  Создайте триггер регистрации с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) . Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) . Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера регистрации.
5.  Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) . Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) . Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать. В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.
6.  Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .

В следующем примере VBScript показано, как создать задачу, которая планирует выполнение программы «Блокнот» при регистрации задачи.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
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
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




