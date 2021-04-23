---
title: Задания
description: Задача — это запланированная работа, которую выполняет служба планировщик задач.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- задачи планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672135"
---
# <a name="tasks"></a><span data-ttu-id="ceed5-104">Задания</span><span class="sxs-lookup"><span data-stu-id="ceed5-104">Tasks</span></span>

<span data-ttu-id="ceed5-105">Задача — это запланированная работа, которую выполняет служба планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ceed5-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="ceed5-106">Задача состоит из различных компонентов, но задача должна содержать триггер, который планировщик задач использует для запуска задачи, и действие, описывающее, какая работа планировщик задач будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="ceed5-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="ceed5-107">При создании задачи она сохраняется в папке Task.</span><span class="sxs-lookup"><span data-stu-id="ceed5-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="ceed5-108">Доступ к папкам задач можно получить через интерфейс [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**таскфолдер**](taskfolder.md) для сценариев), а доступ к задачам можно получить через интерфейс [**ирегистередтаск**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**регистередтаск**](registeredtask.md) для сценариев) при их создании.</span><span class="sxs-lookup"><span data-stu-id="ceed5-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="ceed5-109">Можно изменить списки управления доступом (ACL) для задач и папок задач, чтобы предоставить или запретить определенным пользователям и группам доступ к задаче или папке задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="ceed5-110">Это можно сделать с помощью метода [**ирегистередтаск:: сетсекуритидескриптор**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , метода [**ITaskFolder:: сетсекуритидескриптор**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) или путем указания дескриптора безопасности при регистрации задачи с помощью метода [**регистертаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) или [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .</span><span class="sxs-lookup"><span data-stu-id="ceed5-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="ceed5-111">Если локальной системной учетной записи запрещен доступ к файлу задачи или папке задачи, то служба планировщик задач может получить непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="ceed5-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="ceed5-112">Компоненты задачи</span><span class="sxs-lookup"><span data-stu-id="ceed5-112">Components of a Task</span></span>

<span data-ttu-id="ceed5-113">На следующем рисунке показаны компоненты задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-113">The following illustration shows the task components.</span></span>

![компоненты задачи](images/taskcomponents.png)

<span data-ttu-id="ceed5-115">В следующем списке содержится краткое описание каждого компонента задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="ceed5-116">Триггеры. планировщик задач использует триггеры на основе событий или времени, чтобы выяснить, когда следует запускать задачу.</span><span class="sxs-lookup"><span data-stu-id="ceed5-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="ceed5-117">Каждая задача может указывать один или несколько триггеров для запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="ceed5-118">Дополнительные сведения о триггерах см. в разделе [триггеры задач](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="ceed5-119">Действия. это действия, фактические работы, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="ceed5-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="ceed5-120">Каждая задача может указывать одно или несколько действий для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="ceed5-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="ceed5-121">Дополнительные сведения о действиях см. в разделе [действия задач](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="ceed5-122">Участники: участники определяют контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="ceed5-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="ceed5-123">Например, участник может определить конкретного пользователя или группу пользователей, которые могут выполнять задачу.</span><span class="sxs-lookup"><span data-stu-id="ceed5-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="ceed5-124">Дополнительные сведения об участниках см. в разделе [контексты безопасности для задач](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="ceed5-125">Параметры. это параметры, которые планировщик задач использует для выполнения задачи в отношении условий, которые являются внешними для самой задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="ceed5-126">Например, эти параметры могут задавать приоритет задачи по отношению к другим задачам, может ли выполняться несколько экземпляров задачи, как задача обрабатывается, когда компьютер находится в состоянии простоя, и другие условия.</span><span class="sxs-lookup"><span data-stu-id="ceed5-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="ceed5-127">Дополнительные сведения о параметрах задач см. в разделе [**итасксеттингс**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**тасксеттингс**](tasksettings.md) для сценариев).</span><span class="sxs-lookup"><span data-stu-id="ceed5-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="ceed5-128">По умолчанию задача будет остановлена 72 часов после начала ее выполнения.</span><span class="sxs-lookup"><span data-stu-id="ceed5-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="ceed5-129">Это можно изменить, изменив параметр [**ексекутионтимелимит**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .</span><span class="sxs-lookup"><span data-stu-id="ceed5-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="ceed5-130">Сведения о регистрации: это административная информация, собираемая при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="ceed5-131">Например, эта информация описывает автора задачи, дату регистрации задачи, XML-описание задачи и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="ceed5-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="ceed5-132">Дополнительные сведения о регистрации задач см. в разделе [сведения о регистрации задачи](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="ceed5-133">Данные. это дополнительная документация о задаче, предоставленная автором задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="ceed5-134">Например, эти данные могут содержать справку в формате XML, которая может использоваться пользователями при выполнении задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="ceed5-135">API-интерфейсы задач</span><span class="sxs-lookup"><span data-stu-id="ceed5-135">Task APIs</span></span>

<span data-ttu-id="ceed5-136">Планировщик задач 2,0 предоставляет два набора интерфейсов API: набор объектов сценариев и интерфейсов для планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="ceed5-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="ceed5-137">Дополнительные сведения см. в разделе [Справочник по планировщик задач](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="ceed5-138">Совместимость задач, которая задается с помощью свойства [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , должна быть установлена только для обеспечения совместимости задач версии 1, \_ Если требуется доступ к \_ задаче или ее изменение с компьютера под управлением Windows XP, Windows Server 2003 или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ceed5-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="ceed5-139">В противном случае рекомендуется использовать совместимость с планировщик задач 2,0, так как она содержит больше функций.</span><span class="sxs-lookup"><span data-stu-id="ceed5-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="ceed5-140">Начиная с планировщик задач 2,0, интерфейс [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) для сценариев) используется в качестве отправной точки для создания задач в указанных папках.</span><span class="sxs-lookup"><span data-stu-id="ceed5-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="ceed5-141">Интерфейс [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**таскдефинитион**](taskdefinition.md) для сценариев) используется для хранения всех компонентов задачи, таких как параметры, действия и триггеры.</span><span class="sxs-lookup"><span data-stu-id="ceed5-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="ceed5-142">Интерфейсы API [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)и [**итасксеттингс**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) предоставляют свойства, которые затем используются для определения других компонентов задачи.</span><span class="sxs-lookup"><span data-stu-id="ceed5-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="ceed5-143">Планировщик задач 1,0 предоставляет интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , который поддерживается только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="ceed5-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="ceed5-144">Для сценариев планировщик задач интерфейсы сопоставляются со скриптами объектов с одинаковыми именами, свойствами и методами.</span><span class="sxs-lookup"><span data-stu-id="ceed5-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="ceed5-145">Например, объект скрипта [**TaskService**](taskservice.md) имеет те же свойства и методы, что и интерфейс [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="ceed5-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="ceed5-146">Дополнительные сведения и примеры использования интерфейсов планировщик задач, сценариев и XML см. [в разделе использование Планировщик задач](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="ceed5-147">Задачи планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="ceed5-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="ceed5-148">Задача планировщик задач 1,0 — это любое приложение или тип файла, которые может выполнять планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ceed5-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="ceed5-149">К ним могут относиться следующие данные (поддерживаемые операционной системой, в которой будет выполняться задача): приложения Win32, приложения Win16, приложения OS/2, приложения MS-DOS, пакетные файлы ( \* . bat), командные файлы ( \* cmd) или любой правильно зарегистрированный тип файла.</span><span class="sxs-lookup"><span data-stu-id="ceed5-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="ceed5-150">Данные, описывающие задачу, хранятся в файле задачи, который хранится в папке «Назначенные задания».</span><span class="sxs-lookup"><span data-stu-id="ceed5-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="ceed5-151">Дополнительные сведения см. в разделе [*Папка запланированных задач*](s.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="ceed5-152">Имена этих файлов задач включают имя задачи, а также расширение имени файла задания.</span><span class="sxs-lookup"><span data-stu-id="ceed5-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="ceed5-153">Дополнительные сведения о добавлении задач планировщик задач 1,0 см. в разделе [Добавление рабочих элементов](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="ceed5-154">Дополнительные сведения о перечислении с помощью задач планировщик задач 1,0 см. в разделе [Перечисление задач](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ceed5-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="ceed5-155">Для компьютера под управлением Windows Server 2003, Windows XP или Windows 2000 для создания, мониторинга или управления задачами на компьютере с Windows Vista на компьютере с Windows Vista должны быть выполнены следующие операции, и пользователь, вызывающий метод [**итасксчедулер:: сеттаржеткомпутер**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) , должен быть членом группы администраторов на удаленном компьютере Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ceed5-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="ceed5-156">**Включение исключения "общий доступ к файлам и принтерам" в брандмауэре Windows**</span><span class="sxs-lookup"><span data-stu-id="ceed5-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="ceed5-157">Нажмите кнопку **Пуск** и выберите **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="ceed5-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="ceed5-158">На **панели управления** щелкните **классический вид** , а затем дважды щелкните значок **Брандмауэр Windows** .</span><span class="sxs-lookup"><span data-stu-id="ceed5-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="ceed5-159">В окне **брандмауэра Windows** перейдите на вкладку **исключения** и установите флажок **исключение для общего доступа к файлам и принтерам** .</span><span class="sxs-lookup"><span data-stu-id="ceed5-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="ceed5-160">**Включение службы "Удаленный реестр"**</span><span class="sxs-lookup"><span data-stu-id="ceed5-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="ceed5-161">Откройте окно командной строки и введите следующую команду: **net start "Удаленный реестр"**.</span><span class="sxs-lookup"><span data-stu-id="ceed5-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceed5-162">См. также</span><span class="sxs-lookup"><span data-stu-id="ceed5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceed5-163">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="ceed5-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="ceed5-164">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="ceed5-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="ceed5-165">Действия задач</span><span class="sxs-lookup"><span data-stu-id="ceed5-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="ceed5-166">**итаскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="ceed5-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="ceed5-167">**таскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="ceed5-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="ceed5-168">**GetFolder интерфейса ITaskService**</span><span class="sxs-lookup"><span data-stu-id="ceed5-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="ceed5-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="ceed5-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




