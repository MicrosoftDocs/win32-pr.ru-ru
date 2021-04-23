---
title: Пример триггера времени (XML)
description: В этом примере XML определяет задачу, которая запускает Блокнот в определенное время.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336025"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="8c105-103">Пример триггера времени (XML)</span><span class="sxs-lookup"><span data-stu-id="8c105-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="8c105-104">В этом примере XML определяет задачу, которая запускает Блокнот в определенное время.</span><span class="sxs-lookup"><span data-stu-id="8c105-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="8c105-105">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8c105-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8c105-106">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8c105-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="8c105-107">Определение задачи для запуска Блокнота в определенное время</span><span class="sxs-lookup"><span data-stu-id="8c105-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="8c105-108">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуском блокнота), одним триггером, который запускает задачу в указанное время, и несколькими другими параметрами задач, влияющими на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="8c105-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8c105-109">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="8c105-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8c105-110">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="8c105-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="8c105-111">[**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="8c105-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="8c105-112">[**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="8c105-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="8c105-113">[**Тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md): определяет триггер времени.</span><span class="sxs-lookup"><span data-stu-id="8c105-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="8c105-114">В этом случае используются три дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, а также ограничение времени выполнения, указывающее максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="8c105-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="8c105-115">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени.</span><span class="sxs-lookup"><span data-stu-id="8c105-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="8c105-116">[**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="8c105-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="8c105-117">[**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="8c105-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="8c105-118">[**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей (в данном случае, запуск Блокнота).</span><span class="sxs-lookup"><span data-stu-id="8c105-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c105-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8c105-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c105-120">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="8c105-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




