---
title: Элемент Priority (Сеттингстипе)
description: Задает уровень приоритета для задачи.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Элемент Priority планировщик задач
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414973"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="9639f-104">Элемент Priority (Сеттингстипе)</span><span class="sxs-lookup"><span data-stu-id="9639f-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="9639f-105">Задает уровень приоритета для задачи.</span><span class="sxs-lookup"><span data-stu-id="9639f-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="9639f-106">Элемент **Priority** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9639f-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9639f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="9639f-107">Parent element</span></span>



| <span data-ttu-id="9639f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9639f-108">Element</span></span>                                                           | <span data-ttu-id="9639f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="9639f-109">Derived from</span></span>                                                         | <span data-ttu-id="9639f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9639f-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9639f-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="9639f-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="9639f-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="9639f-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="9639f-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="9639f-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9639f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9639f-114">Remarks</span></span>

<span data-ttu-id="9639f-115">Уровень приоритета 0 является наивысшим приоритетом, а уровень приоритета 10 — самым низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="9639f-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="9639f-116">По умолчанию используется значение 7.</span><span class="sxs-lookup"><span data-stu-id="9639f-116">The default value is 7.</span></span> <span data-ttu-id="9639f-117">Минимальное и максимальное значения задаются простым типом [**приорититипе**](taskschedulerschema-prioritytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="9639f-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="9639f-118">Уровни приоритета 7 и 8 используются для фоновых задач, а уровни приоритета 4, 5 и 6 используются для интерактивных задач.</span><span class="sxs-lookup"><span data-stu-id="9639f-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="9639f-119">Действие задачи запускается в процессе с приоритетом, основанным на значении класса приоритета.</span><span class="sxs-lookup"><span data-stu-id="9639f-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="9639f-120">Значение уровня приоритета (приоритет потока) используется для действий обработчика COM, окна сообщения и задач электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9639f-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="9639f-121">Дополнительные сведения о классах приоритетов и значениях уровней приоритета см. в разделе [приоритеты планирования](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="9639f-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="9639f-122">В следующей таблице перечислены возможные значения для элемента **Priority** , а также соответствующие значения класса приоритета и уровня приоритета.</span><span class="sxs-lookup"><span data-stu-id="9639f-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="9639f-123">Приоритет задачи</span><span class="sxs-lookup"><span data-stu-id="9639f-123">Task Priority</span></span> | <span data-ttu-id="9639f-124">Класс Priority</span><span class="sxs-lookup"><span data-stu-id="9639f-124">Priority Class</span></span>                 | <span data-ttu-id="9639f-125">Уровень приоритета</span><span class="sxs-lookup"><span data-stu-id="9639f-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="9639f-126">0</span><span class="sxs-lookup"><span data-stu-id="9639f-126">0</span></span>             | <span data-ttu-id="9639f-127">\_класс приоритета в режиме реального времени \_</span><span class="sxs-lookup"><span data-stu-id="9639f-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="9639f-128">\_ \_ критическое время ПРИОРИТЕТа потока \_</span><span class="sxs-lookup"><span data-stu-id="9639f-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="9639f-129">1</span><span class="sxs-lookup"><span data-stu-id="9639f-129">1</span></span>             | <span data-ttu-id="9639f-130">класс с высоким \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="9639f-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="9639f-131">приоритет потока — \_ \_ самый высокий</span><span class="sxs-lookup"><span data-stu-id="9639f-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="9639f-132">2</span><span class="sxs-lookup"><span data-stu-id="9639f-132">2</span></span>             | <span data-ttu-id="9639f-133">ВЫШЕ \_ класса с нормальным \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="9639f-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="9639f-134">\_приоритет потока \_ выше \_ обычного</span><span class="sxs-lookup"><span data-stu-id="9639f-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="9639f-135">3</span><span class="sxs-lookup"><span data-stu-id="9639f-135">3</span></span>             | <span data-ttu-id="9639f-136">ВЫШЕ \_ класса с нормальным \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="9639f-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="9639f-137">\_приоритет потока \_ выше \_ обычного</span><span class="sxs-lookup"><span data-stu-id="9639f-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="9639f-138">4</span><span class="sxs-lookup"><span data-stu-id="9639f-138">4</span></span>             | <span data-ttu-id="9639f-139">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="9639f-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="9639f-140">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="9639f-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="9639f-141">5</span><span class="sxs-lookup"><span data-stu-id="9639f-141">5</span></span>             | <span data-ttu-id="9639f-142">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="9639f-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="9639f-143">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="9639f-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="9639f-144">6</span><span class="sxs-lookup"><span data-stu-id="9639f-144">6</span></span>             | <span data-ttu-id="9639f-145">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="9639f-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="9639f-146">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="9639f-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="9639f-147">7</span><span class="sxs-lookup"><span data-stu-id="9639f-147">7</span></span>             | <span data-ttu-id="9639f-148">НИЖЕ \_ обычного \_ класса приоритета \_</span><span class="sxs-lookup"><span data-stu-id="9639f-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="9639f-149">\_приоритет потока \_ ниже \_ обычного</span><span class="sxs-lookup"><span data-stu-id="9639f-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="9639f-150">8</span><span class="sxs-lookup"><span data-stu-id="9639f-150">8</span></span>             | <span data-ttu-id="9639f-151">НИЖЕ \_ обычного \_ класса приоритета \_</span><span class="sxs-lookup"><span data-stu-id="9639f-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="9639f-152">\_приоритет потока \_ ниже \_ обычного</span><span class="sxs-lookup"><span data-stu-id="9639f-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="9639f-153">9</span><span class="sxs-lookup"><span data-stu-id="9639f-153">9</span></span>             | <span data-ttu-id="9639f-154">\_класс приоритета простоя \_</span><span class="sxs-lookup"><span data-stu-id="9639f-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="9639f-155">\_ \_ самый низкий приоритет потока</span><span class="sxs-lookup"><span data-stu-id="9639f-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="9639f-156">10</span><span class="sxs-lookup"><span data-stu-id="9639f-156">10</span></span>            | <span data-ttu-id="9639f-157">\_класс приоритета простоя \_</span><span class="sxs-lookup"><span data-stu-id="9639f-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="9639f-158">приоритет потока — \_ \_ бездействие</span><span class="sxs-lookup"><span data-stu-id="9639f-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="9639f-159">Сведения о разработке на языке C++ см. в разделе [**свойство Priority объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="9639f-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="9639f-160">Сведения о разработке сценариев см. в разделе [**тасксеттингс. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="9639f-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9639f-161">Требования</span><span class="sxs-lookup"><span data-stu-id="9639f-161">Requirements</span></span>



| <span data-ttu-id="9639f-162">Требование</span><span class="sxs-lookup"><span data-stu-id="9639f-162">Requirement</span></span> | <span data-ttu-id="9639f-163">Значение</span><span class="sxs-lookup"><span data-stu-id="9639f-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9639f-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9639f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9639f-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9639f-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9639f-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9639f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9639f-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9639f-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9639f-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9639f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9639f-169">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="9639f-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

