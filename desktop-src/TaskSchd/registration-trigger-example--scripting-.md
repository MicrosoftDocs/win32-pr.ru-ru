---
title: Пример триггера регистрации (сценарии)
description: в этом примере сценария показано, как создать задачу, которая запланирована на выполнение Блокнот при регистрации задачи.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f036d4772c98392881f254e07e192c970a2cb407727294c7f196c9c15cb9e11f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011324"
---
# <a name="registration-trigger-example-scripting"></a>Пример триггера регистрации (сценарии)

в этом примере сценария показано, как создать задачу, которая запланирована на выполнение Блокнот при регистрации задачи. Задача содержит триггер регистрации, указывающий начальную и конечную границы задачи. Начальная граница указывает, когда активируется триггер. задача также содержит действие, указывающее задачу, выполняемую Блокнот.

> [!Note]  
> При обновлении задачи с триггером регистрации задача будет выполнена после обновления.

 

следующая процедура описывает, как запланировать исполняемый файл, например Блокнот, для запуска при регистрации задачи.

**планирование Блокнот для запуска при регистрации задачи**

1.  Создайте объект [**TaskService**](taskservice.md) . Этот объект позволяет создать задачу в указанной папке.
2.  Получение папки задачи и создание задачи. Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.
3.  Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) . используйте свойство [**таскдефинитион. Параметры**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.
4.  Создайте триггер регистрации с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) . Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) . Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера регистрации.
5.  Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) . Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) . Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать. В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.
6.  Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .

в следующем примере на языке VBScript показано, как создать задачу, которая планирует выполнение Блокнот при регистрации задачи.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




