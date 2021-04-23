---
title: Тасксеттингс. Priority, свойство
description: Для создания скриптов Возвращает или задает уровень приоритета задачи.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Свойство Priority планировщик задач
- Свойство Priority планировщик задач, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988290"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="1e8d9-106">Тасксеттингс. Priority, свойство</span><span class="sxs-lookup"><span data-stu-id="1e8d9-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="1e8d9-107">Для создания скриптов Возвращает или задает уровень приоритета задачи.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="1e8d9-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e8d9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e8d9-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="1e8d9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e8d9-110">Property value</span></span>

<span data-ttu-id="1e8d9-111">Уровень приоритета (0-10) задачи.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="1e8d9-112">Значение по умолчанию — 7.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e8d9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e8d9-113">Remarks</span></span>

<span data-ttu-id="1e8d9-114">Уровень приоритета 0 является наивысшим приоритетом, а уровень приоритета 10 — самым низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="1e8d9-115">По умолчанию используется значение 7.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-115">The default value is 7.</span></span> <span data-ttu-id="1e8d9-116">Уровни приоритета 7 и 8 используются для фоновых задач, а уровни приоритета 4, 5 и 6 используются для интерактивных задач.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="1e8d9-117">Действие задачи запускается в процессе с приоритетом, основанным на значении класса приоритета.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="1e8d9-118">Значение уровня приоритета (приоритет потока) используется для действий обработчика COM, окна сообщения и задач электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="1e8d9-119">Дополнительные сведения о классах приоритетов и значениях уровней приоритета см. в разделе [приоритеты планирования](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="1e8d9-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="1e8d9-120">В следующей таблице перечислены возможные значения для параметра *Priority* , а также соответствующие значения класса приоритета и уровня приоритета.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="1e8d9-121">*Приоритет* задачи</span><span class="sxs-lookup"><span data-stu-id="1e8d9-121">Task *priority*</span></span> | <span data-ttu-id="1e8d9-122">Класс Priority</span><span class="sxs-lookup"><span data-stu-id="1e8d9-122">Priority Class</span></span>                 | <span data-ttu-id="1e8d9-123">Уровень приоритета</span><span class="sxs-lookup"><span data-stu-id="1e8d9-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="1e8d9-124">0</span><span class="sxs-lookup"><span data-stu-id="1e8d9-124">0</span></span>               | <span data-ttu-id="1e8d9-125">\_класс приоритета в режиме реального времени \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="1e8d9-126">\_ \_ критическое время ПРИОРИТЕТа потока \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="1e8d9-127">1</span><span class="sxs-lookup"><span data-stu-id="1e8d9-127">1</span></span>               | <span data-ttu-id="1e8d9-128">класс с высоким \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="1e8d9-129">приоритет потока — \_ \_ самый высокий</span><span class="sxs-lookup"><span data-stu-id="1e8d9-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="1e8d9-130">2</span><span class="sxs-lookup"><span data-stu-id="1e8d9-130">2</span></span>               | <span data-ttu-id="1e8d9-131">ВЫШЕ \_ класса с нормальным \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="1e8d9-132">\_приоритет потока \_ выше \_ обычного</span><span class="sxs-lookup"><span data-stu-id="1e8d9-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="1e8d9-133">3</span><span class="sxs-lookup"><span data-stu-id="1e8d9-133">3</span></span>               | <span data-ttu-id="1e8d9-134">ВЫШЕ \_ класса с нормальным \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="1e8d9-135">\_приоритет потока \_ выше \_ обычного</span><span class="sxs-lookup"><span data-stu-id="1e8d9-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="1e8d9-136">4</span><span class="sxs-lookup"><span data-stu-id="1e8d9-136">4</span></span>               | <span data-ttu-id="1e8d9-137">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="1e8d9-138">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="1e8d9-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="1e8d9-139">5</span><span class="sxs-lookup"><span data-stu-id="1e8d9-139">5</span></span>               | <span data-ttu-id="1e8d9-140">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="1e8d9-141">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="1e8d9-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="1e8d9-142">6</span><span class="sxs-lookup"><span data-stu-id="1e8d9-142">6</span></span>               | <span data-ttu-id="1e8d9-143">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="1e8d9-144">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="1e8d9-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="1e8d9-145">7</span><span class="sxs-lookup"><span data-stu-id="1e8d9-145">7</span></span>               | <span data-ttu-id="1e8d9-146">НИЖЕ \_ обычного \_ класса приоритета \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="1e8d9-147">\_приоритет потока \_ ниже \_ обычного</span><span class="sxs-lookup"><span data-stu-id="1e8d9-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="1e8d9-148">8</span><span class="sxs-lookup"><span data-stu-id="1e8d9-148">8</span></span>               | <span data-ttu-id="1e8d9-149">НИЖЕ \_ обычного \_ класса приоритета \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="1e8d9-150">\_приоритет потока \_ ниже \_ обычного</span><span class="sxs-lookup"><span data-stu-id="1e8d9-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="1e8d9-151">9</span><span class="sxs-lookup"><span data-stu-id="1e8d9-151">9</span></span>               | <span data-ttu-id="1e8d9-152">\_класс приоритета простоя \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="1e8d9-153">\_ \_ самый низкий приоритет потока</span><span class="sxs-lookup"><span data-stu-id="1e8d9-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="1e8d9-154">10</span><span class="sxs-lookup"><span data-stu-id="1e8d9-154">10</span></span>              | <span data-ttu-id="1e8d9-155">\_класс приоритета простоя \_</span><span class="sxs-lookup"><span data-stu-id="1e8d9-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="1e8d9-156">приоритет потока — \_ \_ бездействие</span><span class="sxs-lookup"><span data-stu-id="1e8d9-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="1e8d9-157">При чтении или записи XML для задачи этот параметр указывается в элементе [**Priority (сеттингстипе)**](taskschedulerschema-priority-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="1e8d9-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e8d9-158">Требования</span><span class="sxs-lookup"><span data-stu-id="1e8d9-158">Requirements</span></span>



| <span data-ttu-id="1e8d9-159">Требование</span><span class="sxs-lookup"><span data-stu-id="1e8d9-159">Requirement</span></span> | <span data-ttu-id="1e8d9-160">Значение</span><span class="sxs-lookup"><span data-stu-id="1e8d9-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e8d9-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e8d9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="1e8d9-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e8d9-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1e8d9-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e8d9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="1e8d9-164">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e8d9-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e8d9-165">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1e8d9-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e8d9-166"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e8d9-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e8d9-167">DLL</span><span class="sxs-lookup"><span data-stu-id="1e8d9-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e8d9-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e8d9-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e8d9-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e8d9-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e8d9-170">**тасксеттингс**</span><span class="sxs-lookup"><span data-stu-id="1e8d9-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

