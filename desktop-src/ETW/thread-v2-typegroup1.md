---
description: Этот класс является классом типа события для событий запуска и окончания потока. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265061"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="9fe0b-104">\_Класс TypeGroup1 потока версии 2 \_</span><span class="sxs-lookup"><span data-stu-id="9fe0b-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="9fe0b-105">Этот класс является классом типа события для событий запуска и окончания потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="9fe0b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe0b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fe0b-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="9fe0b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9fe0b-108">Members</span></span>

<span data-ttu-id="9fe0b-109">Класс **Thread \_ v2 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9fe0b-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="9fe0b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9fe0b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fe0b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9fe0b-111">Properties</span></span>

<span data-ttu-id="9fe0b-112">Класс **TypeGroup1 в потоке \_ версии 2 \_** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fe0b-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9fe0b-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-116">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9fe0b-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-117">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-118">стаккбасе</span><span class="sxs-lookup"><span data-stu-id="9fe0b-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-121">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-122">Базовый адрес стека потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-123">стакклимит</span><span class="sxs-lookup"><span data-stu-id="9fe0b-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-126">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-127">Ограничение стека потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-128">стартаддр</span><span class="sxs-lookup"><span data-stu-id="9fe0b-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-131">Квалификаторы: Вмидатаид (7), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-132">Адрес памяти, с которого начинается трассировка.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-133">субпроцесстаг</span><span class="sxs-lookup"><span data-stu-id="9fe0b-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-136">Квалификаторы: Вмидатаид (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9fe0b-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-137">Идентифицирует службу, если поток принадлежит службе; в противном случае — нуль.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-138">теббасе</span><span class="sxs-lookup"><span data-stu-id="9fe0b-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-141">Квалификаторы: Вмидатаид (9), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-142">Базовый адрес блока среды потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-143">тсреадид</span><span class="sxs-lookup"><span data-stu-id="9fe0b-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-146">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="9fe0b-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-147">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-148">усерстаккбасе</span><span class="sxs-lookup"><span data-stu-id="9fe0b-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-151">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-152">Базовый адрес стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-153">усерстакклимит</span><span class="sxs-lookup"><span data-stu-id="9fe0b-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-156">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-157">Ограничение стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="9fe0b-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="9fe0b-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fe0b-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9fe0b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fe0b-161">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="9fe0b-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9fe0b-162">Начальный адрес функции, которая будет выполнена этим потоком.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fe0b-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fe0b-163">Remarks</span></span>

<span data-ttu-id="9fe0b-164">Типы событий Дкстарт и Дценд перечисляют потоки, которые выполняются в данный момент во время запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="9fe0b-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe0b-165">Требования</span><span class="sxs-lookup"><span data-stu-id="9fe0b-165">Requirements</span></span>



| <span data-ttu-id="9fe0b-166">Требование</span><span class="sxs-lookup"><span data-stu-id="9fe0b-166">Requirement</span></span> | <span data-ttu-id="9fe0b-167">Значение</span><span class="sxs-lookup"><span data-stu-id="9fe0b-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fe0b-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fe0b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe0b-169">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fe0b-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fe0b-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fe0b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe0b-171">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fe0b-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe0b-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fe0b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe0b-173">**Поток**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="9fe0b-174">**Поток \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="9fe0b-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




