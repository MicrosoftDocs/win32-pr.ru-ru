---
description: Этот класс является классом типа события для событий запуска и окончания потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Класс Thread_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155551"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="de01b-104">\_Класс TypeGroup1 потока</span><span class="sxs-lookup"><span data-stu-id="de01b-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="de01b-105">Этот класс является классом типа события для событий запуска и окончания потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="de01b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="de01b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="de01b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de01b-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="de01b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="de01b-108">Members</span></span>

<span data-ttu-id="de01b-109">Класс **Thread \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="de01b-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="de01b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="de01b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de01b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="de01b-111">Properties</span></span>

<span data-ttu-id="de01b-112">Класс **\_ TypeGroup1 потока** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="de01b-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de01b-113">Сходство</span><span class="sxs-lookup"><span data-stu-id="de01b-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-116">Квалификаторы: Вмидатаид (7), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-117">Набор процессоров, для которых разрешено выполнение потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-118">басеприорити</span><span class="sxs-lookup"><span data-stu-id="de01b-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="de01b-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-121">Квалификаторы: Вмидатаид (11)</span><span class="sxs-lookup"><span data-stu-id="de01b-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="de01b-122">Приоритет планировщика потока (см. функцию [**сетсреадприорити**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) ).</span><span class="sxs-lookup"><span data-stu-id="de01b-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="de01b-123">иоприорити</span><span class="sxs-lookup"><span data-stu-id="de01b-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="de01b-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-126">Квалификаторы: Вмидатаид (13)</span><span class="sxs-lookup"><span data-stu-id="de01b-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="de01b-127">Указание приоритета ввода-вывода для планирования IOs, созданного потоком.</span><span class="sxs-lookup"><span data-stu-id="de01b-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-128">пажеприорити</span><span class="sxs-lookup"><span data-stu-id="de01b-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="de01b-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-131">Квалификаторы: Вмидатаид (12)</span><span class="sxs-lookup"><span data-stu-id="de01b-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="de01b-132">Указание приоритета страницы памяти для страниц памяти, к которым обращается поток.</span><span class="sxs-lookup"><span data-stu-id="de01b-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="de01b-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-136">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="de01b-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="de01b-137">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="de01b-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-138">стаккбасе</span><span class="sxs-lookup"><span data-stu-id="de01b-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-141">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-142">Базовый адрес стека потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-143">стакклимит</span><span class="sxs-lookup"><span data-stu-id="de01b-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-146">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-147">Ограничение стека потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-148">субпроцесстаг</span><span class="sxs-lookup"><span data-stu-id="de01b-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-151">Квалификаторы: Вмидатаид (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="de01b-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="de01b-152">Идентифицирует службу, если поток принадлежит службе; в противном случае — нуль.</span><span class="sxs-lookup"><span data-stu-id="de01b-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-153">теббасе</span><span class="sxs-lookup"><span data-stu-id="de01b-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-156">Квалификаторы: Вмидатаид (9), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-157">Базовый адрес блока среды потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-158">среадфлагс</span><span class="sxs-lookup"><span data-stu-id="de01b-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-159">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="de01b-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-161">Квалификаторы: Вмидатаид (14)</span><span class="sxs-lookup"><span data-stu-id="de01b-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="de01b-162">Не используется.</span><span class="sxs-lookup"><span data-stu-id="de01b-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-163">тсреадид</span><span class="sxs-lookup"><span data-stu-id="de01b-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-166">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="de01b-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="de01b-167">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="de01b-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-168">усерстаккбасе</span><span class="sxs-lookup"><span data-stu-id="de01b-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-169">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-171">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-172">Базовый адрес стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-173">усерстакклимит</span><span class="sxs-lookup"><span data-stu-id="de01b-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-176">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-177">Ограничение стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="de01b-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="de01b-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="de01b-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de01b-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de01b-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de01b-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de01b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de01b-181">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="de01b-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="de01b-182">Начальный адрес функции, которая будет выполнена этим потоком.</span><span class="sxs-lookup"><span data-stu-id="de01b-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de01b-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="de01b-183">Remarks</span></span>

<span data-ttu-id="de01b-184">Типы событий Дкстарт и Дценд перечисляют потоки, которые выполняются в данный момент во время запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="de01b-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="de01b-185">Требования</span><span class="sxs-lookup"><span data-stu-id="de01b-185">Requirements</span></span>



| <span data-ttu-id="de01b-186">Требование</span><span class="sxs-lookup"><span data-stu-id="de01b-186">Requirement</span></span> | <span data-ttu-id="de01b-187">Значение</span><span class="sxs-lookup"><span data-stu-id="de01b-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de01b-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de01b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="de01b-189">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de01b-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de01b-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de01b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="de01b-191">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de01b-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de01b-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de01b-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de01b-193">**Поток**</span><span class="sxs-lookup"><span data-stu-id="de01b-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
