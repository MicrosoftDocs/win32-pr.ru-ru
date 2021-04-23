---
title: Монслидовтригжер. Монссофеар, свойство
description: Для сценариев Возвращает или задает месяцы года, в течение которых выполняется задача. | Монслидовтригжер. Монссофеар, свойство
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- планировщик задач свойства Монссофеар
- Планировщик задач свойства Монссофеар, объект Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, свойство Монссофеар
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914596"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="afa37-107">Монслидовтригжер. Монссофеар, свойство</span><span class="sxs-lookup"><span data-stu-id="afa37-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="afa37-108">Для сценариев Возвращает или задает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="afa37-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa37-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afa37-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="afa37-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="afa37-110">Property value</span></span>

<span data-ttu-id="afa37-111">Битовая маска, указывающая месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="afa37-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="afa37-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afa37-112">Remarks</span></span>

<span data-ttu-id="afa37-113">В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.</span><span class="sxs-lookup"><span data-stu-id="afa37-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="afa37-114">Месяц</span><span class="sxs-lookup"><span data-stu-id="afa37-114">Month</span></span>     | <span data-ttu-id="afa37-115">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="afa37-115">Hex value</span></span> | <span data-ttu-id="afa37-116">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="afa37-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="afa37-117">Январь</span><span class="sxs-lookup"><span data-stu-id="afa37-117">January</span></span>   | <span data-ttu-id="afa37-118">0X01</span><span class="sxs-lookup"><span data-stu-id="afa37-118">0X01</span></span>      | <span data-ttu-id="afa37-119">1</span><span class="sxs-lookup"><span data-stu-id="afa37-119">1</span></span>             |
| <span data-ttu-id="afa37-120">Февраль</span><span class="sxs-lookup"><span data-stu-id="afa37-120">February</span></span>  | <span data-ttu-id="afa37-121">0x02</span><span class="sxs-lookup"><span data-stu-id="afa37-121">0x02</span></span>      | <span data-ttu-id="afa37-122">2</span><span class="sxs-lookup"><span data-stu-id="afa37-122">2</span></span>             |
| <span data-ttu-id="afa37-123">Март</span><span class="sxs-lookup"><span data-stu-id="afa37-123">March</span></span>     | <span data-ttu-id="afa37-124">0X04</span><span class="sxs-lookup"><span data-stu-id="afa37-124">0X04</span></span>      | <span data-ttu-id="afa37-125">4</span><span class="sxs-lookup"><span data-stu-id="afa37-125">4</span></span>             |
| <span data-ttu-id="afa37-126">Апрель</span><span class="sxs-lookup"><span data-stu-id="afa37-126">April</span></span>     | <span data-ttu-id="afa37-127">0X08</span><span class="sxs-lookup"><span data-stu-id="afa37-127">0X08</span></span>      | <span data-ttu-id="afa37-128">8</span><span class="sxs-lookup"><span data-stu-id="afa37-128">8</span></span>             |
| <span data-ttu-id="afa37-129">Май</span><span class="sxs-lookup"><span data-stu-id="afa37-129">May</span></span>       | <span data-ttu-id="afa37-130">0X10</span><span class="sxs-lookup"><span data-stu-id="afa37-130">0X10</span></span>      | <span data-ttu-id="afa37-131">16</span><span class="sxs-lookup"><span data-stu-id="afa37-131">16</span></span>            |
| <span data-ttu-id="afa37-132">Июнь</span><span class="sxs-lookup"><span data-stu-id="afa37-132">June</span></span>      | <span data-ttu-id="afa37-133">0X20</span><span class="sxs-lookup"><span data-stu-id="afa37-133">0X20</span></span>      | <span data-ttu-id="afa37-134">32</span><span class="sxs-lookup"><span data-stu-id="afa37-134">32</span></span>            |
| <span data-ttu-id="afa37-135">Июль</span><span class="sxs-lookup"><span data-stu-id="afa37-135">July</span></span>      | <span data-ttu-id="afa37-136">0x40</span><span class="sxs-lookup"><span data-stu-id="afa37-136">0x40</span></span>      | <span data-ttu-id="afa37-137">64</span><span class="sxs-lookup"><span data-stu-id="afa37-137">64</span></span>            |
| <span data-ttu-id="afa37-138">Август</span><span class="sxs-lookup"><span data-stu-id="afa37-138">August</span></span>    | <span data-ttu-id="afa37-139">0X80</span><span class="sxs-lookup"><span data-stu-id="afa37-139">0X80</span></span>      | <span data-ttu-id="afa37-140">128</span><span class="sxs-lookup"><span data-stu-id="afa37-140">128</span></span>           |
| <span data-ttu-id="afa37-141">Сентябрь</span><span class="sxs-lookup"><span data-stu-id="afa37-141">September</span></span> | <span data-ttu-id="afa37-142">0X100</span><span class="sxs-lookup"><span data-stu-id="afa37-142">0X100</span></span>     | <span data-ttu-id="afa37-143">256</span><span class="sxs-lookup"><span data-stu-id="afa37-143">256</span></span>           |
| <span data-ttu-id="afa37-144">Октябрь</span><span class="sxs-lookup"><span data-stu-id="afa37-144">October</span></span>   | <span data-ttu-id="afa37-145">0X200</span><span class="sxs-lookup"><span data-stu-id="afa37-145">0X200</span></span>     | <span data-ttu-id="afa37-146">512</span><span class="sxs-lookup"><span data-stu-id="afa37-146">512</span></span>           |
| <span data-ttu-id="afa37-147">Ноябрь</span><span class="sxs-lookup"><span data-stu-id="afa37-147">November</span></span>  | <span data-ttu-id="afa37-148">0X400</span><span class="sxs-lookup"><span data-stu-id="afa37-148">0X400</span></span>     | <span data-ttu-id="afa37-149">1024</span><span class="sxs-lookup"><span data-stu-id="afa37-149">1024</span></span>          |
| <span data-ttu-id="afa37-150">Декабрь</span><span class="sxs-lookup"><span data-stu-id="afa37-150">December</span></span>  | <span data-ttu-id="afa37-151">0X800</span><span class="sxs-lookup"><span data-stu-id="afa37-151">0X800</span></span>     | <span data-ttu-id="afa37-152">2048</span><span class="sxs-lookup"><span data-stu-id="afa37-152">2048</span></span>          |



 

<span data-ttu-id="afa37-153">При чтении или записи XML для задачи месяцы года месячного дня недели задаются элементом [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="afa37-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa37-154">Требования</span><span class="sxs-lookup"><span data-stu-id="afa37-154">Requirements</span></span>



| <span data-ttu-id="afa37-155">Требование</span><span class="sxs-lookup"><span data-stu-id="afa37-155">Requirement</span></span> | <span data-ttu-id="afa37-156">Значение</span><span class="sxs-lookup"><span data-stu-id="afa37-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afa37-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afa37-157">Minimum supported client</span></span><br/> | <span data-ttu-id="afa37-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afa37-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afa37-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afa37-159">Minimum supported server</span></span><br/> | <span data-ttu-id="afa37-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afa37-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afa37-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="afa37-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="afa37-162"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="afa37-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="afa37-163">DLL</span><span class="sxs-lookup"><span data-stu-id="afa37-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afa37-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afa37-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa37-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afa37-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa37-166">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="afa37-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="afa37-167">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="afa37-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





