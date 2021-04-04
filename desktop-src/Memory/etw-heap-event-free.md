---
description: Событие трассировки управления памятью для операции освобождения кучи.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: Событие ETW_HEAP_EVENT_FREE (Нтвми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897194"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="10e01-103">\_ \_ Событие освобождения события кучи ETW \_</span><span class="sxs-lookup"><span data-stu-id="10e01-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="10e01-104">Событие **\_ \_ \_ освобождения события кучи ETW** — это событие трассировки управления памятью для операции освобождения кучи.</span><span class="sxs-lookup"><span data-stu-id="10e01-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="10e01-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="10e01-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e01-106">*хеафандле*</span><span class="sxs-lookup"><span data-stu-id="10e01-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="10e01-107">Маркер кучи, в которой была выделена память.</span><span class="sxs-lookup"><span data-stu-id="10e01-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="10e01-108">Это куча, обрабатывающая приложение, передаваемое функции [**аллокатехеап**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="10e01-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="10e01-109">*Адрес*</span><span class="sxs-lookup"><span data-stu-id="10e01-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="10e01-110">Адрес освобожденной памяти.</span><span class="sxs-lookup"><span data-stu-id="10e01-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="10e01-111">*Источник*</span><span class="sxs-lookup"><span data-stu-id="10e01-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="10e01-112">Источник памяти, используемый распределителем для выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="10e01-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="10e01-113">В следующей таблице перечислены возможные значения для *исходного* параметра, как определено в файле заголовка *нтетв. h* :</span><span class="sxs-lookup"><span data-stu-id="10e01-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="10e01-114">Значение</span><span class="sxs-lookup"><span data-stu-id="10e01-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="10e01-115">Значение</span><span class="sxs-lookup"><span data-stu-id="10e01-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="10e01-116"><dt>**Память \_ ИЗ \_ резервного**</dt> блока <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="10e01-117">Память из резервного списка.</span><span class="sxs-lookup"><span data-stu-id="10e01-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="10e01-118"><dt>**Память \_ ИЗ \_ ловфраг**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="10e01-119">Память из кучи с низкой фрагментацией.</span><span class="sxs-lookup"><span data-stu-id="10e01-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="10e01-120"><dt>**Память \_ ИЗ \_ маинпас**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="10e01-121">Память из основного пути кода.</span><span class="sxs-lookup"><span data-stu-id="10e01-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="10e01-122"><dt> **Память \_ от \_ словпас**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="10e01-123">Память от скорости c.</span><span class="sxs-lookup"><span data-stu-id="10e01-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="10e01-124"><dt>**Память \_ ИЗ \_ недопустимых**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="10e01-125">Недопустимая память.</span><span class="sxs-lookup"><span data-stu-id="10e01-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="10e01-126"><dt>**Память \_ ИЗ \_ \_ кучи сегментов**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="10e01-127">Это значение зарезервировано для будущего использования и никогда не будет возвращаться.</span><span class="sxs-lookup"><span data-stu-id="10e01-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10e01-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10e01-128">Remarks</span></span>

<span data-ttu-id="10e01-129">Событие **\_ \_ \_ освобождения события кучи ETW** регистрируется во всех операциях освобождения кучи.</span><span class="sxs-lookup"><span data-stu-id="10e01-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e01-130">Требования</span><span class="sxs-lookup"><span data-stu-id="10e01-130">Requirements</span></span>



| <span data-ttu-id="10e01-131">Требование</span><span class="sxs-lookup"><span data-stu-id="10e01-131">Requirement</span></span> | <span data-ttu-id="10e01-132">Значение</span><span class="sxs-lookup"><span data-stu-id="10e01-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10e01-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10e01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="10e01-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10e01-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10e01-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10e01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="10e01-136">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="10e01-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="10e01-137">Header</span><span class="sxs-lookup"><span data-stu-id="10e01-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e01-138"><dt>Нтвми. h</dt></span><span class="sxs-lookup"><span data-stu-id="10e01-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e01-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10e01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e01-140">События трассировки управления памятью</span><span class="sxs-lookup"><span data-stu-id="10e01-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
