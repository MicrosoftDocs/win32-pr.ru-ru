---
title: IDXCoreAdapter::QueryState
description: Извлекает текущее состояние указанного элемента на адаптере.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719137"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="758ab-103">Метод Идкскореадаптер:: Куеристате</span><span class="sxs-lookup"><span data-stu-id="758ab-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="758ab-104">Извлекает текущее состояние указанного элемента на адаптере.</span><span class="sxs-lookup"><span data-stu-id="758ab-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="758ab-105">Перед вызовом **куеристате** для типа свойства вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="758ab-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="758ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="758ab-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="758ab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="758ab-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="758ab-108">state</span><span class="sxs-lookup"><span data-stu-id="758ab-108">state</span></span>

<span data-ttu-id="758ab-109">Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="758ab-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="758ab-110">Тип элемента состояния на адаптере, состояние которого вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="758ab-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="758ab-111">Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="758ab-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="758ab-112">инпутстатедетаилссизе</span><span class="sxs-lookup"><span data-stu-id="758ab-112">inputStateDetailsSize</span></span>

<span data-ttu-id="758ab-113">Тип: **size_t**</span><span class="sxs-lookup"><span data-stu-id="758ab-113">Type: **size_t**</span></span>

<span data-ttu-id="758ab-114">Размер (в байтах) буфера сведений о входном состоянии, который вы (необязательно) выделяете и предоставляете в *инпутстатедетаилс*.</span><span class="sxs-lookup"><span data-stu-id="758ab-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="758ab-115">Инпутстатедетаилс [in]</span><span class="sxs-lookup"><span data-stu-id="758ab-115">inputStateDetails [in]</span></span>

<span data-ttu-id="758ab-116">Тип: **void const \***</span><span class="sxs-lookup"><span data-stu-id="758ab-116">Type: **void const\***</span></span>

<span data-ttu-id="758ab-117">Необязательный указатель на постоянный буфер сведений о состоянии ввода, который вы выделили в приложении, содержащий все сведения о запросе, необходимые для типа состояния, указанного в поле *штат*.</span><span class="sxs-lookup"><span data-stu-id="758ab-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="758ab-118">Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="758ab-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="758ab-119">аутпутбуфферсизе</span><span class="sxs-lookup"><span data-stu-id="758ab-119">outputBufferSize</span></span>

<span data-ttu-id="758ab-120">Тип: **size_t**</span><span class="sxs-lookup"><span data-stu-id="758ab-120">Type: **size_t**</span></span>

<span data-ttu-id="758ab-121">Размер (в байтах) выходного буфера, который вы выделили и предоставляющих в *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="758ab-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="758ab-122">outputBuffer [out]</span><span class="sxs-lookup"><span data-stu-id="758ab-122">outputBuffer [out]</span></span>

<span data-ttu-id="758ab-123">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="758ab-123">Type: **void\***</span></span>

<span data-ttu-id="758ab-124">Указатель на выходной буфер, выделенный в приложении, и который заполняется функцией.</span><span class="sxs-lookup"><span data-stu-id="758ab-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="758ab-125">Дополнительные сведения о требованиях к выходному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="758ab-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="758ab-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="758ab-126">Returns</span></span>

<span data-ttu-id="758ab-127">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="758ab-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="758ab-128">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="758ab-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="758ab-129">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="758ab-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="758ab-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="758ab-130">Return value</span></span>|<span data-ttu-id="758ab-131">Описание</span><span class="sxs-lookup"><span data-stu-id="758ab-131">Description</span></span>|
|-|-|
|<span data-ttu-id="758ab-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="758ab-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="758ab-133">Адаптер больше не находится в допустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="758ab-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="758ab-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="758ab-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="758ab-135">Тип состояния, указанный в *состоянии* , не распознается данной операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="758ab-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="758ab-136">Вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="758ab-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="758ab-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="758ab-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="758ab-138">Тип состояния, указанный в *состоянии* , не поддерживается адаптером.</span><span class="sxs-lookup"><span data-stu-id="758ab-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="758ab-139">Вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="758ab-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="758ab-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="758ab-140">E_INVALIDARG</span></span>|<span data-ttu-id="758ab-141">Недостаточный размер буфера предоставляется для *outputBuffer* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).</span><span class="sxs-lookup"><span data-stu-id="758ab-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="758ab-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="758ab-142">E_POINTER</span></span>|<span data-ttu-id="758ab-143">`nullptr` был предоставлен для *outputBuffer* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).</span><span class="sxs-lookup"><span data-stu-id="758ab-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="758ab-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="758ab-144">Remarks</span></span>

<span data-ttu-id="758ab-145">Дополнительные сведения о каждом типе состояния адаптера и используемых входных и выходных данных см. в разделе [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="758ab-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="758ab-146">Эта функция обнуляет буфер *outputBuffer* перед заполнением.</span><span class="sxs-lookup"><span data-stu-id="758ab-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="758ab-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="758ab-147">See also</span></span>

<span data-ttu-id="758ab-148">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="758ab-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>