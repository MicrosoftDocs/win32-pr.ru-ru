---
title: Пример еженедельного триггера (XML)
description: В этом примере XML определяет задачу, запускающую блокнот на основе еженедельно.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104412372"
---
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="646c1-103">Пример еженедельного триггера (XML)</span><span class="sxs-lookup"><span data-stu-id="646c1-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="646c1-104">В этом примере XML определяет задачу, запускающую блокнот на основе еженедельно.</span><span class="sxs-lookup"><span data-stu-id="646c1-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="646c1-105">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="646c1-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="646c1-106">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="646c1-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="646c1-107">Определение задачи запуска Блокнота каждую неделю по понедельнику в 8:00 AM</span><span class="sxs-lookup"><span data-stu-id="646c1-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="646c1-108">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнота), одним триггером календаря (запускает задачу каждую неделю в понедельник в 8:00 AM), а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="646c1-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="646c1-109">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="646c1-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="646c1-110">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="646c1-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="646c1-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="646c1-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="646c1-112">Содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="646c1-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="646c1-113">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="646c1-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="646c1-114">Определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="646c1-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="646c1-115">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="646c1-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="646c1-116">Определяет триггер еженедельного календаря.</span><span class="sxs-lookup"><span data-stu-id="646c1-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="646c1-117">В этом случае используются только четыре дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, еженедельное расписание и дни недели, в которых будет выполняться задача.</span><span class="sxs-lookup"><span data-stu-id="646c1-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="646c1-118">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров календаря.</span><span class="sxs-lookup"><span data-stu-id="646c1-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="646c1-119">**счедулебивик**</span><span class="sxs-lookup"><span data-stu-id="646c1-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="646c1-120">Определяет еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="646c1-120">Defines the weekly schedule.</span></span> <span data-ttu-id="646c1-121">В этом случае интервал задается для выполнения задачи каждую неделю в понедельник.</span><span class="sxs-lookup"><span data-stu-id="646c1-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="646c1-122">**Основного**</span><span class="sxs-lookup"><span data-stu-id="646c1-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="646c1-123">Определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="646c1-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="646c1-124">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="646c1-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="646c1-125">Определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="646c1-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="646c1-126">**Действия**</span><span class="sxs-lookup"><span data-stu-id="646c1-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="646c1-127">Определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).</span><span class="sxs-lookup"><span data-stu-id="646c1-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="646c1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="646c1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="646c1-129">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="646c1-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




