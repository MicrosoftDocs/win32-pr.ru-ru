---
description: Событие трассировки управления памятью для операции выделения кучи.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Событие ETW_HEAP_EVENT_ALLOC (Нтвми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343622"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="439bc-103">\_ \_ Событие выделения события кучи ETW \_</span><span class="sxs-lookup"><span data-stu-id="439bc-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="439bc-104">Событие **выделения \_ \_ события кучи \_ ETW** — это событие трассировки управления памятью для операции выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="439bc-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="439bc-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="439bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="439bc-106">*хеафандле*</span><span class="sxs-lookup"><span data-stu-id="439bc-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="439bc-107">Маркер кучи, в которой была выделена память.</span><span class="sxs-lookup"><span data-stu-id="439bc-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="439bc-108">Это куча, обрабатывающая приложение, передаваемое функции [**аллокатехеап**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="439bc-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="439bc-109">*Размер*</span><span class="sxs-lookup"><span data-stu-id="439bc-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="439bc-110">Размер в байтах, выделенный из кучи.</span><span class="sxs-lookup"><span data-stu-id="439bc-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="439bc-111">*Адрес*</span><span class="sxs-lookup"><span data-stu-id="439bc-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="439bc-112">Адрес выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="439bc-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="439bc-113">*Источник*</span><span class="sxs-lookup"><span data-stu-id="439bc-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="439bc-114">Источник памяти, используемый распределителем для выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="439bc-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="439bc-115">В следующей таблице перечислены возможные значения для *исходного* параметра, как определено в файле заголовка *нтетв. h* :</span><span class="sxs-lookup"><span data-stu-id="439bc-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="439bc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="439bc-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="439bc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="439bc-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="439bc-118"><dt>**Память \_ ИЗ \_ резервного**</dt> блока <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="439bc-119">Память из резервного списка.</span><span class="sxs-lookup"><span data-stu-id="439bc-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="439bc-120"><dt>**Память \_ ИЗ \_ ловфраг**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="439bc-121">Память из кучи с низкой фрагментацией.</span><span class="sxs-lookup"><span data-stu-id="439bc-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="439bc-122"><dt>**Память \_ ИЗ \_ маинпас**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="439bc-123">Память из основного пути кода.</span><span class="sxs-lookup"><span data-stu-id="439bc-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="439bc-124"><dt> **Память \_ от \_ словпас**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="439bc-125">Память из скорости.</span><span class="sxs-lookup"><span data-stu-id="439bc-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="439bc-126"><dt>**Память \_ ИЗ \_ недопустимых**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="439bc-127">Недопустимая память.</span><span class="sxs-lookup"><span data-stu-id="439bc-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="439bc-128"><dt>**Память \_ ИЗ \_ \_ кучи сегментов**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="439bc-129">Это значение зарезервировано для будущего использования и никогда не будет возвращаться.</span><span class="sxs-lookup"><span data-stu-id="439bc-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="439bc-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="439bc-130">Remarks</span></span>

<span data-ttu-id="439bc-131">Событие **выделения \_ \_ события кучи \_ ETW** регистрируется во всех выделениях кучи.</span><span class="sxs-lookup"><span data-stu-id="439bc-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="439bc-132">Требования</span><span class="sxs-lookup"><span data-stu-id="439bc-132">Requirements</span></span>



| <span data-ttu-id="439bc-133">Требование</span><span class="sxs-lookup"><span data-stu-id="439bc-133">Requirement</span></span> | <span data-ttu-id="439bc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="439bc-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="439bc-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="439bc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="439bc-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="439bc-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="439bc-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="439bc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="439bc-138">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="439bc-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="439bc-139">Header</span><span class="sxs-lookup"><span data-stu-id="439bc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="439bc-140"><dt>Нтвми. h</dt></span><span class="sxs-lookup"><span data-stu-id="439bc-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="439bc-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="439bc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="439bc-142">События трассировки управления памятью</span><span class="sxs-lookup"><span data-stu-id="439bc-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
