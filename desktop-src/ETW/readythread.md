---
description: Этот класс является классом типа события для готовых событий потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Класс Реадисреад
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897645"
---
# <a name="readythread-class"></a><span data-ttu-id="f5e91-104">Класс Реадисреад</span><span class="sxs-lookup"><span data-stu-id="f5e91-104">ReadyThread class</span></span>

<span data-ttu-id="f5e91-105">Этот класс является классом типа события для готовых событий потока.</span><span class="sxs-lookup"><span data-stu-id="f5e91-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="f5e91-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="f5e91-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e91-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5e91-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="f5e91-108">Участники</span><span class="sxs-lookup"><span data-stu-id="f5e91-108">Members</span></span>

<span data-ttu-id="f5e91-109">Класс **реадисреад** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5e91-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="f5e91-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5e91-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5e91-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5e91-111">Properties</span></span>

<span data-ttu-id="f5e91-112">Класс **реадисреад** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5e91-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5e91-113">аджустинкремент</span><span class="sxs-lookup"><span data-stu-id="f5e91-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e91-114">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f5e91-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5e91-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="f5e91-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f5e91-117">Значение, по которому регулируется приоритет.</span><span class="sxs-lookup"><span data-stu-id="f5e91-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="f5e91-118">аджустреасон</span><span class="sxs-lookup"><span data-stu-id="f5e91-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e91-119">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f5e91-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5e91-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-121">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="f5e91-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f5e91-122">Причина повышения приоритета.</span><span class="sxs-lookup"><span data-stu-id="f5e91-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="f5e91-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e91-123">Value</span></span>                                                                        | <span data-ttu-id="f5e91-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e91-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5e91-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="f5e91-126">Не учитывать шаг приращения.</span><span class="sxs-lookup"><span data-stu-id="f5e91-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="f5e91-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f5e91-128">Примените шаг приращения, который будет Decay постепенно в конце каждого такта.</span><span class="sxs-lookup"><span data-stu-id="f5e91-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="f5e91-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f5e91-130">Применяйте инкремент в качестве увеличения, которое будет полностью Decay в такте (как правило, для пожертвования с учетом приоритета).</span><span class="sxs-lookup"><span data-stu-id="f5e91-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f5e91-131">Flag</span><span class="sxs-lookup"><span data-stu-id="f5e91-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e91-132">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f5e91-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5e91-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-134">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="f5e91-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f5e91-135">Ниже приведены возможные флаги состояния.</span><span class="sxs-lookup"><span data-stu-id="f5e91-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="f5e91-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e91-136">Value</span></span>                                                                          | <span data-ttu-id="f5e91-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e91-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5e91-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="f5e91-139">Поток был подготовлен от DPC (отложенный вызов процедуры).</span><span class="sxs-lookup"><span data-stu-id="f5e91-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="f5e91-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="f5e91-141">Стек ядра в настоящее время переключен.</span><span class="sxs-lookup"><span data-stu-id="f5e91-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="f5e91-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="f5e91-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="f5e91-143">Адресное пространство процесса загружается.</span><span class="sxs-lookup"><span data-stu-id="f5e91-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="f5e91-144">Обратите внимание, что при переключении стека ядра или адресного пространства процесса будет добавлено дополнительное событие Реадисреад после того, как стек ядра или адресное пространство процесса перейдет обратно в, и поток будет готов к отправке.</span><span class="sxs-lookup"><span data-stu-id="f5e91-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="f5e91-145">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="f5e91-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e91-146">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f5e91-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5e91-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-148">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="f5e91-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f5e91-149">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f5e91-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f5e91-150">тсреадид</span><span class="sxs-lookup"><span data-stu-id="f5e91-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e91-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5e91-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5e91-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e91-153">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f5e91-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f5e91-154">Идентификатор потока для выполнения.</span><span class="sxs-lookup"><span data-stu-id="f5e91-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5e91-155">Требования</span><span class="sxs-lookup"><span data-stu-id="f5e91-155">Requirements</span></span>



| <span data-ttu-id="f5e91-156">Требование</span><span class="sxs-lookup"><span data-stu-id="f5e91-156">Requirement</span></span> | <span data-ttu-id="f5e91-157">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e91-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f5e91-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5e91-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e91-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5e91-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f5e91-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5e91-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e91-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5e91-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f5e91-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5e91-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e91-163">**Поток \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="f5e91-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




