---
title: Объект Идлесеттингс
description: Объект скрипта, указывающий, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- планировщик задач объекта Идлесеттингс
- Планировщик задач объекта Идлесеттингс, описание
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415241"
---
# <a name="idlesettings-object"></a><span data-ttu-id="cdf39-105">Объект Идлесеттингс</span><span class="sxs-lookup"><span data-stu-id="cdf39-105">IdleSettings object</span></span>

<span data-ttu-id="cdf39-106">Объект скрипта, указывающий, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="cdf39-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="cdf39-107">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="cdf39-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="cdf39-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="cdf39-108">Members</span></span>

<span data-ttu-id="cdf39-109">Объект **идлесеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdf39-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="cdf39-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdf39-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdf39-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdf39-111">Properties</span></span>

<span data-ttu-id="cdf39-112">Объект **идлесеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cdf39-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="cdf39-113">Параметры *идледуратион* и *ваиттимеаут* являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="cdf39-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="cdf39-114">Они по-прежнему находятся в пользовательском интерфейсе планировщик задач, а методы интерфейса по-прежнему могут возвращать допустимые значения, но они больше не используются.</span><span class="sxs-lookup"><span data-stu-id="cdf39-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="cdf39-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="cdf39-115">Property</span></span>                                                       | <span data-ttu-id="cdf39-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="cdf39-116">Access type</span></span>           | <span data-ttu-id="cdf39-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cdf39-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdf39-118">**рестартонидле**</span><span class="sxs-lookup"><span data-stu-id="cdf39-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="cdf39-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cdf39-119">Read/write</span></span><br/> | <span data-ttu-id="cdf39-120">Возвращает или задает логическое значение, указывающее, перезапускается ли задача, когда компьютер циклически переключается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="cdf39-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="cdf39-121">**стопонидлинд**</span><span class="sxs-lookup"><span data-stu-id="cdf39-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="cdf39-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cdf39-122">Read/write</span></span><br/> | <span data-ttu-id="cdf39-123">Возвращает или задает логическое значение, указывающее, что планировщик задач будет завершать задачу, если условие простоя заканчивается до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="cdf39-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="cdf39-124">Не **рекомендуется**: [ **идледуратион**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="cdf39-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="cdf39-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cdf39-125">Read/write</span></span><br/> | <span data-ttu-id="cdf39-126">Возвращает или задает значение, указывающее период времени, в течение которого компьютер должен находиться в состоянии простоя перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="cdf39-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="cdf39-127">Не **рекомендуется**: [ **ваиттимеаут**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="cdf39-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="cdf39-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="cdf39-128">Read/write</span></span><br/> | <span data-ttu-id="cdf39-129">Возвращает или задает значение, указывающее время, в течение которого планировщик задач будет ожидать наступления условия простоя.</span><span class="sxs-lookup"><span data-stu-id="cdf39-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="cdf39-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdf39-130">Remarks</span></span>

<span data-ttu-id="cdf39-131">При чтении или записи XML для задачи этот параметр указывается в элементе [**идлесеттингс**](taskschedulerschema-idlesettings-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="cdf39-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="cdf39-132">Если задача запускается триггером Idle, свойство [**идлесеттингс. ваиттимеаут**](idlesettings-waittimeout.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cdf39-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="cdf39-133">*Идлесеттингс. идледуратион* и *идлесеттингс. ваиттимеаут* являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="cdf39-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf39-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cdf39-134">Requirements</span></span>

| <span data-ttu-id="cdf39-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cdf39-135">Requirement</span></span> | <span data-ttu-id="cdf39-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cdf39-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf39-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdf39-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf39-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdf39-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cdf39-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdf39-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf39-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdf39-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cdf39-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cdf39-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="cdf39-142"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cdf39-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cdf39-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf39-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf39-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf39-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="cdf39-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdf39-145">See also</span></span>

[<span data-ttu-id="cdf39-146">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="cdf39-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="cdf39-147">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cdf39-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
