---
description: Этот класс является классом типа события для событий запуска потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Класс Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998749"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="9f4d0-104">\_ \_ Класс TypeGroup1 потока v1</span><span class="sxs-lookup"><span data-stu-id="9f4d0-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="9f4d0-105">Этот класс является классом типа события для событий запуска потока.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="9f4d0-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f4d0-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="9f4d0-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9f4d0-108">Members</span></span>

<span data-ttu-id="9f4d0-109">Класс **Thread \_ v1 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9f4d0-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="9f4d0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f4d0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f4d0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f4d0-111">Properties</span></span>

<span data-ttu-id="9f4d0-112">Класс **Thread \_ v1 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f4d0-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9f4d0-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-116">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-117">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="9f4d0-118">**Windows Server 2003:** Содержит квалификатор формата ("x").</span><span class="sxs-lookup"><span data-stu-id="9f4d0-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-119">стаккбасе</span><span class="sxs-lookup"><span data-stu-id="9f4d0-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-122">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-123">Базовый адрес стека потока.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-124">стакклимит</span><span class="sxs-lookup"><span data-stu-id="9f4d0-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-127">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-128">Ограничение стека потока.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-129">стартаддр</span><span class="sxs-lookup"><span data-stu-id="9f4d0-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-132">Квалификаторы: Вмидатаид (7), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-133">Адрес памяти, с которого начинается трассировка.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-134">тсреадид</span><span class="sxs-lookup"><span data-stu-id="9f4d0-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-137">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-138">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="9f4d0-139">**Windows Server 2003:** Содержит квалификатор формата ("x").</span><span class="sxs-lookup"><span data-stu-id="9f4d0-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-140">усерстаккбасе</span><span class="sxs-lookup"><span data-stu-id="9f4d0-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-143">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-144">Базовый адрес стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-145">усерстакклимит</span><span class="sxs-lookup"><span data-stu-id="9f4d0-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-148">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-149">Ограничение стека пользовательского режима потока.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-150">ваитмоде</span><span class="sxs-lookup"><span data-stu-id="9f4d0-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-151">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-153">Квалификаторы: Вмидатаид (9), Format ("c")</span><span class="sxs-lookup"><span data-stu-id="9f4d0-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-154">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="9f4d0-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d0-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f4d0-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f4d0-158">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f4d0-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f4d0-159">Начальный адрес функции, которая будет выполнена этим потоком.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f4d0-160">Требования</span><span class="sxs-lookup"><span data-stu-id="9f4d0-160">Requirements</span></span>



| <span data-ttu-id="9f4d0-161">Требование</span><span class="sxs-lookup"><span data-stu-id="9f4d0-161">Requirement</span></span> | <span data-ttu-id="9f4d0-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9f4d0-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f4d0-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f4d0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4d0-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f4d0-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9f4d0-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f4d0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4d0-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f4d0-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9f4d0-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f4d0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4d0-168">**Поток \_ v1**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




