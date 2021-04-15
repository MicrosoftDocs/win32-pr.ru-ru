---
description: Событие трассировки управления памятью для операции перераспределения кучи.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Событие ETW_HEAP_EVENT_REALLOC (Нтвми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683354"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="ee4ad-103">\_ \_ \_ Событие перераспределения события кучи ETW</span><span class="sxs-lookup"><span data-stu-id="ee4ad-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="ee4ad-104">Событие перераспределения **\_ \_ события \_ кучи ETW** — это событие трассировки управления памятью для операции перераспределения кучи.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="ee4ad-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee4ad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4ad-106">*хеафандле*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-107">Маркер кучи, в которой была выделена память.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="ee4ad-108">Это куча, обрабатывающая приложение, передаваемое функции [**аллокатехеап**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ee4ad-109">*неваддресс*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-110">Новый адрес выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ee4ad-111">*олдаддресс*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-112">Старый адрес памяти, выделенной ранее.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ee4ad-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-114">Новый размер в байтах, выделенный из кучи.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="ee4ad-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-116">Старый размер в байтах, ранее выделенных из кучи.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="ee4ad-117">*Источник*</span><span class="sxs-lookup"><span data-stu-id="ee4ad-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4ad-118">Источник памяти, используемый распределителем для выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="ee4ad-119">В следующей таблице перечислены возможные значения для *исходного* параметра, как определено в файле заголовка *нтетв. h* :</span><span class="sxs-lookup"><span data-stu-id="ee4ad-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="ee4ad-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4ad-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="ee4ad-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4ad-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="ee4ad-122"><dt>**Память \_ ИЗ \_ резервного**</dt> блока <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="ee4ad-123">Память из резервного списка.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="ee4ad-124"><dt>**Память \_ ИЗ \_ ловфраг**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="ee4ad-125">Память из кучи с низкой фрагментацией.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="ee4ad-126"><dt>**Память \_ ИЗ \_ маинпас**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="ee4ad-127">Память из основного пути кода.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="ee4ad-128"><dt> **Память \_ от \_ словпас**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ee4ad-129">Память от скорости c.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="ee4ad-130"><dt>**Память \_ ИЗ \_ недопустимых**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="ee4ad-131">Недопустимая память.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="ee4ad-132"><dt>**Память \_ ИЗ \_ \_ кучи сегментов**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="ee4ad-133">Это значение зарезервировано для будущего использования и никогда не будет возвращаться.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="ee4ad-134">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4ad-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee4ad-135">Remarks</span></span>

<span data-ttu-id="ee4ad-136">Событие **\_ \_ \_ перераспределения события кучи ETW** регистрируется во всех перераспределениях кучи.</span><span class="sxs-lookup"><span data-stu-id="ee4ad-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4ad-137">Требования</span><span class="sxs-lookup"><span data-stu-id="ee4ad-137">Requirements</span></span>



| <span data-ttu-id="ee4ad-138">Требование</span><span class="sxs-lookup"><span data-stu-id="ee4ad-138">Requirement</span></span> | <span data-ttu-id="ee4ad-139">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4ad-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4ad-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee4ad-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4ad-141">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ee4ad-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ee4ad-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee4ad-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4ad-143">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee4ad-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ee4ad-144">Header</span><span class="sxs-lookup"><span data-stu-id="ee4ad-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4ad-145"><dt>Нтвми. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4ad-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4ad-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee4ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4ad-147">События трассировки управления памятью</span><span class="sxs-lookup"><span data-stu-id="ee4ad-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
