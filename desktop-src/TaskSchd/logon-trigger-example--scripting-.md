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
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="df275-103">Пример триггера LOGON (скрипт)</span><span class="sxs-lookup"><span data-stu-id="df275-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="df275-104">В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="df275-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="df275-105">Задача содержит триггер входа, указывающий начальную границу задачи для запуска, и идентификатор пользователя, указывающий пользователя.</span><span class="sxs-lookup"><span data-stu-id="df275-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="df275-106">Задача регистрируется с помощью группы администраторов в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="df275-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="df275-107">Следующая процедура описывает, как запланировать запуск исполняемого файла, например Блокнота, при входе указанного пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="df275-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="df275-108">**Планирование запуска программы «Блокнот» при входе пользователя**</span><span class="sxs-lookup"><span data-stu-id="df275-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="df275-109">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="df275-110">Этот объект позволяет создать задачу в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="df275-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="df275-111">Получение папки задачи и создание задачи.</span><span class="sxs-lookup"><span data-stu-id="df275-111">Get a task folder and create a task.</span></span> <span data-ttu-id="df275-112">Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.</span><span class="sxs-lookup"><span data-stu-id="df275-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="df275-113">Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="df275-114">Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.</span><span class="sxs-lookup"><span data-stu-id="df275-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="df275-115">Создайте триггер входа с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="df275-116">Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="df275-117">Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера входа.</span><span class="sxs-lookup"><span data-stu-id="df275-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="df275-118">При создании триггера задайте начальную и конечную границы триггера, чтобы активировать и деактивировать триггер.</span><span class="sxs-lookup"><span data-stu-id="df275-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="df275-119">Необходимо задать свойство [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) для триггера, чтобы запланированные действия задачи выполнялись, когда указанный пользователь входит в систему после начальной границы.</span><span class="sxs-lookup"><span data-stu-id="df275-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="df275-120">Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="df275-121">Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="df275-122">Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать.</span><span class="sxs-lookup"><span data-stu-id="df275-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="df275-123">В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="df275-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="df275-124">Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="df275-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="df275-125">В этом примере выполняется регистрация задачи, чтобы она использовала группу "Администраторы" в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="df275-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="df275-126">В следующем примере на языке VBScript показано, как запланировать задачу для выполнения в блокноте при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="df275-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="df275-127">См. также</span><span class="sxs-lookup"><span data-stu-id="df275-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df275-128">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="df275-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




