---
title: Пример триггера загрузки (написание сценариев)
description: В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при загрузке системы.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067987"
---
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="0b2ca-103">Пример триггера загрузки (написание сценариев)</span><span class="sxs-lookup"><span data-stu-id="0b2ca-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="0b2ca-104">В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="0b2ca-105">Задача содержит триггер загрузки, который задает начальную границу и время задержки для запуска задачи после загрузки системы.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="0b2ca-106">Задача также содержит действие, указывающее задачу для выполнения в блокноте.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="0b2ca-107">Задача регистрируется с использованием учетной записи локальной службы в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="0b2ca-108">В следующей процедуре описывается, как запланировать запуск исполняемого файла, например Блокнота, при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="0b2ca-109">**Планирование запуска программы «Блокнот» при загрузке системы**</span><span class="sxs-lookup"><span data-stu-id="0b2ca-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="0b2ca-110">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="0b2ca-111">Этот объект позволяет создать задачу в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="0b2ca-112">Получение папки задачи и создание задачи.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-112">Get a task folder and create a task.</span></span> <span data-ttu-id="0b2ca-113">Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="0b2ca-114">Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="0b2ca-115">Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="0b2ca-116">Создайте триггер входа с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="0b2ca-117">Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="0b2ca-118">Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера загрузки.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="0b2ca-119">При создании триггера задайте свойства [**стартбаундари**](trigger-startboundary.md) и [**ендбаундари**](trigger-endboundary.md) триггера, чтобы активировать и деактивировать триггер.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="0b2ca-120">Можно также указать значение свойства [**delay**](boottrigger-delay.md) триггера загрузки.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="0b2ca-121">Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="0b2ca-122">Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="0b2ca-123">Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="0b2ca-124">В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="0b2ca-125">Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ca-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="0b2ca-126">Задача регистрируется с использованием учетной записи локальной службы в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="0b2ca-127">В следующем примере на языке VBScript показано, как запланировать выполнение задачи через 30 секунд после загрузки системы.</span><span class="sxs-lookup"><span data-stu-id="0b2ca-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

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
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="0b2ca-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0b2ca-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b2ca-129">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="0b2ca-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




