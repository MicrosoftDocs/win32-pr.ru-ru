---
title: Идлесеттингс (Сеттингстипе), элемент
description: Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- планировщик задач элемента Идлесеттингс
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136926"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="704d6-104">Идлесеттингс (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="704d6-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="704d6-105">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="704d6-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="704d6-106">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="704d6-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="704d6-107">Элемент **идлесеттингс** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="704d6-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="704d6-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="704d6-108">Parent element</span></span>

| <span data-ttu-id="704d6-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="704d6-109">Element</span></span>                                                           | <span data-ttu-id="704d6-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="704d6-110">Derived from</span></span>                                                         | <span data-ttu-id="704d6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="704d6-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="704d6-112">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="704d6-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="704d6-113">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="704d6-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="704d6-114">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="704d6-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="704d6-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="704d6-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="704d6-116">Параметры *Duration* и *ваиттимеаут* являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="704d6-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="704d6-117">Они по-прежнему находятся в пользовательском интерфейсе планировщик задач, а методы интерфейса по-прежнему могут возвращать допустимые значения, но они больше не используются.</span><span class="sxs-lookup"><span data-stu-id="704d6-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="704d6-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="704d6-118">Element</span></span>                                                                                  | <span data-ttu-id="704d6-119">Тип</span><span class="sxs-lookup"><span data-stu-id="704d6-119">Type</span></span>     | <span data-ttu-id="704d6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="704d6-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="704d6-121">**рестартонидле**</span><span class="sxs-lookup"><span data-stu-id="704d6-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="704d6-122">Логическое</span><span class="sxs-lookup"><span data-stu-id="704d6-122">boolean</span></span>  | <span data-ttu-id="704d6-123">Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="704d6-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="704d6-124">**стопонидлинд**</span><span class="sxs-lookup"><span data-stu-id="704d6-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="704d6-125">Логическое</span><span class="sxs-lookup"><span data-stu-id="704d6-125">boolean</span></span>  | <span data-ttu-id="704d6-126">Указывает, что планировщик задач будет прекращать выполнение задачи, если условие простоя заканчивается до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="704d6-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="704d6-127">**Устарело**: [ **Продолжительность**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="704d6-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="704d6-128">длительность</span><span class="sxs-lookup"><span data-stu-id="704d6-128">duration</span></span> | <span data-ttu-id="704d6-129">Указывает, как долго компьютер должен находиться в состоянии простоя перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="704d6-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="704d6-130">Не **рекомендуется**: [ **ваиттимеаут**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="704d6-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="704d6-131">длительность</span><span class="sxs-lookup"><span data-stu-id="704d6-131">duration</span></span> | <span data-ttu-id="704d6-132">Указывает период времени, в течение которого планировщик задач будет ожидать наступления условия простоя.</span><span class="sxs-lookup"><span data-stu-id="704d6-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="704d6-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="704d6-133">Remarks</span></span>

<span data-ttu-id="704d6-134">Для разработки скриптов параметры простоя указываются с помощью свойства [**тасксеттингс. идлесеттингс**](tasksettings-idlesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="704d6-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="704d6-135">Для разработки на C++ параметры простоя указываются с помощью свойства [**итасксеттингс:: идлесеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .</span><span class="sxs-lookup"><span data-stu-id="704d6-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="704d6-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="704d6-136">Examples</span></span>

<span data-ttu-id="704d6-137">Следующий XML-код определяет элемент Settings, позволяющий планировщик задач ожидать 24 часа в течение неактивного состояния, а затем допускает запуск задачи только через 10 минут {Идледуратион).</span><span class="sxs-lookup"><span data-stu-id="704d6-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="704d6-138">Требования</span><span class="sxs-lookup"><span data-stu-id="704d6-138">Requirements</span></span>

| <span data-ttu-id="704d6-139">Требование</span><span class="sxs-lookup"><span data-stu-id="704d6-139">Requirement</span></span> | <span data-ttu-id="704d6-140">Значение</span><span class="sxs-lookup"><span data-stu-id="704d6-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="704d6-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="704d6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="704d6-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="704d6-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="704d6-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="704d6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="704d6-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="704d6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="704d6-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="704d6-145">See also</span></span>

[<span data-ttu-id="704d6-146">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="704d6-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="704d6-147">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="704d6-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
