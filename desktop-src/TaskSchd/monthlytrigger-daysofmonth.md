---
title: Монслитригжер. DaysOfMonth, свойство
description: Для сценариев Возвращает или задает дни месяца, в которые выполняется задача.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- планировщик задач свойства DaysOfMonth
- Планировщик задач свойства DaysOfMonth, объект Монслитригжер
- Планировщик задач объекта Монслитригжер, свойство DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136351"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="05f03-106">Монслитригжер. DaysOfMonth, свойство</span><span class="sxs-lookup"><span data-stu-id="05f03-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="05f03-107">Для сценариев Возвращает или задает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="05f03-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f03-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05f03-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="05f03-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="05f03-109">Property value</span></span>

<span data-ttu-id="05f03-110">Битовая маска, указывающая дни месяца, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="05f03-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f03-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05f03-111">Remarks</span></span>



| <span data-ttu-id="05f03-112">День месяца</span><span class="sxs-lookup"><span data-stu-id="05f03-112">Day of month</span></span> | <span data-ttu-id="05f03-113">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="05f03-113">Hex value</span></span>  | <span data-ttu-id="05f03-114">Десятичное значение</span><span class="sxs-lookup"><span data-stu-id="05f03-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="05f03-115">1</span><span class="sxs-lookup"><span data-stu-id="05f03-115">1</span></span>            | <span data-ttu-id="05f03-116">0x01</span><span class="sxs-lookup"><span data-stu-id="05f03-116">0x01</span></span>       | <span data-ttu-id="05f03-117">1</span><span class="sxs-lookup"><span data-stu-id="05f03-117">1</span></span>             |
| <span data-ttu-id="05f03-118">2</span><span class="sxs-lookup"><span data-stu-id="05f03-118">2</span></span>            | <span data-ttu-id="05f03-119">0x02</span><span class="sxs-lookup"><span data-stu-id="05f03-119">0x02</span></span>       | <span data-ttu-id="05f03-120">2</span><span class="sxs-lookup"><span data-stu-id="05f03-120">2</span></span>             |
| <span data-ttu-id="05f03-121">3</span><span class="sxs-lookup"><span data-stu-id="05f03-121">3</span></span>            | <span data-ttu-id="05f03-122">0x04</span><span class="sxs-lookup"><span data-stu-id="05f03-122">0x04</span></span>       | <span data-ttu-id="05f03-123">4</span><span class="sxs-lookup"><span data-stu-id="05f03-123">4</span></span>             |
| <span data-ttu-id="05f03-124">4</span><span class="sxs-lookup"><span data-stu-id="05f03-124">4</span></span>            | <span data-ttu-id="05f03-125">0x08</span><span class="sxs-lookup"><span data-stu-id="05f03-125">0x08</span></span>       | <span data-ttu-id="05f03-126">8</span><span class="sxs-lookup"><span data-stu-id="05f03-126">8</span></span>             |
| <span data-ttu-id="05f03-127">5</span><span class="sxs-lookup"><span data-stu-id="05f03-127">5</span></span>            | <span data-ttu-id="05f03-128">0x10</span><span class="sxs-lookup"><span data-stu-id="05f03-128">0x10</span></span>       | <span data-ttu-id="05f03-129">16</span><span class="sxs-lookup"><span data-stu-id="05f03-129">16</span></span>            |
| <span data-ttu-id="05f03-130">6</span><span class="sxs-lookup"><span data-stu-id="05f03-130">6</span></span>            | <span data-ttu-id="05f03-131">0x20</span><span class="sxs-lookup"><span data-stu-id="05f03-131">0x20</span></span>       | <span data-ttu-id="05f03-132">32</span><span class="sxs-lookup"><span data-stu-id="05f03-132">32</span></span>            |
| <span data-ttu-id="05f03-133">7</span><span class="sxs-lookup"><span data-stu-id="05f03-133">7</span></span>            | <span data-ttu-id="05f03-134">0x40</span><span class="sxs-lookup"><span data-stu-id="05f03-134">0x40</span></span>       | <span data-ttu-id="05f03-135">64</span><span class="sxs-lookup"><span data-stu-id="05f03-135">64</span></span>            |
| <span data-ttu-id="05f03-136">8</span><span class="sxs-lookup"><span data-stu-id="05f03-136">8</span></span>            | <span data-ttu-id="05f03-137">0x80</span><span class="sxs-lookup"><span data-stu-id="05f03-137">0x80</span></span>       | <span data-ttu-id="05f03-138">128</span><span class="sxs-lookup"><span data-stu-id="05f03-138">128</span></span>           |
| <span data-ttu-id="05f03-139">9</span><span class="sxs-lookup"><span data-stu-id="05f03-139">9</span></span>            | <span data-ttu-id="05f03-140">0x100</span><span class="sxs-lookup"><span data-stu-id="05f03-140">0x100</span></span>      | <span data-ttu-id="05f03-141">256</span><span class="sxs-lookup"><span data-stu-id="05f03-141">256</span></span>           |
| <span data-ttu-id="05f03-142">10</span><span class="sxs-lookup"><span data-stu-id="05f03-142">10</span></span>           | <span data-ttu-id="05f03-143">0x200</span><span class="sxs-lookup"><span data-stu-id="05f03-143">0x200</span></span>      | <span data-ttu-id="05f03-144">512</span><span class="sxs-lookup"><span data-stu-id="05f03-144">512</span></span>           |
| <span data-ttu-id="05f03-145">11</span><span class="sxs-lookup"><span data-stu-id="05f03-145">11</span></span>           | <span data-ttu-id="05f03-146">0x400</span><span class="sxs-lookup"><span data-stu-id="05f03-146">0x400</span></span>      | <span data-ttu-id="05f03-147">1024</span><span class="sxs-lookup"><span data-stu-id="05f03-147">1024</span></span>          |
| <span data-ttu-id="05f03-148">12</span><span class="sxs-lookup"><span data-stu-id="05f03-148">12</span></span>           | <span data-ttu-id="05f03-149">0x800</span><span class="sxs-lookup"><span data-stu-id="05f03-149">0x800</span></span>      | <span data-ttu-id="05f03-150">2048</span><span class="sxs-lookup"><span data-stu-id="05f03-150">2048</span></span>          |
| <span data-ttu-id="05f03-151">13</span><span class="sxs-lookup"><span data-stu-id="05f03-151">13</span></span>           | <span data-ttu-id="05f03-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="05f03-152">0x1000</span></span>     | <span data-ttu-id="05f03-153">4096</span><span class="sxs-lookup"><span data-stu-id="05f03-153">4096</span></span>          |
| <span data-ttu-id="05f03-154">14</span><span class="sxs-lookup"><span data-stu-id="05f03-154">14</span></span>           | <span data-ttu-id="05f03-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="05f03-155">0x2000</span></span>     | <span data-ttu-id="05f03-156">8192</span><span class="sxs-lookup"><span data-stu-id="05f03-156">8192</span></span>          |
| <span data-ttu-id="05f03-157">15</span><span class="sxs-lookup"><span data-stu-id="05f03-157">15</span></span>           | <span data-ttu-id="05f03-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="05f03-158">0x4000</span></span>     | <span data-ttu-id="05f03-159">16384</span><span class="sxs-lookup"><span data-stu-id="05f03-159">16384</span></span>         |
| <span data-ttu-id="05f03-160">16</span><span class="sxs-lookup"><span data-stu-id="05f03-160">16</span></span>           | <span data-ttu-id="05f03-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="05f03-161">0x8000</span></span>     | <span data-ttu-id="05f03-162">32768</span><span class="sxs-lookup"><span data-stu-id="05f03-162">32768</span></span>         |
| <span data-ttu-id="05f03-163">17</span><span class="sxs-lookup"><span data-stu-id="05f03-163">17</span></span>           | <span data-ttu-id="05f03-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="05f03-164">0x10000</span></span>    | <span data-ttu-id="05f03-165">65536</span><span class="sxs-lookup"><span data-stu-id="05f03-165">65536</span></span>         |
| <span data-ttu-id="05f03-166">18</span><span class="sxs-lookup"><span data-stu-id="05f03-166">18</span></span>           | <span data-ttu-id="05f03-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="05f03-167">0x20000</span></span>    | <span data-ttu-id="05f03-168">131072</span><span class="sxs-lookup"><span data-stu-id="05f03-168">131072</span></span>        |
| <span data-ttu-id="05f03-169">19</span><span class="sxs-lookup"><span data-stu-id="05f03-169">19</span></span>           | <span data-ttu-id="05f03-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="05f03-170">0x40000</span></span>    | <span data-ttu-id="05f03-171">262144</span><span class="sxs-lookup"><span data-stu-id="05f03-171">262144</span></span>        |
| <span data-ttu-id="05f03-172">20</span><span class="sxs-lookup"><span data-stu-id="05f03-172">20</span></span>           | <span data-ttu-id="05f03-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="05f03-173">0x80000</span></span>    | <span data-ttu-id="05f03-174">524288</span><span class="sxs-lookup"><span data-stu-id="05f03-174">524288</span></span>        |
| <span data-ttu-id="05f03-175">21</span><span class="sxs-lookup"><span data-stu-id="05f03-175">21</span></span>           | <span data-ttu-id="05f03-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="05f03-176">0x100000</span></span>   | <span data-ttu-id="05f03-177">1048576</span><span class="sxs-lookup"><span data-stu-id="05f03-177">1048576</span></span>       |
| <span data-ttu-id="05f03-178">22</span><span class="sxs-lookup"><span data-stu-id="05f03-178">22</span></span>           | <span data-ttu-id="05f03-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="05f03-179">0x200000</span></span>   | <span data-ttu-id="05f03-180">2097152</span><span class="sxs-lookup"><span data-stu-id="05f03-180">2097152</span></span>       |
| <span data-ttu-id="05f03-181">23</span><span class="sxs-lookup"><span data-stu-id="05f03-181">23</span></span>           | <span data-ttu-id="05f03-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="05f03-182">0x400000</span></span>   | <span data-ttu-id="05f03-183">4194304</span><span class="sxs-lookup"><span data-stu-id="05f03-183">4194304</span></span>       |
| <span data-ttu-id="05f03-184">24</span><span class="sxs-lookup"><span data-stu-id="05f03-184">24</span></span>           | <span data-ttu-id="05f03-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="05f03-185">0x800000</span></span>   | <span data-ttu-id="05f03-186">8388608</span><span class="sxs-lookup"><span data-stu-id="05f03-186">8388608</span></span>       |
| <span data-ttu-id="05f03-187">25</span><span class="sxs-lookup"><span data-stu-id="05f03-187">25</span></span>           | <span data-ttu-id="05f03-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="05f03-188">0x1000000</span></span>  | <span data-ttu-id="05f03-189">16777216</span><span class="sxs-lookup"><span data-stu-id="05f03-189">16777216</span></span>      |
| <span data-ttu-id="05f03-190">26</span><span class="sxs-lookup"><span data-stu-id="05f03-190">26</span></span>           | <span data-ttu-id="05f03-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="05f03-191">0x2000000</span></span>  | <span data-ttu-id="05f03-192">33554432</span><span class="sxs-lookup"><span data-stu-id="05f03-192">33554432</span></span>      |
| <span data-ttu-id="05f03-193">27</span><span class="sxs-lookup"><span data-stu-id="05f03-193">27</span></span>           | <span data-ttu-id="05f03-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="05f03-194">0x4000000</span></span>  | <span data-ttu-id="05f03-195">67108864</span><span class="sxs-lookup"><span data-stu-id="05f03-195">67108864</span></span>      |
| <span data-ttu-id="05f03-196">28</span><span class="sxs-lookup"><span data-stu-id="05f03-196">28</span></span>           | <span data-ttu-id="05f03-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="05f03-197">0x8000000</span></span>  | <span data-ttu-id="05f03-198">134217728</span><span class="sxs-lookup"><span data-stu-id="05f03-198">134217728</span></span>     |
| <span data-ttu-id="05f03-199">29</span><span class="sxs-lookup"><span data-stu-id="05f03-199">29</span></span>           | <span data-ttu-id="05f03-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="05f03-200">0x10000000</span></span> | <span data-ttu-id="05f03-201">268435456</span><span class="sxs-lookup"><span data-stu-id="05f03-201">268435456</span></span>     |
| <span data-ttu-id="05f03-202">30</span><span class="sxs-lookup"><span data-stu-id="05f03-202">30</span></span>           | <span data-ttu-id="05f03-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="05f03-203">0x20000000</span></span> | <span data-ttu-id="05f03-204">536 870 912</span><span class="sxs-lookup"><span data-stu-id="05f03-204">536870912</span></span>     |
| <span data-ttu-id="05f03-205">31</span><span class="sxs-lookup"><span data-stu-id="05f03-205">31</span></span>           | <span data-ttu-id="05f03-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="05f03-206">0x40000000</span></span> | <span data-ttu-id="05f03-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="05f03-207">1073741824</span></span>    |
| <span data-ttu-id="05f03-208">Последний</span><span class="sxs-lookup"><span data-stu-id="05f03-208">Last</span></span>         | <span data-ttu-id="05f03-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="05f03-209">0x80000000</span></span> | <span data-ttu-id="05f03-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="05f03-210">2147483648</span></span>    |



 

<span data-ttu-id="05f03-211">При чтении или записи собственного XML-кода для задачи дни месяца указываются с помощью элемента [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="05f03-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f03-212">Требования</span><span class="sxs-lookup"><span data-stu-id="05f03-212">Requirements</span></span>



| <span data-ttu-id="05f03-213">Требование</span><span class="sxs-lookup"><span data-stu-id="05f03-213">Requirement</span></span> | <span data-ttu-id="05f03-214">Значение</span><span class="sxs-lookup"><span data-stu-id="05f03-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05f03-215">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05f03-215">Minimum supported client</span></span><br/> | <span data-ttu-id="05f03-216">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05f03-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="05f03-217">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05f03-217">Minimum supported server</span></span><br/> | <span data-ttu-id="05f03-218">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05f03-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05f03-219">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="05f03-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="05f03-220"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="05f03-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="05f03-221">DLL</span><span class="sxs-lookup"><span data-stu-id="05f03-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f03-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f03-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f03-223">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05f03-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f03-224">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="05f03-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="05f03-225">**монслитригжер**</span><span class="sxs-lookup"><span data-stu-id="05f03-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





