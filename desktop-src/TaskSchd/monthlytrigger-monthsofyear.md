---
title: Монслитригжер. Монссофеар, свойство
description: Для сценариев Возвращает или задает месяцы года, в течение которых выполняется задача. | Монслитригжер. Монссофеар, свойство
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- планировщик задач свойства Монссофеар
- Планировщик задач свойства Монссофеар, объект Монслитригжер
- Планировщик задач объекта Монслитригжер, свойство Монссофеар
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914496"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="40905-107">Монслитригжер. Монссофеар, свойство</span><span class="sxs-lookup"><span data-stu-id="40905-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="40905-108">Для сценариев Возвращает или задает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="40905-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="40905-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40905-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="40905-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="40905-110">Property value</span></span>

<span data-ttu-id="40905-111">Битовая маска, указывающая месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="40905-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="40905-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40905-112">Remarks</span></span>

<span data-ttu-id="40905-113">В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.</span><span class="sxs-lookup"><span data-stu-id="40905-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="40905-114">Месяц</span><span class="sxs-lookup"><span data-stu-id="40905-114">Month</span></span>     | <span data-ttu-id="40905-115">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="40905-115">Hex value</span></span> | <span data-ttu-id="40905-116">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="40905-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="40905-117">Январь</span><span class="sxs-lookup"><span data-stu-id="40905-117">January</span></span>   | <span data-ttu-id="40905-118">0X01</span><span class="sxs-lookup"><span data-stu-id="40905-118">0X01</span></span>      | <span data-ttu-id="40905-119">1</span><span class="sxs-lookup"><span data-stu-id="40905-119">1</span></span>             |
| <span data-ttu-id="40905-120">Февраль</span><span class="sxs-lookup"><span data-stu-id="40905-120">February</span></span>  | <span data-ttu-id="40905-121">0x02</span><span class="sxs-lookup"><span data-stu-id="40905-121">0x02</span></span>      | <span data-ttu-id="40905-122">2</span><span class="sxs-lookup"><span data-stu-id="40905-122">2</span></span>             |
| <span data-ttu-id="40905-123">Март</span><span class="sxs-lookup"><span data-stu-id="40905-123">March</span></span>     | <span data-ttu-id="40905-124">0X04</span><span class="sxs-lookup"><span data-stu-id="40905-124">0X04</span></span>      | <span data-ttu-id="40905-125">4</span><span class="sxs-lookup"><span data-stu-id="40905-125">4</span></span>             |
| <span data-ttu-id="40905-126">Апрель</span><span class="sxs-lookup"><span data-stu-id="40905-126">April</span></span>     | <span data-ttu-id="40905-127">0X08</span><span class="sxs-lookup"><span data-stu-id="40905-127">0X08</span></span>      | <span data-ttu-id="40905-128">8</span><span class="sxs-lookup"><span data-stu-id="40905-128">8</span></span>             |
| <span data-ttu-id="40905-129">Май</span><span class="sxs-lookup"><span data-stu-id="40905-129">May</span></span>       | <span data-ttu-id="40905-130">0X10</span><span class="sxs-lookup"><span data-stu-id="40905-130">0X10</span></span>      | <span data-ttu-id="40905-131">16</span><span class="sxs-lookup"><span data-stu-id="40905-131">16</span></span>            |
| <span data-ttu-id="40905-132">Июнь</span><span class="sxs-lookup"><span data-stu-id="40905-132">June</span></span>      | <span data-ttu-id="40905-133">0X20</span><span class="sxs-lookup"><span data-stu-id="40905-133">0X20</span></span>      | <span data-ttu-id="40905-134">32</span><span class="sxs-lookup"><span data-stu-id="40905-134">32</span></span>            |
| <span data-ttu-id="40905-135">Июль</span><span class="sxs-lookup"><span data-stu-id="40905-135">July</span></span>      | <span data-ttu-id="40905-136">0x40</span><span class="sxs-lookup"><span data-stu-id="40905-136">0x40</span></span>      | <span data-ttu-id="40905-137">64</span><span class="sxs-lookup"><span data-stu-id="40905-137">64</span></span>            |
| <span data-ttu-id="40905-138">Август</span><span class="sxs-lookup"><span data-stu-id="40905-138">August</span></span>    | <span data-ttu-id="40905-139">0X80</span><span class="sxs-lookup"><span data-stu-id="40905-139">0X80</span></span>      | <span data-ttu-id="40905-140">128</span><span class="sxs-lookup"><span data-stu-id="40905-140">128</span></span>           |
| <span data-ttu-id="40905-141">Сентябрь</span><span class="sxs-lookup"><span data-stu-id="40905-141">September</span></span> | <span data-ttu-id="40905-142">0X100</span><span class="sxs-lookup"><span data-stu-id="40905-142">0X100</span></span>     | <span data-ttu-id="40905-143">256</span><span class="sxs-lookup"><span data-stu-id="40905-143">256</span></span>           |
| <span data-ttu-id="40905-144">Октябрь</span><span class="sxs-lookup"><span data-stu-id="40905-144">October</span></span>   | <span data-ttu-id="40905-145">0X200</span><span class="sxs-lookup"><span data-stu-id="40905-145">0X200</span></span>     | <span data-ttu-id="40905-146">512</span><span class="sxs-lookup"><span data-stu-id="40905-146">512</span></span>           |
| <span data-ttu-id="40905-147">Ноябрь</span><span class="sxs-lookup"><span data-stu-id="40905-147">November</span></span>  | <span data-ttu-id="40905-148">0X400</span><span class="sxs-lookup"><span data-stu-id="40905-148">0X400</span></span>     | <span data-ttu-id="40905-149">1024</span><span class="sxs-lookup"><span data-stu-id="40905-149">1024</span></span>          |
| <span data-ttu-id="40905-150">Декабрь</span><span class="sxs-lookup"><span data-stu-id="40905-150">December</span></span>  | <span data-ttu-id="40905-151">0X800</span><span class="sxs-lookup"><span data-stu-id="40905-151">0X800</span></span>     | <span data-ttu-id="40905-152">2048</span><span class="sxs-lookup"><span data-stu-id="40905-152">2048</span></span>          |



 

<span data-ttu-id="40905-153">При чтении или записи собственного XML-кода для задачи месяцы года указываются с помощью элемента [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="40905-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="40905-154">Требования</span><span class="sxs-lookup"><span data-stu-id="40905-154">Requirements</span></span>



| <span data-ttu-id="40905-155">Требование</span><span class="sxs-lookup"><span data-stu-id="40905-155">Requirement</span></span> | <span data-ttu-id="40905-156">Значение</span><span class="sxs-lookup"><span data-stu-id="40905-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40905-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40905-157">Minimum supported client</span></span><br/> | <span data-ttu-id="40905-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40905-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="40905-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40905-159">Minimum supported server</span></span><br/> | <span data-ttu-id="40905-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40905-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40905-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="40905-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="40905-162"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40905-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40905-163">DLL</span><span class="sxs-lookup"><span data-stu-id="40905-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40905-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40905-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40905-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40905-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40905-166">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="40905-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="40905-167">**монслитригжер**</span><span class="sxs-lookup"><span data-stu-id="40905-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





