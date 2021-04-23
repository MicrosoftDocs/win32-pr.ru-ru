---
title: IDXCoreAdapter::SetState
description: Задает состояние указанного элемента на адаптере.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719136"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="33c55-103">Метод Идкскореадаптер:: SetState</span><span class="sxs-lookup"><span data-stu-id="33c55-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="33c55-104">Задает состояние указанного элемента на адаптере.</span><span class="sxs-lookup"><span data-stu-id="33c55-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="33c55-105">Перед вызовом **SetState** для типа свойства вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="33c55-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="33c55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33c55-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="33c55-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="33c55-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="33c55-108">state</span><span class="sxs-lookup"><span data-stu-id="33c55-108">state</span></span>

<span data-ttu-id="33c55-109">Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="33c55-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="33c55-110">Тип элемента состояния на адаптере, состояние которого вы хотите задать.</span><span class="sxs-lookup"><span data-stu-id="33c55-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="33c55-111">Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="33c55-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="33c55-112">инпутстатедетаилссизе</span><span class="sxs-lookup"><span data-stu-id="33c55-112">inputStateDetailsSize</span></span>

<span data-ttu-id="33c55-113">Тип: **size_t**</span><span class="sxs-lookup"><span data-stu-id="33c55-113">Type: **size_t**</span></span>

<span data-ttu-id="33c55-114">Размер (в байтах) буфера сведений о входном состоянии, который вы (необязательно) выделяете и предоставляете в *инпутстатедетаилс*.</span><span class="sxs-lookup"><span data-stu-id="33c55-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="33c55-115">Инпутстатедетаилс [in]</span><span class="sxs-lookup"><span data-stu-id="33c55-115">inputStateDetails [in]</span></span>

<span data-ttu-id="33c55-116">Тип: **void const \***</span><span class="sxs-lookup"><span data-stu-id="33c55-116">Type: **void const\***</span></span>

<span data-ttu-id="33c55-117">Необязательный указатель на постоянный буфер сведений о состоянии ввода, который вы выделили в приложении, содержащий все сведения о запросе, необходимые для типа состояния, указанного в поле *штат*.</span><span class="sxs-lookup"><span data-stu-id="33c55-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="33c55-118">Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="33c55-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="33c55-119">инпутдатасизе</span><span class="sxs-lookup"><span data-stu-id="33c55-119">inputDataSize</span></span>

<span data-ttu-id="33c55-120">Тип: **size_t**</span><span class="sxs-lookup"><span data-stu-id="33c55-120">Type: **size_t**</span></span>

<span data-ttu-id="33c55-121">Размер (в байтах) входного буфера, который вы выделили и предоставляющих в *inputData*.</span><span class="sxs-lookup"><span data-stu-id="33c55-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="33c55-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="33c55-122">inputData [in]</span></span>

<span data-ttu-id="33c55-123">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="33c55-123">Type: **void\***</span></span>

<span data-ttu-id="33c55-124">Указатель на входной буфер, выделенный в приложении, содержащий сведения о состоянии, которые необходимо задать для элемента состояния, тип которого указан в поле *штат*.</span><span class="sxs-lookup"><span data-stu-id="33c55-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="33c55-125">Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="33c55-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="33c55-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33c55-126">Returns</span></span>

<span data-ttu-id="33c55-127">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="33c55-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="33c55-128">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="33c55-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="33c55-129">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="33c55-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="33c55-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33c55-130">Return value</span></span>|<span data-ttu-id="33c55-131">Описание</span><span class="sxs-lookup"><span data-stu-id="33c55-131">Description</span></span>|
|-|-|
|<span data-ttu-id="33c55-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="33c55-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="33c55-133">Адаптер больше не находится в допустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="33c55-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="33c55-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="33c55-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="33c55-135">Тип состояния, указанный в *состоянии* , не распознается данной операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="33c55-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="33c55-136">Вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="33c55-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="33c55-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="33c55-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="33c55-138">Тип состояния, указанный в *состоянии* , не поддерживается адаптером.</span><span class="sxs-lookup"><span data-stu-id="33c55-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="33c55-139">Вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="33c55-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="33c55-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="33c55-140">E_INVALIDARG</span></span>|<span data-ttu-id="33c55-141">Недостаточный размер буфера предоставляется для *inputData* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).</span><span class="sxs-lookup"><span data-stu-id="33c55-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="33c55-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="33c55-142">E_POINTER</span></span>|<span data-ttu-id="33c55-143">`nullptr` был предоставлен для *inputData* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).</span><span class="sxs-lookup"><span data-stu-id="33c55-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="33c55-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33c55-144">See also</span></span>

<span data-ttu-id="33c55-145">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="33c55-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>