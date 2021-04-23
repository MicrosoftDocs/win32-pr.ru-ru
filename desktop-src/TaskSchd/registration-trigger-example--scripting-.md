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
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="7bb26-103">Пример триггера регистрации (сценарии)</span><span class="sxs-lookup"><span data-stu-id="7bb26-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="7bb26-104">В этом примере сценария показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="7bb26-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="7bb26-105">Задача содержит триггер регистрации, указывающий начальную и конечную границы задачи.</span><span class="sxs-lookup"><span data-stu-id="7bb26-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="7bb26-106">Начальная граница указывает, когда активируется триггер.</span><span class="sxs-lookup"><span data-stu-id="7bb26-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="7bb26-107">Задача также содержит действие, указывающее задачу для выполнения в блокноте.</span><span class="sxs-lookup"><span data-stu-id="7bb26-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="7bb26-108">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="7bb26-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="7bb26-109">В следующей процедуре описывается, как запланировать запуск исполняемого файла, например Блокнота, при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="7bb26-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="7bb26-110">**Планирование запуска программы «Блокнот» при регистрации задачи**</span><span class="sxs-lookup"><span data-stu-id="7bb26-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="7bb26-111">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="7bb26-112">Этот объект позволяет создать задачу в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="7bb26-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="7bb26-113">Получение папки задачи и создание задачи.</span><span class="sxs-lookup"><span data-stu-id="7bb26-113">Get a task folder and create a task.</span></span> <span data-ttu-id="7bb26-114">Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.</span><span class="sxs-lookup"><span data-stu-id="7bb26-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="7bb26-115">Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="7bb26-116">Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.</span><span class="sxs-lookup"><span data-stu-id="7bb26-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="7bb26-117">Создайте триггер регистрации с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="7bb26-118">Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="7bb26-119">Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который требуется создать) для создания триггера регистрации.</span><span class="sxs-lookup"><span data-stu-id="7bb26-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="7bb26-120">Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="7bb26-121">Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="7bb26-122">Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое требуется создать.</span><span class="sxs-lookup"><span data-stu-id="7bb26-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="7bb26-123">В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, запускающее исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="7bb26-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="7bb26-124">Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7bb26-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="7bb26-125">В следующем примере VBScript показано, как создать задачу, которая планирует выполнение программы «Блокнот» при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="7bb26-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7bb26-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7bb26-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb26-127">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7bb26-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




