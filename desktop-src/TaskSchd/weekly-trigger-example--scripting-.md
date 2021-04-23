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
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="0b158-103">Пример еженедельного триггера (скрипт)</span><span class="sxs-lookup"><span data-stu-id="0b158-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="0b158-104">В этом примере сценария показано, как создать задачу, запускающую Блокнот в 8:00 утра в понедельник каждой недели.</span><span class="sxs-lookup"><span data-stu-id="0b158-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="0b158-105">Задача содержит ежедневный триггер, указывающий время выполнения задачи и исполняемое действие, запускающее Блокнот.</span><span class="sxs-lookup"><span data-stu-id="0b158-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="0b158-106">Следующая процедура описывает, как запланировать задачу запуска исполняемого файла в 8:00 утра в понедельник каждой недели.</span><span class="sxs-lookup"><span data-stu-id="0b158-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="0b158-107">**Чтобы запланировать запуск Блокнота в 8:00 утра в понедельник каждой недели**</span><span class="sxs-lookup"><span data-stu-id="0b158-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="0b158-108">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0b158-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="0b158-109">Этот объект позволяет создать задачу в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="0b158-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="0b158-110">Получение папки задачи и создание задачи.</span><span class="sxs-lookup"><span data-stu-id="0b158-110">Get a task folder and create a task.</span></span> <span data-ttu-id="0b158-111">Используйте метод [**TaskService.**](taskservice-getfolder.md) GetObject, чтобы получить папку, в которой хранится задача, и метод [**TaskService.**](taskservice-newtask.md) Create, чтобы создать объект [**таскдефинитион**](taskdefinition.md) , представляющий задачу.</span><span class="sxs-lookup"><span data-stu-id="0b158-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="0b158-112">Определите сведения о задаче с помощью объекта [**таскдефинитион**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0b158-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="0b158-113">Используйте свойство [**таскдефинитион. Settings**](taskdefinition-settings.md) , чтобы определить параметры, определяющие, как служба Планировщик задач выполняет задачу, и свойство [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) для определения сведений, описывающих задачу.</span><span class="sxs-lookup"><span data-stu-id="0b158-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="0b158-114">Создайте еженедельный триггер с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="0b158-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="0b158-115">Это свойство предоставляет доступ к объекту [**тригжерколлектион**](triggercollection.md) , который используется для создания триггера.</span><span class="sxs-lookup"><span data-stu-id="0b158-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="0b158-116">Используйте метод [**тригжерколлектион. Create**](triggercollection-create.md) (указав тип триггера, который вы хотите создать), чтобы создать еженедельный триггер.</span><span class="sxs-lookup"><span data-stu-id="0b158-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="0b158-117">Задайте свойство [**виклитригжер. стартбаундари**](trigger-startboundary.md) , чтобы указать, когда активируется триггер, и время дня выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0b158-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="0b158-118">В этом примере триггер активируется 1 января 2005, а задача выполняется в 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="0b158-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="0b158-119">Задайте свойство [**виклитригжер. ендбаундари**](trigger-endboundary.md), чтобы указать, когда активируется триггер.</span><span class="sxs-lookup"><span data-stu-id="0b158-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="0b158-120">В этом примере триггер деактивируется 1 января 2015.</span><span class="sxs-lookup"><span data-stu-id="0b158-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="0b158-121">Задайте свойство [**виклитригжер. DaysOfWeek**](weeklytrigger-daysofweek.md) , чтобы указать дни недели, в которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="0b158-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="0b158-122">В этом примере задача выполняется в понедельник.</span><span class="sxs-lookup"><span data-stu-id="0b158-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="0b158-123">Задайте свойство [**виклитригжер. виксинтервал**](weeklytrigger-weeksinterval.md), чтобы указать интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="0b158-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="0b158-124">В этом примере задача выполняется каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="0b158-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="0b158-125">Создайте действие для выполнения задачи с помощью свойства [**таскдефинитион. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="0b158-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="0b158-126">Это свойство предоставляет доступ к объекту [**ActionCollection**](actioncollection.md) , который используется для создания действия.</span><span class="sxs-lookup"><span data-stu-id="0b158-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="0b158-127">Используйте метод [**ActionCollection. Create**](actioncollection-create.md) , чтобы указать тип действия, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="0b158-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="0b158-128">В этом примере используется объект [**ексекактион**](execaction.md) , который представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="0b158-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="0b158-129">Зарегистрируйте задачу с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0b158-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="0b158-130">В этом примере задача запустится в блокноте в 8:00 AM в понедельник каждой недели.</span><span class="sxs-lookup"><span data-stu-id="0b158-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="0b158-131">В следующем примере на языке VBScript показано, как запланировать выполнение задачи в блокноте каждый день в 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="0b158-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0b158-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0b158-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b158-133">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="0b158-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




