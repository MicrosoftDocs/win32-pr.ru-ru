---
description: Регистрирует поставщик и инициализирует наборы счетчиков.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Функция Каунтеринитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998529"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="c00f4-103">Функция Каунтеринитиализе</span><span class="sxs-lookup"><span data-stu-id="c00f4-103">CounterInitialize function</span></span>

<span data-ttu-id="c00f4-104">Регистрирует поставщик и инициализирует наборы счетчиков.</span><span class="sxs-lookup"><span data-stu-id="c00f4-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c00f4-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="c00f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c00f4-106">Parameters</span></span>

<span data-ttu-id="c00f4-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c00f4-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c00f4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c00f4-108">Return value</span></span>

<span data-ttu-id="c00f4-109">Возвращает ошибку \_ успешного выполнения; в противном случае — стандартный код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="c00f4-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c00f4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c00f4-110">Remarks</span></span>

<span data-ttu-id="c00f4-111">Поставщик вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c00f4-111">Your provider calls this function.</span></span> <span data-ttu-id="c00f4-112">Функция включает вызовы функции [**перфстартпровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) и функции [**перфсеткаунтерсетинфо**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="c00f4-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="c00f4-113">Средство [**КТРПП**](ctrpp.md) создает эту встроенную функцию при указании аргумента **-o** .</span><span class="sxs-lookup"><span data-stu-id="c00f4-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="c00f4-114">Имя функции включает строку *префикса* , если указан аргумент **-prefix** .</span><span class="sxs-lookup"><span data-stu-id="c00f4-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="c00f4-115">Если указать аргументы **-меморираутинес** или **-нотификатионкаллбакк** (или указать атрибут **обратного вызова** для элемента [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), то сигнатура **каунтеринитиализе** изменяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c00f4-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="c00f4-116">где</span><span class="sxs-lookup"><span data-stu-id="c00f4-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="c00f4-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>нотификатионкаллбакк</span><span class="sxs-lookup"><span data-stu-id="c00f4-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="c00f4-118">Имя функции обратного вызова [*контролкаллбакк*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) , которая реализуется для получения уведомлений о запросах потребителей (например, запросов на добавление или удаление счетчиков из запроса).</span><span class="sxs-lookup"><span data-stu-id="c00f4-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="c00f4-119">Если не реализовать функцию обратного вызова *контролкаллбакк* , задайте значение **null** .</span><span class="sxs-lookup"><span data-stu-id="c00f4-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c00f4-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>меморяллокатионфунктион</span><span class="sxs-lookup"><span data-stu-id="c00f4-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="c00f4-121">Имя функции обратного вызова [*аллокатемемори*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) , которая вызывается в PERFLIB для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="c00f4-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="c00f4-122">Задайте **значение NULL** , если не был указан аргумент **-меморираутинес** .</span><span class="sxs-lookup"><span data-stu-id="c00f4-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="c00f4-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>меморифрифунктион</span><span class="sxs-lookup"><span data-stu-id="c00f4-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="c00f4-124">Имя функции обратного вызова [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) , вызывающей PERFLIB для освобождения памяти, выделенной с помощью функции [*аллокатемемори*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) .</span><span class="sxs-lookup"><span data-stu-id="c00f4-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="c00f4-125">Задайте **значение NULL** , если *Меморяллокатионфунктион* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c00f4-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c00f4-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>меморифунктионконтекст</span><span class="sxs-lookup"><span data-stu-id="c00f4-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="c00f4-127">Контекстные сведения, передаваемые в подпрограммы выделения памяти и свободные.</span><span class="sxs-lookup"><span data-stu-id="c00f4-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="c00f4-128">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c00f4-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c00f4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c00f4-129">Requirements</span></span>



| <span data-ttu-id="c00f4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c00f4-130">Requirement</span></span> | <span data-ttu-id="c00f4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c00f4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c00f4-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c00f4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c00f4-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c00f4-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c00f4-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c00f4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c00f4-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c00f4-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

