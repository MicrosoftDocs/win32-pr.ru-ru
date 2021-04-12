---
title: Элемент Settings (taskType)
description: Задает параметры, которые планировщик задач использует для выполнения задачи.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Элемент Settings планировщик задач
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415232"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="770e8-104">Элемент Settings (taskType)</span><span class="sxs-lookup"><span data-stu-id="770e8-104">Settings (taskType) Element</span></span>

<span data-ttu-id="770e8-105">Задает параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="770e8-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="770e8-106">Элемент **Settings** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="770e8-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="770e8-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="770e8-107">Parent element</span></span>



| <span data-ttu-id="770e8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="770e8-108">Element</span></span>                                          | <span data-ttu-id="770e8-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="770e8-109">Derived from</span></span>                                                 | <span data-ttu-id="770e8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="770e8-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="770e8-111">**Задача**</span><span class="sxs-lookup"><span data-stu-id="770e8-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="770e8-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="770e8-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="770e8-113">Указывает задачу, которая выполняется службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="770e8-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="770e8-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="770e8-114">Child elements</span></span>



| <span data-ttu-id="770e8-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="770e8-115">Element</span></span>                                                                                                          | <span data-ttu-id="770e8-116">Тип</span><span class="sxs-lookup"><span data-stu-id="770e8-116">Type</span></span>                                                                                              | <span data-ttu-id="770e8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="770e8-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="770e8-118">**алловхардтерминате**</span><span class="sxs-lookup"><span data-stu-id="770e8-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="770e8-119">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-119">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-120">Указывает, что задачу можно завершить с помощью Терминатепроцесс.</span><span class="sxs-lookup"><span data-stu-id="770e8-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="770e8-121">**алловстартондеманд**</span><span class="sxs-lookup"><span data-stu-id="770e8-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="770e8-122">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-122">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-123">Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="770e8-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="770e8-124">**делетикспиредтаскафтер**</span><span class="sxs-lookup"><span data-stu-id="770e8-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="770e8-125">длительность</span><span class="sxs-lookup"><span data-stu-id="770e8-125">duration</span></span>                                                                                          | <span data-ttu-id="770e8-126">Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.</span><span class="sxs-lookup"><span data-stu-id="770e8-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="770e8-127">**дисалловстартифонбаттериес**</span><span class="sxs-lookup"><span data-stu-id="770e8-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="770e8-128">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-128">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-129">Указывает, что задача не будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="770e8-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="770e8-130">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="770e8-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="770e8-131">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-131">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-132">Указывает, что задача включена.</span><span class="sxs-lookup"><span data-stu-id="770e8-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="770e8-133">Задачу можно выполнить, только если этот параметр имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="770e8-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="770e8-134">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="770e8-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="770e8-135">длительность</span><span class="sxs-lookup"><span data-stu-id="770e8-135">duration</span></span>                                                                                          | <span data-ttu-id="770e8-136">Количество времени, отведенное на выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="770e8-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="770e8-137">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="770e8-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="770e8-138">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-138">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-139">Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="770e8-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="770e8-140">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="770e8-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="770e8-141">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="770e8-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="770e8-142">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="770e8-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="770e8-143">**маинтенанцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="770e8-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="770e8-144">**маинтенанцесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="770e8-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="770e8-145">Указывает, как планировщик задач выполняет задачи во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="770e8-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="770e8-146">**мултиплеинстанцесполици**</span><span class="sxs-lookup"><span data-stu-id="770e8-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="770e8-147">**мултиплеинстанцесполицитипе**</span><span class="sxs-lookup"><span data-stu-id="770e8-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="770e8-148">Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.</span><span class="sxs-lookup"><span data-stu-id="770e8-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="770e8-149">**Priority**</span><span class="sxs-lookup"><span data-stu-id="770e8-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="770e8-150">**приорититипе**</span><span class="sxs-lookup"><span data-stu-id="770e8-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="770e8-151">Задает уровень приоритета для задачи.</span><span class="sxs-lookup"><span data-stu-id="770e8-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="770e8-152">**рестартонфаилуре**</span><span class="sxs-lookup"><span data-stu-id="770e8-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="770e8-153">**рестарттипе**</span><span class="sxs-lookup"><span data-stu-id="770e8-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="770e8-154">Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.</span><span class="sxs-lookup"><span data-stu-id="770e8-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="770e8-155">**рунонлифидле**</span><span class="sxs-lookup"><span data-stu-id="770e8-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="770e8-156">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-156">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-157">Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="770e8-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="770e8-158">**рунонлифнетворкаваилабле**</span><span class="sxs-lookup"><span data-stu-id="770e8-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="770e8-159">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-159">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-160">Указывает, что планировщик задач будет выполнять задачу только при доступности сети.</span><span class="sxs-lookup"><span data-stu-id="770e8-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="770e8-161">**стартвхенаваилабле**</span><span class="sxs-lookup"><span data-stu-id="770e8-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="770e8-162">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-162">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-163">Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="770e8-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="770e8-164">**Стопифгоингонбаттериес (Сеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="770e8-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="770e8-165">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-165">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-166">Указывает, что задача будет остановлена при переходе компьютера на питание.</span><span class="sxs-lookup"><span data-stu-id="770e8-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="770e8-167">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="770e8-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="770e8-168">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-168">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-169">Указывает, будет ли задача автоматически отключена планировщик задач при запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="770e8-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="770e8-170">**Вакеторун (Сеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="770e8-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="770e8-171">Логическое</span><span class="sxs-lookup"><span data-stu-id="770e8-171">boolean</span></span>                                                                                           | <span data-ttu-id="770e8-172">Указывает, что планировщик задач будет выводить компьютер из спящего режима во время выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="770e8-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="770e8-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="770e8-173">Remarks</span></span>

<span data-ttu-id="770e8-174">Можно выбрать один или несколько дочерних элементов, указанных выше.</span><span class="sxs-lookup"><span data-stu-id="770e8-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="770e8-175">Для разработки на C++ сведения о регистрации задачи указываются с помощью [**Свойства Settings объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span><span class="sxs-lookup"><span data-stu-id="770e8-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="770e8-176">Для разработки сценариев сведения о регистрации задачи указываются с помощью свойства [**таскдефинитион. Settings**](taskdefinition-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="770e8-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="770e8-177">Примеры</span><span class="sxs-lookup"><span data-stu-id="770e8-177">Examples</span></span>

<span data-ttu-id="770e8-178">В следующем примере кода XML определяется элемент Settings, позволяющий жестко завершить задачу.</span><span class="sxs-lookup"><span data-stu-id="770e8-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="770e8-179">Дополнительные сведения и полный пример XML для настройки параметров задачи см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="770e8-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="770e8-180">Требования</span><span class="sxs-lookup"><span data-stu-id="770e8-180">Requirements</span></span>



| <span data-ttu-id="770e8-181">Требование</span><span class="sxs-lookup"><span data-stu-id="770e8-181">Requirement</span></span> | <span data-ttu-id="770e8-182">Значение</span><span class="sxs-lookup"><span data-stu-id="770e8-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="770e8-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="770e8-183">Minimum supported client</span></span><br/> | <span data-ttu-id="770e8-184">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="770e8-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="770e8-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="770e8-185">Minimum supported server</span></span><br/> | <span data-ttu-id="770e8-186">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="770e8-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="770e8-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="770e8-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770e8-188">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="770e8-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="770e8-189">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="770e8-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





