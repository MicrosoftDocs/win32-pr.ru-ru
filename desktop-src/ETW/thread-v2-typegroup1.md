---
description: Thread_V2_TypeGroup1 Class — этот класс является классом типа события для событий запуска и окончания потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Класс Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105662"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="650ab-104">\_Класс TypeGroup1 потока версии 2 \_</span><span class="sxs-lookup"><span data-stu-id="650ab-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="650ab-105">Этот класс является классом типа события для событий запуска и окончания потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="650ab-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="650ab-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="650ab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="650ab-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="650ab-108">Члены</span><span class="sxs-lookup"><span data-stu-id="650ab-108">Members</span></span>

<span data-ttu-id="650ab-109">Класс **Thread \_ v2 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="650ab-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="650ab-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="650ab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="650ab-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="650ab-111">Properties</span></span>

<span data-ttu-id="650ab-112">Класс **TypeGroup1 в потоке \_ версии 2 \_** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="650ab-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="650ab-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="650ab-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-116">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="650ab-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="650ab-117">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="650ab-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-118">стаккбасе</span><span class="sxs-lookup"><span data-stu-id="650ab-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-121">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-122">Базовый адрес стека потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-123">стакклимит</span><span class="sxs-lookup"><span data-stu-id="650ab-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-126">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-127">Ограничение стека потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-128">стартаддр</span><span class="sxs-lookup"><span data-stu-id="650ab-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-131">Квалификаторы: Вмидатаид (7), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-132">Адрес памяти, с которого начинается трассировка.</span><span class="sxs-lookup"><span data-stu-id="650ab-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-133">субпроцесстаг</span><span class="sxs-lookup"><span data-stu-id="650ab-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-136">Квалификаторы: Вмидатаид (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="650ab-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="650ab-137">Идентифицирует службу, если поток принадлежит службе; в противном случае — нуль.</span><span class="sxs-lookup"><span data-stu-id="650ab-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-138">теббасе</span><span class="sxs-lookup"><span data-stu-id="650ab-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-141">Квалификаторы: Вмидатаид (9), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-142">Базовый адрес блока среды потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-143">тсреадид</span><span class="sxs-lookup"><span data-stu-id="650ab-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-146">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="650ab-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="650ab-147">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="650ab-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-148">усерстаккбасе</span><span class="sxs-lookup"><span data-stu-id="650ab-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-151">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-152">Базовый адрес стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-153">усерстакклимит</span><span class="sxs-lookup"><span data-stu-id="650ab-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-156">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-157">Ограничение стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="650ab-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="650ab-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="650ab-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="650ab-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="650ab-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="650ab-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="650ab-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="650ab-161">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="650ab-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="650ab-162">Начальный адрес функции, которая будет выполнена этим потоком.</span><span class="sxs-lookup"><span data-stu-id="650ab-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="650ab-163">Remarks</span><span class="sxs-lookup"><span data-stu-id="650ab-163">Remarks</span></span>

<span data-ttu-id="650ab-164">Типы событий Дкстарт и Дценд перечисляют потоки, которые выполняются в данный момент во время запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="650ab-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="650ab-165">Требования</span><span class="sxs-lookup"><span data-stu-id="650ab-165">Requirements</span></span>



| <span data-ttu-id="650ab-166">Требование</span><span class="sxs-lookup"><span data-stu-id="650ab-166">Requirement</span></span> | <span data-ttu-id="650ab-167">Значение</span><span class="sxs-lookup"><span data-stu-id="650ab-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="650ab-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="650ab-168">Minimum supported client</span></span><br/> | <span data-ttu-id="650ab-169">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="650ab-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="650ab-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="650ab-170">Minimum supported server</span></span><br/> | <span data-ttu-id="650ab-171">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="650ab-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="650ab-172">См. также</span><span class="sxs-lookup"><span data-stu-id="650ab-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650ab-173">**Thread**</span><span class="sxs-lookup"><span data-stu-id="650ab-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="650ab-174">**Поток \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="650ab-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




