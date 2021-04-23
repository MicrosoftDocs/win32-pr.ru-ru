---
title: Монслидовтригжер. DaysOfWeek, свойство
description: Для сценариев Возвращает или задает дни недели, в которые выполняется задача.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- планировщик задач свойства DaysOfWeek
- Планировщик задач свойства DaysOfWeek, объект Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, свойство DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492309"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="8a892-106">Монслидовтригжер. DaysOfWeek, свойство</span><span class="sxs-lookup"><span data-stu-id="8a892-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="8a892-107">Для сценариев Возвращает или задает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="8a892-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a892-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a892-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="8a892-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8a892-109">Property value</span></span>

<span data-ttu-id="8a892-110">Битовая маска, указывающая дни недели, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="8a892-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a892-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a892-111">Remarks</span></span>

<span data-ttu-id="8a892-112">В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.</span><span class="sxs-lookup"><span data-stu-id="8a892-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="8a892-113">День недели</span><span class="sxs-lookup"><span data-stu-id="8a892-113">Day of Week</span></span> | <span data-ttu-id="8a892-114">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="8a892-114">Hex Value</span></span> | <span data-ttu-id="8a892-115">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="8a892-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="8a892-116">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="8a892-116">Sunday</span></span>      | <span data-ttu-id="8a892-117">0x01</span><span class="sxs-lookup"><span data-stu-id="8a892-117">0x01</span></span>      | <span data-ttu-id="8a892-118">1</span><span class="sxs-lookup"><span data-stu-id="8a892-118">1</span></span>             |
| <span data-ttu-id="8a892-119">Понедельник</span><span class="sxs-lookup"><span data-stu-id="8a892-119">Monday</span></span>      | <span data-ttu-id="8a892-120">0x02</span><span class="sxs-lookup"><span data-stu-id="8a892-120">0x02</span></span>      | <span data-ttu-id="8a892-121">2</span><span class="sxs-lookup"><span data-stu-id="8a892-121">2</span></span>             |
| <span data-ttu-id="8a892-122">Вторник</span><span class="sxs-lookup"><span data-stu-id="8a892-122">Tuesday</span></span>     | <span data-ttu-id="8a892-123">0x04</span><span class="sxs-lookup"><span data-stu-id="8a892-123">0x04</span></span>      | <span data-ttu-id="8a892-124">4</span><span class="sxs-lookup"><span data-stu-id="8a892-124">4</span></span>             |
| <span data-ttu-id="8a892-125">Среда</span><span class="sxs-lookup"><span data-stu-id="8a892-125">Wednesday</span></span>   | <span data-ttu-id="8a892-126">0x08</span><span class="sxs-lookup"><span data-stu-id="8a892-126">0x08</span></span>      | <span data-ttu-id="8a892-127">8</span><span class="sxs-lookup"><span data-stu-id="8a892-127">8</span></span>             |
| <span data-ttu-id="8a892-128">Четверг</span><span class="sxs-lookup"><span data-stu-id="8a892-128">Thursday</span></span>    | <span data-ttu-id="8a892-129">0x10</span><span class="sxs-lookup"><span data-stu-id="8a892-129">0x10</span></span>      | <span data-ttu-id="8a892-130">16</span><span class="sxs-lookup"><span data-stu-id="8a892-130">16</span></span>            |
| <span data-ttu-id="8a892-131">Пятница</span><span class="sxs-lookup"><span data-stu-id="8a892-131">Friday</span></span>      | <span data-ttu-id="8a892-132">0x20</span><span class="sxs-lookup"><span data-stu-id="8a892-132">0x20</span></span>      | <span data-ttu-id="8a892-133">32</span><span class="sxs-lookup"><span data-stu-id="8a892-133">32</span></span>            |
| <span data-ttu-id="8a892-134">Суббота</span><span class="sxs-lookup"><span data-stu-id="8a892-134">Saturday</span></span>    | <span data-ttu-id="8a892-135">0x40</span><span class="sxs-lookup"><span data-stu-id="8a892-135">0x40</span></span>      | <span data-ttu-id="8a892-136">64</span><span class="sxs-lookup"><span data-stu-id="8a892-136">64</span></span>            |



 

<span data-ttu-id="8a892-137">При чтении или записи XML для задачи дни недели месячного дня недели задаются элементом [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a892-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a892-138">Требования</span><span class="sxs-lookup"><span data-stu-id="8a892-138">Requirements</span></span>



| <span data-ttu-id="8a892-139">Требование</span><span class="sxs-lookup"><span data-stu-id="8a892-139">Requirement</span></span> | <span data-ttu-id="8a892-140">Значение</span><span class="sxs-lookup"><span data-stu-id="8a892-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a892-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a892-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8a892-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a892-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8a892-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a892-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8a892-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a892-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a892-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8a892-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a892-146"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a892-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a892-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8a892-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a892-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a892-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a892-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a892-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a892-150">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="8a892-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="8a892-151">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8a892-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





