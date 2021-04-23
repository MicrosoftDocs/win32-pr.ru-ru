---
title: IDXCoreAdapter::GetProperty
description: Извлекает значение указанного свойства адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338977"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="d0078-103">Идкскореадаптер:: метод Property</span><span class="sxs-lookup"><span data-stu-id="d0078-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="d0078-104">Извлекает значение указанного свойства адаптера.</span><span class="sxs-lookup"><span data-stu-id="d0078-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="d0078-105">Перед вызовом метода **Property** для типа свойства вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="d0078-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="d0078-106">Кроме того, перед вызовом метода **Property** вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить необходимый размер буфера, в котором будет получено значение свойства.</span><span class="sxs-lookup"><span data-stu-id="d0078-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0078-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0078-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="d0078-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0078-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="d0078-109">свойство;</span><span class="sxs-lookup"><span data-stu-id="d0078-109">property</span></span>

<span data-ttu-id="d0078-110">Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="d0078-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="d0078-111">Тип свойства, значение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="d0078-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="d0078-112">Дополнительные сведения о каждом свойстве адаптера см. в таблице в [дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d0078-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="d0078-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="d0078-113">bufferSize</span></span>

<span data-ttu-id="d0078-114">Тип: **size_t**</span><span class="sxs-lookup"><span data-stu-id="d0078-114">Type: **size_t**</span></span>

<span data-ttu-id="d0078-115">Размер (в байтах) выходного буфера, который вы выделили и предоставляющих в *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="d0078-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="d0078-116">propertyData [out]</span><span class="sxs-lookup"><span data-stu-id="d0078-116">propertyData [out]</span></span>

<span data-ttu-id="d0078-117">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="d0078-117">Type: **void\***</span></span>

<span data-ttu-id="d0078-118">Указатель на выходной буфер, выделенный в приложении, и который заполняется функцией.</span><span class="sxs-lookup"><span data-stu-id="d0078-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="d0078-119">Вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить размер буфера *PropertyData* для заданного свойства адаптера.</span><span class="sxs-lookup"><span data-stu-id="d0078-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="d0078-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0078-120">Returns</span></span>

<span data-ttu-id="d0078-121">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="d0078-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="d0078-122">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="d0078-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d0078-123">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d0078-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="d0078-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0078-124">Return value</span></span>|<span data-ttu-id="d0078-125">Описание</span><span class="sxs-lookup"><span data-stu-id="d0078-125">Description</span></span>|
|-|-|
|<span data-ttu-id="d0078-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="d0078-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="d0078-127">Тип свойства, указанный в *свойстве* , не распознается данной операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="d0078-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="d0078-128">Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="d0078-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="d0078-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d0078-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="d0078-130">Тип свойства, указанный в *свойстве* , не поддерживается адаптером.</span><span class="sxs-lookup"><span data-stu-id="d0078-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="d0078-131">Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="d0078-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="d0078-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d0078-132">E_INVALIDARG</span></span>|<span data-ttu-id="d0078-133">Недостаточный размер буфера указан в *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="d0078-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="d0078-134">Вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить размер буфера *PropertyData* для заданного свойства адаптера.</span><span class="sxs-lookup"><span data-stu-id="d0078-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="d0078-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="d0078-135">E_POINTER</span></span>|<span data-ttu-id="d0078-136">`nullptr` был предоставлен для *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="d0078-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d0078-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0078-137">Remarks</span></span>

<span data-ttu-id="d0078-138">Вы можете вызвать метод **Property** для адаптера, который больше не является допустимым &mdash; . в результате эта функция не будет завершаться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d0078-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="d0078-139">Эта функция обнуляет буфер *PropertyData* перед заполнением.</span><span class="sxs-lookup"><span data-stu-id="d0078-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0078-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0078-140">See also</span></span>

<span data-ttu-id="d0078-141">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="d0078-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>