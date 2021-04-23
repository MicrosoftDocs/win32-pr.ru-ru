---
title: Пример ежедневного триггера (XML)
description: В этом примере XML-код определяет задачу, которая запускает Блокнот в 8 00 AM каждый день.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "103785526"
---
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="d0b78-103">Пример ежедневного триггера (XML)</span><span class="sxs-lookup"><span data-stu-id="d0b78-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="d0b78-104">В этом примере XML-код определяет задачу, которая запускает Блокнот в 8:00 AM каждый день.</span><span class="sxs-lookup"><span data-stu-id="d0b78-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="d0b78-105">В примере также показано, как задать шаблон повторения для триггера, чтобы повторить задачу.</span><span class="sxs-lookup"><span data-stu-id="d0b78-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="d0b78-106">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="d0b78-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="d0b78-107">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="d0b78-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="d0b78-108">Определение задачи для запуска Блокнота каждый день в 8:00 AM</span><span class="sxs-lookup"><span data-stu-id="d0b78-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="d0b78-109">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнота), одним триггером календаря (запускает задачу каждый день в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d0b78-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="d0b78-110">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="d0b78-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="d0b78-111">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="d0b78-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="d0b78-112">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="d0b78-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="d0b78-113">Содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d0b78-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="d0b78-114">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="d0b78-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="d0b78-115">Определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="d0b78-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="d0b78-116">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="d0b78-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="d0b78-117">Определяет триггер ежедневного календаря.</span><span class="sxs-lookup"><span data-stu-id="d0b78-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="d0b78-118">В этом случае используются четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, ежедневное расписание и шаблон повторения для задачи.</span><span class="sxs-lookup"><span data-stu-id="d0b78-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="d0b78-119">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.</span><span class="sxs-lookup"><span data-stu-id="d0b78-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="d0b78-120">**счедулебидай**</span><span class="sxs-lookup"><span data-stu-id="d0b78-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="d0b78-121">Определяет ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="d0b78-121">Defines the daily schedule.</span></span> <span data-ttu-id="d0b78-122">В этом случае интервал установлен для выполнения задачи каждый день.</span><span class="sxs-lookup"><span data-stu-id="d0b78-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="d0b78-123">[**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="d0b78-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="d0b78-124">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="d0b78-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="d0b78-125">Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="d0b78-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="d0b78-126">**Действия**</span><span class="sxs-lookup"><span data-stu-id="d0b78-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="d0b78-127">Определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).</span><span class="sxs-lookup"><span data-stu-id="d0b78-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0b78-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d0b78-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b78-129">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="d0b78-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




