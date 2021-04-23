---
title: Пример триггера регистрации (XML)
description: В этом примере XML определяет задачу, которая запускает программу «Блокнот» при регистрации задачи.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "105681576"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="c5d56-103">Пример триггера регистрации (XML)</span><span class="sxs-lookup"><span data-stu-id="c5d56-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="c5d56-104">В этом примере XML определяет задачу, которая запускает программу «Блокнот» при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="c5d56-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="c5d56-105">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="c5d56-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="c5d56-106">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="c5d56-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="c5d56-107">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="c5d56-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="c5d56-108">Определение задачи для запуска Блокнота при регистрации</span><span class="sxs-lookup"><span data-stu-id="c5d56-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="c5d56-109">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуском блокнота), одним триггером регистрации, запускающим задачу при регистрации, и несколькими другими параметрами задач, влияющими на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c5d56-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="c5d56-110">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="c5d56-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="c5d56-111">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="c5d56-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="c5d56-112">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="c5d56-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="c5d56-113">[**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="c5d56-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="c5d56-114">[**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="c5d56-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="c5d56-115">[**Регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md): определяет триггер регистрации.</span><span class="sxs-lookup"><span data-stu-id="c5d56-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="c5d56-116">В этом случае используются только два дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется.</span><span class="sxs-lookup"><span data-stu-id="c5d56-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="c5d56-117">[**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="c5d56-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="c5d56-118">[**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="c5d56-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="c5d56-119">[**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="c5d56-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="c5d56-120">В этом случае Запустите Блокнот.</span><span class="sxs-lookup"><span data-stu-id="c5d56-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5d56-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c5d56-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d56-122">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="c5d56-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




