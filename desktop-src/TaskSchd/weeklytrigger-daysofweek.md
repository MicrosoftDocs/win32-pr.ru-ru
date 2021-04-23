---
title: Виклитригжер. DaysOfWeek, свойство
description: Для сценариев Возвращает или задает дни недели, в которые выполняется задача.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- планировщик задач свойства DaysOfWeek
- Планировщик задач свойства DaysOfWeek, объект Виклитригжер
- Планировщик задач объекта Виклитригжер, свойство DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535591"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="ed94e-106">Виклитригжер. DaysOfWeek, свойство</span><span class="sxs-lookup"><span data-stu-id="ed94e-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="ed94e-107">Для сценариев Возвращает или задает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="ed94e-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed94e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed94e-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="ed94e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ed94e-109">Property value</span></span>

<span data-ttu-id="ed94e-110">Битовая маска, указывающая дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="ed94e-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed94e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed94e-111">Remarks</span></span>

<span data-ttu-id="ed94e-112">В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.</span><span class="sxs-lookup"><span data-stu-id="ed94e-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="ed94e-113">Месяц</span><span class="sxs-lookup"><span data-stu-id="ed94e-113">Month</span></span>     | <span data-ttu-id="ed94e-114">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="ed94e-114">Hex value</span></span> | <span data-ttu-id="ed94e-115">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="ed94e-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="ed94e-116">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="ed94e-116">Sunday</span></span>    | <span data-ttu-id="ed94e-117">0X01</span><span class="sxs-lookup"><span data-stu-id="ed94e-117">0X01</span></span>      | <span data-ttu-id="ed94e-118">1</span><span class="sxs-lookup"><span data-stu-id="ed94e-118">1</span></span>             |
| <span data-ttu-id="ed94e-119">Понедельник</span><span class="sxs-lookup"><span data-stu-id="ed94e-119">Monday</span></span>    | <span data-ttu-id="ed94e-120">0x02</span><span class="sxs-lookup"><span data-stu-id="ed94e-120">0x02</span></span>      | <span data-ttu-id="ed94e-121">2</span><span class="sxs-lookup"><span data-stu-id="ed94e-121">2</span></span>             |
| <span data-ttu-id="ed94e-122">Вторник</span><span class="sxs-lookup"><span data-stu-id="ed94e-122">Tuesday</span></span>   | <span data-ttu-id="ed94e-123">0X04</span><span class="sxs-lookup"><span data-stu-id="ed94e-123">0X04</span></span>      | <span data-ttu-id="ed94e-124">4</span><span class="sxs-lookup"><span data-stu-id="ed94e-124">4</span></span>             |
| <span data-ttu-id="ed94e-125">Среда</span><span class="sxs-lookup"><span data-stu-id="ed94e-125">Wednesday</span></span> | <span data-ttu-id="ed94e-126">0X08</span><span class="sxs-lookup"><span data-stu-id="ed94e-126">0X08</span></span>      | <span data-ttu-id="ed94e-127">8</span><span class="sxs-lookup"><span data-stu-id="ed94e-127">8</span></span>             |
| <span data-ttu-id="ed94e-128">Четверг</span><span class="sxs-lookup"><span data-stu-id="ed94e-128">Thursday</span></span>  | <span data-ttu-id="ed94e-129">0X10</span><span class="sxs-lookup"><span data-stu-id="ed94e-129">0X10</span></span>      | <span data-ttu-id="ed94e-130">16</span><span class="sxs-lookup"><span data-stu-id="ed94e-130">16</span></span>            |
| <span data-ttu-id="ed94e-131">Пятница</span><span class="sxs-lookup"><span data-stu-id="ed94e-131">Friday</span></span>    | <span data-ttu-id="ed94e-132">0x20</span><span class="sxs-lookup"><span data-stu-id="ed94e-132">0x20</span></span>      | <span data-ttu-id="ed94e-133">32</span><span class="sxs-lookup"><span data-stu-id="ed94e-133">32</span></span>            |
| <span data-ttu-id="ed94e-134">Суббота</span><span class="sxs-lookup"><span data-stu-id="ed94e-134">Saturday</span></span>  | <span data-ttu-id="ed94e-135">0X40</span><span class="sxs-lookup"><span data-stu-id="ed94e-135">0X40</span></span>      | <span data-ttu-id="ed94e-136">64</span><span class="sxs-lookup"><span data-stu-id="ed94e-136">64</span></span>            |



 

<span data-ttu-id="ed94e-137">При чтении или записи собственного XML-кода для задачи дни недели указываются с помощью элемента [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ed94e-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed94e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="ed94e-138">Requirements</span></span>



| <span data-ttu-id="ed94e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="ed94e-139">Requirement</span></span> | <span data-ttu-id="ed94e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="ed94e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed94e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed94e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ed94e-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed94e-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ed94e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed94e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ed94e-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed94e-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed94e-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ed94e-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed94e-146"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ed94e-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ed94e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ed94e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed94e-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed94e-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed94e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed94e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed94e-150">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ed94e-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





