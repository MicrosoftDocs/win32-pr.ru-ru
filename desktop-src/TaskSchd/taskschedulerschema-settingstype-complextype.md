---
title: Сложный тип Сеттингстипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Settings (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- планировщик задач сложного типа Сеттингстипе
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681982"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="8d212-104">Сложный тип Сеттингстипе</span><span class="sxs-lookup"><span data-stu-id="8d212-104">settingsType Complex Type</span></span>

<span data-ttu-id="8d212-105">Определяет дочерние элементы и сведения о последовательности для элемента [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8d212-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8d212-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8d212-106">Child elements</span></span>



| <span data-ttu-id="8d212-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8d212-107">Element</span></span>                                                                                                             | <span data-ttu-id="8d212-108">Тип</span><span class="sxs-lookup"><span data-stu-id="8d212-108">Type</span></span>                                                                                              | <span data-ttu-id="8d212-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8d212-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d212-110">**алловхардтерминате**</span><span class="sxs-lookup"><span data-stu-id="8d212-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="8d212-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-111">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-112">Указывает, допускает ли служба планировщик задач жесткое завершение задачи.</span><span class="sxs-lookup"><span data-stu-id="8d212-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="8d212-113">**алловстартондеманд**</span><span class="sxs-lookup"><span data-stu-id="8d212-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="8d212-114">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-114">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-115">Указывает, что задачу можно запустить с помощью команды Run или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="8d212-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="8d212-116">**делетикспиредтаскафтер**</span><span class="sxs-lookup"><span data-stu-id="8d212-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="8d212-117">длительность</span><span class="sxs-lookup"><span data-stu-id="8d212-117">duration</span></span>                                                                                          | <span data-ttu-id="8d212-118">Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.</span><span class="sxs-lookup"><span data-stu-id="8d212-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="8d212-119">Если для этого элемента не указано значение, то служба планировщик задач не удалит задачу.</span><span class="sxs-lookup"><span data-stu-id="8d212-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="8d212-120">**дисалловстартифонбаттериес**</span><span class="sxs-lookup"><span data-stu-id="8d212-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="8d212-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-121">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-122">Указывает, что задача не будет запущена, если компьютер работает от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="8d212-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="8d212-123">**дисалловстартонремотеаппсессион**</span><span class="sxs-lookup"><span data-stu-id="8d212-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="8d212-124">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-124">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-125">Указывает, что задача не должна запускаться, если задача запускается в локально интегрированном сеансе с удаленными приложениями.</span><span class="sxs-lookup"><span data-stu-id="8d212-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="8d212-126">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="8d212-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="8d212-127">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-127">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-128">Указывает, что задача включена.</span><span class="sxs-lookup"><span data-stu-id="8d212-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="8d212-129">Задачу можно выполнить, только если этот параметр имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8d212-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="8d212-130">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="8d212-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="8d212-131">длительность</span><span class="sxs-lookup"><span data-stu-id="8d212-131">duration</span></span>                                                                                          | <span data-ttu-id="8d212-132">Указывает время, в течение которого может завершиться задача.</span><span class="sxs-lookup"><span data-stu-id="8d212-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="8d212-133">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="8d212-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="8d212-134">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-134">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-135">Указывает по умолчанию, что задача не будет отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d212-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="8d212-136">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="8d212-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="8d212-137">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="8d212-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="8d212-138">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="8d212-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="8d212-139">**мултиплеинстанцесполици**</span><span class="sxs-lookup"><span data-stu-id="8d212-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="8d212-140">**мултиплеинстанцесполицитипе**</span><span class="sxs-lookup"><span data-stu-id="8d212-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="8d212-141">Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.</span><span class="sxs-lookup"><span data-stu-id="8d212-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="8d212-142">**нетворкпрофиленаме**</span><span class="sxs-lookup"><span data-stu-id="8d212-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="8d212-143">строка</span><span class="sxs-lookup"><span data-stu-id="8d212-143">string</span></span>                                                                                            | <span data-ttu-id="8d212-144">Указывает имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8d212-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="8d212-145">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="8d212-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="8d212-146">Имя используется в целях показа.</span><span class="sxs-lookup"><span data-stu-id="8d212-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="8d212-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="8d212-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="8d212-148">**нетворксеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="8d212-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="8d212-149">Указывает параметры, используемые службой планировщик задач для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8d212-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="8d212-150">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="8d212-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="8d212-151">**Priority**</span><span class="sxs-lookup"><span data-stu-id="8d212-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="8d212-152">**приорититипе**</span><span class="sxs-lookup"><span data-stu-id="8d212-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="8d212-153">Задает уровень приоритета для задачи.</span><span class="sxs-lookup"><span data-stu-id="8d212-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="8d212-154">**рестартонфаилуре**</span><span class="sxs-lookup"><span data-stu-id="8d212-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="8d212-155">**рестарттипе**</span><span class="sxs-lookup"><span data-stu-id="8d212-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="8d212-156">Указывает, что планировщик задач попытается перезапустить задачу по какой либо причине по ошибке.</span><span class="sxs-lookup"><span data-stu-id="8d212-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="8d212-157">**рунонлифидле**</span><span class="sxs-lookup"><span data-stu-id="8d212-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="8d212-158">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-158">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-159">Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="8d212-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="8d212-160">**рунонлифнетворкаваилабле**</span><span class="sxs-lookup"><span data-stu-id="8d212-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="8d212-161">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-161">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-162">Указывает, что планировщик задач будет выполнять задачу только при доступности сети.</span><span class="sxs-lookup"><span data-stu-id="8d212-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="8d212-163">**стартвхенаваилабле**</span><span class="sxs-lookup"><span data-stu-id="8d212-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="8d212-164">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-164">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-165">Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="8d212-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="8d212-166">**стопифгоингонбаттериес**</span><span class="sxs-lookup"><span data-stu-id="8d212-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="8d212-167">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-167">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-168">Указывает, что задача будет остановлена, если компьютер переключается на питание от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="8d212-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="8d212-169">**усеунифиедсчедулинженгине**</span><span class="sxs-lookup"><span data-stu-id="8d212-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="8d212-170">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-170">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-171">Указывает, что задача выполняется с помощью единого механизма планирования.</span><span class="sxs-lookup"><span data-stu-id="8d212-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="8d212-172">**вакеторун**</span><span class="sxs-lookup"><span data-stu-id="8d212-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="8d212-173">Логическое</span><span class="sxs-lookup"><span data-stu-id="8d212-173">boolean</span></span>                                                                                           | <span data-ttu-id="8d212-174">Указывает, что планировщик задач будет выводить компьютер из спящего режима перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="8d212-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="8d212-175">Требования</span><span class="sxs-lookup"><span data-stu-id="8d212-175">Requirements</span></span>



| <span data-ttu-id="8d212-176">Требование</span><span class="sxs-lookup"><span data-stu-id="8d212-176">Requirement</span></span> | <span data-ttu-id="8d212-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8d212-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8d212-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d212-178">Minimum supported client</span></span><br/> | <span data-ttu-id="8d212-179">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d212-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8d212-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d212-180">Minimum supported server</span></span><br/> | <span data-ttu-id="8d212-181">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d212-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d212-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d212-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d212-183">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="8d212-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8d212-184">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8d212-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





