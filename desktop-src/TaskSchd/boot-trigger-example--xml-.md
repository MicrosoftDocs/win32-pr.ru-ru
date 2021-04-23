---
title: Пример триггера Boot (XML)
description: В этом примере XML определяет задачу, запускающую Блокнот при загрузке системы.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336038"
---
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="24cbf-103">Пример триггера Boot (XML)</span><span class="sxs-lookup"><span data-stu-id="24cbf-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="24cbf-104">В этом примере XML определяет задачу, запускающую Блокнот при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="24cbf-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="24cbf-105">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="24cbf-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="24cbf-106">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="24cbf-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="24cbf-107">Определение задачи для запуска программы «Блокнот» при загрузке системы</span><span class="sxs-lookup"><span data-stu-id="24cbf-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="24cbf-108">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуском блокнота), одним триггером загрузки, который запускает задачу при загрузке системы, и несколькими другими параметрами задач, влияющими на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="24cbf-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="24cbf-109">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="24cbf-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="24cbf-110">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="24cbf-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="24cbf-111">[**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="24cbf-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="24cbf-112">[**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="24cbf-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="24cbf-113">[**Буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md): определяет триггер загрузки.</span><span class="sxs-lookup"><span data-stu-id="24cbf-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="24cbf-114">В этом случае используются только два дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется.</span><span class="sxs-lookup"><span data-stu-id="24cbf-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="24cbf-115">[**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="24cbf-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="24cbf-116">[**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="24cbf-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="24cbf-117">[**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="24cbf-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="24cbf-118">В этом случае Запустите Блокнот.</span><span class="sxs-lookup"><span data-stu-id="24cbf-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24cbf-119">См. также</span><span class="sxs-lookup"><span data-stu-id="24cbf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24cbf-120">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="24cbf-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




