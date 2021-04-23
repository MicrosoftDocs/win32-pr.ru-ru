---
title: Пример триггера LOGON (XML)
description: В этом примере XML определяет задачу, запускающую Блокнот при входе пользователя в систему.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104412378"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="12cdc-103">Пример триггера LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="12cdc-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="12cdc-104">В этом примере XML определяет задачу, запускающую Блокнот при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="12cdc-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="12cdc-105">Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="12cdc-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="12cdc-106">Если вы используете средство Schtasks.exe (расположенное в каталоге C: \\ Windows \\ System32), для регистрации задачи выполните следующую команду: **schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="12cdc-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="12cdc-107">Определение задачи для запуска программы «Блокнот» при загрузке системы</span><span class="sxs-lookup"><span data-stu-id="12cdc-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="12cdc-108">В следующем примере XML показано, как определить задачу с одним действием выполнения (запуском блокнота), одним триггером входа, запускающим задачу при входе пользователя в систему, и несколькими другими параметрами задач, влияющими на то, как задача обрабатывается планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="12cdc-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="12cdc-109">В качестве значения элемента **UserID** задайте имя пользователя на компьютере, на котором зарегистрирована задача.</span><span class="sxs-lookup"><span data-stu-id="12cdc-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="12cdc-110">Элементы схемы TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="12cdc-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="12cdc-111">Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.</span><span class="sxs-lookup"><span data-stu-id="12cdc-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="12cdc-112">[**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="12cdc-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="12cdc-113">[**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.</span><span class="sxs-lookup"><span data-stu-id="12cdc-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="12cdc-114">[**Логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md): определяет триггер входа.</span><span class="sxs-lookup"><span data-stu-id="12cdc-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="12cdc-115">В этом случае используются три дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, и элемент [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) , который является идентификатором пользователя.</span><span class="sxs-lookup"><span data-stu-id="12cdc-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="12cdc-116">Задача запускается, когда пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="12cdc-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="12cdc-117">[**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="12cdc-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="12cdc-118">[**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="12cdc-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="12cdc-119">[**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="12cdc-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="12cdc-120">В этом случае Запустите Блокнот.</span><span class="sxs-lookup"><span data-stu-id="12cdc-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12cdc-121">См. также</span><span class="sxs-lookup"><span data-stu-id="12cdc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12cdc-122">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="12cdc-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




