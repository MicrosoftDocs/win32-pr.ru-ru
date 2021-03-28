---
description: Этот класс является классом типа событий для событий переключения контекста. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Класс Ксвитч
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263346"
---
# <a name="cswitch-class"></a><span data-ttu-id="e2b76-104">Класс Ксвитч</span><span class="sxs-lookup"><span data-stu-id="e2b76-104">CSwitch class</span></span>

<span data-ttu-id="e2b76-105">Этот класс является классом типа событий для событий переключения контекста.</span><span class="sxs-lookup"><span data-stu-id="e2b76-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="e2b76-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e2b76-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b76-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2b76-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="e2b76-108">Участники</span><span class="sxs-lookup"><span data-stu-id="e2b76-108">Members</span></span>

<span data-ttu-id="e2b76-109">Класс **ксвитч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e2b76-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="e2b76-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2b76-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2b76-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2b76-111">Properties</span></span>

<span data-ttu-id="e2b76-112">Класс **ксвитч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e2b76-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2b76-113">**невсреадид**</span><span class="sxs-lookup"><span data-stu-id="e2b76-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b76-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-116">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e2b76-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-117">Новый идентификатор потока после параметра.</span><span class="sxs-lookup"><span data-stu-id="e2b76-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-118">**невсреадприорити**</span><span class="sxs-lookup"><span data-stu-id="e2b76-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-119">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-121">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="e2b76-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-122">Приоритет потока нового потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-123">**невсреадваиттиме**</span><span class="sxs-lookup"><span data-stu-id="e2b76-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b76-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-126">Квалификаторы: Вмидатаид (11), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e2b76-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-127">Время ожидания для нового потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-128">**олдсреадид**</span><span class="sxs-lookup"><span data-stu-id="e2b76-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b76-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-131">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e2b76-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-132">ИДЕНТИФИКАТОР предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-133">**олдсреадприорити**</span><span class="sxs-lookup"><span data-stu-id="e2b76-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-134">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-136">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="e2b76-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-137">Приоритет потока предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-138">**олдсреадстате**</span><span class="sxs-lookup"><span data-stu-id="e2b76-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-139">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-141">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="e2b76-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-142">Состояние предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-142">State of the previous thread.</span></span> <span data-ttu-id="e2b76-143">Возможны следующие значения состояния:</span><span class="sxs-lookup"><span data-stu-id="e2b76-143">The following are the possible state values:</span></span>

| <span data-ttu-id="e2b76-144">Состояние</span><span class="sxs-lookup"><span data-stu-id="e2b76-144">State</span></span> | <span data-ttu-id="e2b76-145">Описание</span><span class="sxs-lookup"><span data-stu-id="e2b76-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="e2b76-146">0</span><span class="sxs-lookup"><span data-stu-id="e2b76-146">0</span></span>     | <span data-ttu-id="e2b76-147">инициализированные</span><span class="sxs-lookup"><span data-stu-id="e2b76-147">Initialized</span></span>                                   |
| <span data-ttu-id="e2b76-148">1</span><span class="sxs-lookup"><span data-stu-id="e2b76-148">1</span></span>     | <span data-ttu-id="e2b76-149">Ready</span><span class="sxs-lookup"><span data-stu-id="e2b76-149">Ready</span></span>                                         |
| <span data-ttu-id="e2b76-150">2</span><span class="sxs-lookup"><span data-stu-id="e2b76-150">2</span></span>     | <span data-ttu-id="e2b76-151">Запущен</span><span class="sxs-lookup"><span data-stu-id="e2b76-151">Running</span></span>                                       |
| <span data-ttu-id="e2b76-152">3</span><span class="sxs-lookup"><span data-stu-id="e2b76-152">3</span></span>     | <span data-ttu-id="e2b76-153">Ждущий режим</span><span class="sxs-lookup"><span data-stu-id="e2b76-153">Standby</span></span>                                       |
| <span data-ttu-id="e2b76-154">4</span><span class="sxs-lookup"><span data-stu-id="e2b76-154">4</span></span>     | <span data-ttu-id="e2b76-155">Завершен</span><span class="sxs-lookup"><span data-stu-id="e2b76-155">Terminated</span></span>                                    |
| <span data-ttu-id="e2b76-156">5</span><span class="sxs-lookup"><span data-stu-id="e2b76-156">5</span></span>     | <span data-ttu-id="e2b76-157">Ожидание</span><span class="sxs-lookup"><span data-stu-id="e2b76-157">Waiting</span></span>                                       |
| <span data-ttu-id="e2b76-158">6</span><span class="sxs-lookup"><span data-stu-id="e2b76-158">6</span></span>     | <span data-ttu-id="e2b76-159">Переход</span><span class="sxs-lookup"><span data-stu-id="e2b76-159">Transition</span></span>                                    |
| <span data-ttu-id="e2b76-160">7</span><span class="sxs-lookup"><span data-stu-id="e2b76-160">7</span></span>     | <span data-ttu-id="e2b76-161">Деферредреади (добавляется для Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="e2b76-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="e2b76-162">**олдсреадваитидеалпроцессор**</span><span class="sxs-lookup"><span data-stu-id="e2b76-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-163">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-165">Квалификаторы: Вмидатаид (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e2b76-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-166">Идеальное время ожидания предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-167">**олдсреадваитмоде**</span><span class="sxs-lookup"><span data-stu-id="e2b76-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-168">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-170">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="e2b76-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-171">Режим ожидания для предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="e2b76-172">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e2b76-172">The following are the possible values:</span></span>

| <span data-ttu-id="e2b76-173">Состояние</span><span class="sxs-lookup"><span data-stu-id="e2b76-173">State</span></span> | <span data-ttu-id="e2b76-174">Описание</span><span class="sxs-lookup"><span data-stu-id="e2b76-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="e2b76-175">0</span><span class="sxs-lookup"><span data-stu-id="e2b76-175">0</span></span>     | <span data-ttu-id="e2b76-176">Значение kernelmode</span><span class="sxs-lookup"><span data-stu-id="e2b76-176">KernelMode</span></span>  |
| <span data-ttu-id="e2b76-177">1</span><span class="sxs-lookup"><span data-stu-id="e2b76-177">1</span></span>     | <span data-ttu-id="e2b76-178">Пользовательском</span><span class="sxs-lookup"><span data-stu-id="e2b76-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="e2b76-179">**олдсреадваитреасон**</span><span class="sxs-lookup"><span data-stu-id="e2b76-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-180">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-182">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="e2b76-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-183">Причина ожидания предыдущего потока.</span><span class="sxs-lookup"><span data-stu-id="e2b76-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="e2b76-184">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e2b76-184">The following are the possible values:</span></span>

| <span data-ttu-id="e2b76-185">Состояние</span><span class="sxs-lookup"><span data-stu-id="e2b76-185">State</span></span> | <span data-ttu-id="e2b76-186">Описание</span><span class="sxs-lookup"><span data-stu-id="e2b76-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="e2b76-187">0</span><span class="sxs-lookup"><span data-stu-id="e2b76-187">0</span></span>     | <span data-ttu-id="e2b76-188">Руководитель</span><span class="sxs-lookup"><span data-stu-id="e2b76-188">Executive</span></span>         |
| <span data-ttu-id="e2b76-189">1</span><span class="sxs-lookup"><span data-stu-id="e2b76-189">1</span></span>     | <span data-ttu-id="e2b76-190">фрипаже</span><span class="sxs-lookup"><span data-stu-id="e2b76-190">FreePage</span></span>          |
| <span data-ttu-id="e2b76-191">2</span><span class="sxs-lookup"><span data-stu-id="e2b76-191">2</span></span>     | <span data-ttu-id="e2b76-192">Начало загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="e2b76-192">PageIn</span></span>            |
| <span data-ttu-id="e2b76-193">3</span><span class="sxs-lookup"><span data-stu-id="e2b76-193">3</span></span>     | <span data-ttu-id="e2b76-194">пулаллокатион</span><span class="sxs-lookup"><span data-stu-id="e2b76-194">PoolAllocation</span></span>    |
| <span data-ttu-id="e2b76-195">4</span><span class="sxs-lookup"><span data-stu-id="e2b76-195">4</span></span>     | <span data-ttu-id="e2b76-196">делайексекутион</span><span class="sxs-lookup"><span data-stu-id="e2b76-196">DelayExecution</span></span>    |
| <span data-ttu-id="e2b76-197">5</span><span class="sxs-lookup"><span data-stu-id="e2b76-197">5</span></span>     | <span data-ttu-id="e2b76-198">Приостановлена</span><span class="sxs-lookup"><span data-stu-id="e2b76-198">Suspended</span></span>         |
| <span data-ttu-id="e2b76-199">6</span><span class="sxs-lookup"><span data-stu-id="e2b76-199">6</span></span>     | <span data-ttu-id="e2b76-200">усеррекуест</span><span class="sxs-lookup"><span data-stu-id="e2b76-200">UserRequest</span></span>       |
| <span data-ttu-id="e2b76-201">7</span><span class="sxs-lookup"><span data-stu-id="e2b76-201">7</span></span>     | <span data-ttu-id="e2b76-202">врексекутиве</span><span class="sxs-lookup"><span data-stu-id="e2b76-202">WrExecutive</span></span>       |
| <span data-ttu-id="e2b76-203">8</span><span class="sxs-lookup"><span data-stu-id="e2b76-203">8</span></span>     | <span data-ttu-id="e2b76-204">врфрипаже</span><span class="sxs-lookup"><span data-stu-id="e2b76-204">WrFreePage</span></span>        |
| <span data-ttu-id="e2b76-205">9</span><span class="sxs-lookup"><span data-stu-id="e2b76-205">9</span></span>     | <span data-ttu-id="e2b76-206">врпажеин</span><span class="sxs-lookup"><span data-stu-id="e2b76-206">WrPageIn</span></span>          |
| <span data-ttu-id="e2b76-207">10</span><span class="sxs-lookup"><span data-stu-id="e2b76-207">10</span></span>    | <span data-ttu-id="e2b76-208">врпулаллокатион</span><span class="sxs-lookup"><span data-stu-id="e2b76-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="e2b76-209">11</span><span class="sxs-lookup"><span data-stu-id="e2b76-209">11</span></span>    | <span data-ttu-id="e2b76-210">врделайексекутион</span><span class="sxs-lookup"><span data-stu-id="e2b76-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="e2b76-211">12</span><span class="sxs-lookup"><span data-stu-id="e2b76-211">12</span></span>    | <span data-ttu-id="e2b76-212">врсуспендед</span><span class="sxs-lookup"><span data-stu-id="e2b76-212">WrSuspended</span></span>       |
| <span data-ttu-id="e2b76-213">13</span><span class="sxs-lookup"><span data-stu-id="e2b76-213">13</span></span>    | <span data-ttu-id="e2b76-214">врусеррекуест</span><span class="sxs-lookup"><span data-stu-id="e2b76-214">WrUserRequest</span></span>     |
| <span data-ttu-id="e2b76-215">14</span><span class="sxs-lookup"><span data-stu-id="e2b76-215">14</span></span>    | <span data-ttu-id="e2b76-216">вревентпаир</span><span class="sxs-lookup"><span data-stu-id="e2b76-216">WrEventPair</span></span>       |
| <span data-ttu-id="e2b76-217">15</span><span class="sxs-lookup"><span data-stu-id="e2b76-217">15</span></span>    | <span data-ttu-id="e2b76-218">вркуеуе</span><span class="sxs-lookup"><span data-stu-id="e2b76-218">WrQueue</span></span>           |
| <span data-ttu-id="e2b76-219">16</span><span class="sxs-lookup"><span data-stu-id="e2b76-219">16</span></span>    | <span data-ttu-id="e2b76-220">врлпкрецеиве</span><span class="sxs-lookup"><span data-stu-id="e2b76-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="e2b76-221">17</span><span class="sxs-lookup"><span data-stu-id="e2b76-221">17</span></span>    | <span data-ttu-id="e2b76-222">врлпкрепли</span><span class="sxs-lookup"><span data-stu-id="e2b76-222">WrLpcReply</span></span>        |
| <span data-ttu-id="e2b76-223">18</span><span class="sxs-lookup"><span data-stu-id="e2b76-223">18</span></span>    | <span data-ttu-id="e2b76-224">врвиртуалмемори</span><span class="sxs-lookup"><span data-stu-id="e2b76-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="e2b76-225">19</span><span class="sxs-lookup"><span data-stu-id="e2b76-225">19</span></span>    | <span data-ttu-id="e2b76-226">врпажеаут</span><span class="sxs-lookup"><span data-stu-id="e2b76-226">WrPageOut</span></span>         |
| <span data-ttu-id="e2b76-227">20</span><span class="sxs-lookup"><span data-stu-id="e2b76-227">20</span></span>    | <span data-ttu-id="e2b76-228">вррендезваус</span><span class="sxs-lookup"><span data-stu-id="e2b76-228">WrRendezvous</span></span>      |
| <span data-ttu-id="e2b76-229">21</span><span class="sxs-lookup"><span data-stu-id="e2b76-229">21</span></span>    | <span data-ttu-id="e2b76-230">вркэйедевент</span><span class="sxs-lookup"><span data-stu-id="e2b76-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="e2b76-231">22</span><span class="sxs-lookup"><span data-stu-id="e2b76-231">22</span></span>    | <span data-ttu-id="e2b76-232">вртерминатед</span><span class="sxs-lookup"><span data-stu-id="e2b76-232">WrTerminated</span></span>      |
| <span data-ttu-id="e2b76-233">23</span><span class="sxs-lookup"><span data-stu-id="e2b76-233">23</span></span>    | <span data-ttu-id="e2b76-234">врпроцессинсвап</span><span class="sxs-lookup"><span data-stu-id="e2b76-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="e2b76-235">24</span><span class="sxs-lookup"><span data-stu-id="e2b76-235">24</span></span>    | <span data-ttu-id="e2b76-236">вркпуратеконтрол</span><span class="sxs-lookup"><span data-stu-id="e2b76-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="e2b76-237">25</span><span class="sxs-lookup"><span data-stu-id="e2b76-237">25</span></span>    | <span data-ttu-id="e2b76-238">вркаллаутстакк</span><span class="sxs-lookup"><span data-stu-id="e2b76-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="e2b76-239">26</span><span class="sxs-lookup"><span data-stu-id="e2b76-239">26</span></span>    | <span data-ttu-id="e2b76-240">вркернел</span><span class="sxs-lookup"><span data-stu-id="e2b76-240">WrKernel</span></span>          |
| <span data-ttu-id="e2b76-241">27</span><span class="sxs-lookup"><span data-stu-id="e2b76-241">27</span></span>    | <span data-ttu-id="e2b76-242">врресаурце</span><span class="sxs-lookup"><span data-stu-id="e2b76-242">WrResource</span></span>        |
| <span data-ttu-id="e2b76-243">28</span><span class="sxs-lookup"><span data-stu-id="e2b76-243">28</span></span>    | <span data-ttu-id="e2b76-244">врпушлокк</span><span class="sxs-lookup"><span data-stu-id="e2b76-244">WrPushLock</span></span>        |
| <span data-ttu-id="e2b76-245">29</span><span class="sxs-lookup"><span data-stu-id="e2b76-245">29</span></span>    | <span data-ttu-id="e2b76-246">врмутекс</span><span class="sxs-lookup"><span data-stu-id="e2b76-246">WrMutex</span></span>           |
| <span data-ttu-id="e2b76-247">30</span><span class="sxs-lookup"><span data-stu-id="e2b76-247">30</span></span>    | <span data-ttu-id="e2b76-248">вркуантуменд</span><span class="sxs-lookup"><span data-stu-id="e2b76-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="e2b76-249">31</span><span class="sxs-lookup"><span data-stu-id="e2b76-249">31</span></span>    | <span data-ttu-id="e2b76-250">врдиспатчинт</span><span class="sxs-lookup"><span data-stu-id="e2b76-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="e2b76-251">32</span><span class="sxs-lookup"><span data-stu-id="e2b76-251">32</span></span>    | <span data-ttu-id="e2b76-252">врпримптед</span><span class="sxs-lookup"><span data-stu-id="e2b76-252">WrPreempted</span></span>       |
| <span data-ttu-id="e2b76-253">33</span><span class="sxs-lookup"><span data-stu-id="e2b76-253">33</span></span>    | <span data-ttu-id="e2b76-254">вриелдексекутион</span><span class="sxs-lookup"><span data-stu-id="e2b76-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="e2b76-255">34</span><span class="sxs-lookup"><span data-stu-id="e2b76-255">34</span></span>    | <span data-ttu-id="e2b76-256">врфастмутекс</span><span class="sxs-lookup"><span data-stu-id="e2b76-256">WrFastMutex</span></span>       |
| <span data-ttu-id="e2b76-257">35</span><span class="sxs-lookup"><span data-stu-id="e2b76-257">35</span></span>    | <span data-ttu-id="e2b76-258">вргуардедмутекс</span><span class="sxs-lookup"><span data-stu-id="e2b76-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="e2b76-259">36</span><span class="sxs-lookup"><span data-stu-id="e2b76-259">36</span></span>    | <span data-ttu-id="e2b76-260">вррундовн</span><span class="sxs-lookup"><span data-stu-id="e2b76-260">WrRundown</span></span>         |
| <span data-ttu-id="e2b76-261">37</span><span class="sxs-lookup"><span data-stu-id="e2b76-261">37</span></span>    | <span data-ttu-id="e2b76-262">максимумваитреасон</span><span class="sxs-lookup"><span data-stu-id="e2b76-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="e2b76-263">**превиаускстате**</span><span class="sxs-lookup"><span data-stu-id="e2b76-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-264">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-266">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="e2b76-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-267">Индекс состояния C, которое использовалось процессором в последний раз.</span><span class="sxs-lookup"><span data-stu-id="e2b76-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="e2b76-268">Значение 0 представляет самое светлое состояние простоя с более высоким значением, представляющим более глубокие состояния C.</span><span class="sxs-lookup"><span data-stu-id="e2b76-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e2b76-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-270">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b76-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-272">Квалификаторы: Вмидатаид (12)</span><span class="sxs-lookup"><span data-stu-id="e2b76-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-273">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e2b76-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e2b76-274">**спаребите**</span><span class="sxs-lookup"><span data-stu-id="e2b76-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b76-275">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="e2b76-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b76-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b76-277">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="e2b76-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="e2b76-278">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b76-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2b76-279">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2b76-279">Remarks</span></span>

<span data-ttu-id="e2b76-280">Эти события создают большой объем событий.</span><span class="sxs-lookup"><span data-stu-id="e2b76-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b76-281">Требования</span><span class="sxs-lookup"><span data-stu-id="e2b76-281">Requirements</span></span>



| <span data-ttu-id="e2b76-282">Требование</span><span class="sxs-lookup"><span data-stu-id="e2b76-282">Requirement</span></span> | <span data-ttu-id="e2b76-283">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b76-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2b76-284">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2b76-284">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b76-285">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2b76-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2b76-286">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2b76-286">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b76-287">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2b76-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2b76-288">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2b76-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b76-289">**Поток**</span><span class="sxs-lookup"><span data-stu-id="e2b76-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="e2b76-290">**Поток \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="e2b76-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




