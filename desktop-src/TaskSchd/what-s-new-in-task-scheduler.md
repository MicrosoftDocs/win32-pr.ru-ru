---
title: Новые возможности планировщик задач
description: Список новых функциональных возможностей, появившихся в разных версиях планировщик задач.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Планировщик задач планировщик задач, новые возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673153"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="c8685-104">Новые возможности планировщик задач</span><span class="sxs-lookup"><span data-stu-id="c8685-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="c8685-105">Следующие изменения обобщают новые возможности в разных версиях планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c8685-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="c8685-106">Windows 10 (и Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="c8685-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="c8685-107">В Windows 10 появились следующие изменения планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c8685-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="c8685-108">При включенной экономии заряда задачи Windows планировщик задач запускаются только в том случае, если задано следующее:</span><span class="sxs-lookup"><span data-stu-id="c8685-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="c8685-109">Не задано для **запуска задачи только в том случае, если компьютер бездействует...** (задача не использует [**идлесеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="c8685-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="c8685-110">Не задано для запуска во время автоматического обслуживания (задача не использует [**маинтенанцесеттингс**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="c8685-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="c8685-111">Задается для **запуска только при входе пользователя в систему** (задача [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) — **\_ \_ Интерактивный \_ маркер входа в систему** или **\_ \_ Группа входа задач**).</span><span class="sxs-lookup"><span data-stu-id="c8685-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="c8685-112">Все остальные триггеры откладываются до тех пор, пока не будет снята экономия заряда.</span><span class="sxs-lookup"><span data-stu-id="c8685-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="c8685-113">Дополнительные сведения о доступе к состоянию заставки аккумулятора в приложении см. в разделе [**\_ \_ состояние питания системы**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span><span class="sxs-lookup"><span data-stu-id="c8685-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="c8685-114">Общие сведения о экономии заряда батареи см. [в разделе Заставка аккумулятора (в руководстве по компонентам оборудования)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="c8685-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="c8685-115">По соображениям безопасности пользователь без прав администратора не может просматривать или управлять задачей планировщик задач Windows, созданной другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="c8685-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="c8685-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c8685-116">Windows 8</span></span>

<span data-ttu-id="c8685-117">В Windows 8 появились следующие изменения планировщик задач 2,0:</span><span class="sxs-lookup"><span data-stu-id="c8685-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="c8685-118">Поддержка PowerShell: пользователи могут управлять (создавать, удалять, изменять, явно запускать, прекращать и т. д.). Задачи планировщик задач Windows с помощью модуля PowerShell Счедуледтаскс.</span><span class="sxs-lookup"><span data-stu-id="c8685-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="c8685-119">Управляемые пароли. Администраторы могут использовать Active Directory управляемые учетные записи паролей в качестве участников задач.</span><span class="sxs-lookup"><span data-stu-id="c8685-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="c8685-120">Для этих задач больше не требуется принудительная политика сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="c8685-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="c8685-121">Изменения API: появились два новых параметра задачи с интерфейсом [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .</span><span class="sxs-lookup"><span data-stu-id="c8685-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="c8685-122">[**Маинтенанцесеттингс**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings). задачи, использующие эти параметры, рассматриваются как новые типы запланированных задач, которые вызываются во время автоматического обслуживания ОС в соответствии с заданными периодичностью и крайним сроком.</span><span class="sxs-lookup"><span data-stu-id="c8685-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="c8685-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile). задания, которые являются временными, всегда отключаются при загрузке ОС и должны быть явно повторно включены при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c8685-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="c8685-124">Временные задачи используются отказоустойчивыми кластерами, чтобы гарантировать, что в кластере одновременно планируется только один экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="c8685-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="c8685-125">Механизм единого планирования теперь поддерживает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="c8685-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="c8685-126">Тип входа S4U с помощью элемента [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c8685-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="c8685-127">Значения запроса XPath для триггеров событий с помощью элемента [**валуекуериес**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c8685-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="c8685-128">Не разрешать жесткое завершение задачи с помощью элемента [**алловхардтерминате**](taskschedulerschema-allowhardterminate-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c8685-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="c8685-129">Функции, устаревшие в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="c8685-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="c8685-130">Действие: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (в качестве обходного пути можно использовать [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) с командлетом [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) ).</span><span class="sxs-lookup"><span data-stu-id="c8685-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="c8685-131">Действие: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="c8685-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="c8685-132">AT.exe cmdline, программа</span><span class="sxs-lookup"><span data-stu-id="c8685-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="c8685-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8685-133">Windows 7</span></span>

<span data-ttu-id="c8685-134">В Windows 7 появились следующие изменения планировщик задач 2,0:</span><span class="sxs-lookup"><span data-stu-id="c8685-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="c8685-135">С помощью единого механизма планирования, предоставляемого базовой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="c8685-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="c8685-136">Возможность отклонять запуск задач в удаленных приложениях, интегрированных локально (на шинах) сеансах.</span><span class="sxs-lookup"><span data-stu-id="c8685-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="c8685-137">Усиление безопасности задач (для задач, выполняемых как "СЕТЕВая служба" или "только ЛОКАЛЬная служба"):</span><span class="sxs-lookup"><span data-stu-id="c8685-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="c8685-138">Возможность назначения задаче типа идентификатора безопасности (например, неограниченности или отсутствия).</span><span class="sxs-lookup"><span data-stu-id="c8685-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="c8685-139">Разрешить разработчикам задач запрашивать точный набор привилегий, необходимых для их задачи.</span><span class="sxs-lookup"><span data-stu-id="c8685-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="c8685-140">Изменения API:</span><span class="sxs-lookup"><span data-stu-id="c8685-140">API changes:</span></span>

    -   <span data-ttu-id="c8685-141">Поддержка усиления безопасности для задач. Новая функция усиления безопасности задач появилась в новом интерфейсе IPrincipal2.</span><span class="sxs-lookup"><span data-stu-id="c8685-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="c8685-142">Появились два новых параметра задачи с новым интерфейсом ITaskSettings2.</span><span class="sxs-lookup"><span data-stu-id="c8685-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="c8685-143">Дисалловстартонремотеаппсессион. новый параметр Дисалловстартонремотеаппсессион может отклонить запуск задачи, если он активирован в [удаленных приложениях, интегрированных локально (шина)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .</span><span class="sxs-lookup"><span data-stu-id="c8685-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="c8685-144">Усеунифиедсчедулинженгине. Использование параметра Усеунифиедсчедулинженгине обеспечивает согласованное поведение для задач и служб Windows, так как управление осуществляется единообразно с помощью общего механизма планирования на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="c8685-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="c8685-145">Хотя рекомендуется использовать унифицированный механизм, он не поддерживает некоторые функции планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c8685-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="c8685-146">Если сочетание свойств не разрешит выполнение задачи в едином механизме, регистрация такого объекта будет отклонена.</span><span class="sxs-lookup"><span data-stu-id="c8685-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="c8685-147">Функции задач, которые не поддерживаются единым ядром планирования, включают:</span><span class="sxs-lookup"><span data-stu-id="c8685-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="c8685-148">Типы входа:</span><span class="sxs-lookup"><span data-stu-id="c8685-148">Logon types:</span></span>

                -   [<span data-ttu-id="c8685-149">\_ \_ Интерактивный маркер входа для задачи \_ \_ или \_ пароль</span><span class="sxs-lookup"><span data-stu-id="c8685-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="c8685-150">Политика нескольких экземпляров:</span><span class="sxs-lookup"><span data-stu-id="c8685-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="c8685-151">**\_экземпляры задач \_ прекращают \_ существующие**</span><span class="sxs-lookup"><span data-stu-id="c8685-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="c8685-152">Действия:</span><span class="sxs-lookup"><span data-stu-id="c8685-152">Actions:</span></span>

                -   [<span data-ttu-id="c8685-153">Отправка электронного сообщения</span><span class="sxs-lookup"><span data-stu-id="c8685-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="c8685-154">Отображение сообщения</span><span class="sxs-lookup"><span data-stu-id="c8685-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="c8685-155">Параметры:</span><span class="sxs-lookup"><span data-stu-id="c8685-155">Settings:</span></span>

                -   [<span data-ttu-id="c8685-156">Сетевые параметры задачи</span><span class="sxs-lookup"><span data-stu-id="c8685-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="c8685-157">Запретить жесткое завершение задачи</span><span class="sxs-lookup"><span data-stu-id="c8685-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="c8685-158">Триггеры:</span><span class="sxs-lookup"><span data-stu-id="c8685-158">Triggers:</span></span>

                -   [<span data-ttu-id="c8685-159">Ограничение времени выполнения триггера</span><span class="sxs-lookup"><span data-stu-id="c8685-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="c8685-160">Шаблоны повторений для триггеров календаря</span><span class="sxs-lookup"><span data-stu-id="c8685-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="c8685-161">Значения запроса XPath для триггеров событий</span><span class="sxs-lookup"><span data-stu-id="c8685-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="c8685-162">[Ежемесячные](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) и месячные типы триггеров [дней недели](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)</span><span class="sxs-lookup"><span data-stu-id="c8685-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="c8685-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8685-163">Windows Vista</span></span>

<span data-ttu-id="c8685-164">Планировщик задач API 2,0 следует использовать при разработке приложений, использующих службу планировщик задач в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8685-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="c8685-165">Дополнительные сведения см. в разделе [Справочник по планировщик задач](task-scheduler-reference.md) и [Использование планировщик задач](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="c8685-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="c8685-166">Windows 2000, Windows XP и Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8685-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="c8685-167">API-интерфейс планировщик задач 2,0 недоступен.</span><span class="sxs-lookup"><span data-stu-id="c8685-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="c8685-168">Используйте планировщик задач 1,0.</span><span class="sxs-lookup"><span data-stu-id="c8685-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8685-169">См. также</span><span class="sxs-lookup"><span data-stu-id="c8685-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8685-170">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c8685-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c8685-171">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="c8685-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
