---
title: Пример ежедневного триггера (сценарии)
description: В этом примере сценария показано, как создать задачу, которая запускает приложение «Блокнот» в 8 00 AM каждый день.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888199"
---
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="06689-103">Пример ежедневного триггера (сценарии)</span><span class="sxs-lookup"><span data-stu-id="06689-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="06689-104">В этом примере сценария показано, как создать задачу, которая запускает приложение «Блокнот» в 8:00 AM каждый день.</span><span class="sxs-lookup"><span data-stu-id="06689-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="06689-105">Задача содержит ежедневный триггер, указывающий начальную границу для активации триггера, а также задание времени суток, в течение которого задача выполняется каждый день, и конечную границу для деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="06689-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="06689-106">В примере также показано, как задать шаблон повторения для триггера, чтобы повторить задачу.</span><span class="sxs-lookup"><span data-stu-id="06689-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="06689-107">Задача также содержит исполняемое действие, запускающее Блокнот.</span><span class="sxs-lookup"><span data-stu-id="06689-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="06689-108">Следующая процедура описывает, как запланировать задачу запуска исполняемого файла в 8:00 AM каждый день.</span><span class="sxs-lookup"><span data-stu-id="06689-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="06689-109">(Эти шаги соответствуют комментариям к коду, которые содержатся в примере кода.)</span><span class="sxs-lookup"><span data-stu-id="06689-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="06689-110">**Чтобы запланировать запуск программы "Блокнот" в 8:00 AM каждый день**</span><span class="sxs-lookup"><span data-stu-id="06689-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="06689-111">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="06689-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="06689-112">Этот объект позволяет создать задачу в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="06689-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="06689-113">Получение папки задачи и создание задачи.</span><span class="sxs-lookup"><span data-stu-id="06689-113">Get a task folder and create a task.</span></span> <span data-ttu-id="06689-114">Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.</span><span class="sxs-lookup"><span data-stu-id="06689-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="06689-115">Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="06689-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="06689-116">Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.</span><span class="sxs-lookup"><span data-stu-id="06689-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="06689-117">Создайте ежедневный триггер с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="06689-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="06689-118">Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) , который используется для создания триггера.</span><span class="sxs-lookup"><span data-stu-id="06689-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="06689-119">Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который вы хотите создать) для создания ежедневного триггера.</span><span class="sxs-lookup"><span data-stu-id="06689-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="06689-120">При создании триггера задайте начальную границу для активации триггера и укажите время суток, в течение которого выполняется задача, интервал между днями и конечную границу для деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="06689-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="06689-121">В приведенном ниже примере показано, как задать шаблон повторения для триггера, чтобы повторить задачу.</span><span class="sxs-lookup"><span data-stu-id="06689-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="06689-122">Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="06689-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="06689-123">Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) , который используется для создания действия.</span><span class="sxs-lookup"><span data-stu-id="06689-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="06689-124">Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="06689-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="06689-125">В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="06689-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="06689-126">Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="06689-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="06689-127">В этом примере задача запустится в блокноте каждый день в 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="06689-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="06689-128">В следующем примере на языке VBScript показано, как запланировать выполнение задачи в блокноте каждый день в 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="06689-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

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
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="06689-129">См. также</span><span class="sxs-lookup"><span data-stu-id="06689-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06689-130">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="06689-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




