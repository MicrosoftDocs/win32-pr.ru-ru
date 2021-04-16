---
title: IDXCoreAdapter::GetPropertySize
description: Для указанного свойства адаптера получает размер буфера в байтах, необходимого для вызова метода [Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719126"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="88539-103">Метод Идкскореадаптер:: Жетпропертисизе</span><span class="sxs-lookup"><span data-stu-id="88539-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="88539-104">Для указанного свойства адаптера получает размер буфера в байтах, необходимого для вызова метода [Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="88539-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="88539-105">Перед вызовом **жетпропертисизе** для типа свойства вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="88539-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="88539-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88539-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="88539-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="88539-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="88539-108">свойство;</span><span class="sxs-lookup"><span data-stu-id="88539-108">property</span></span>

<span data-ttu-id="88539-109">Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="88539-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="88539-110">Тип свойства, размер которого требуется получить в байтах.</span><span class="sxs-lookup"><span data-stu-id="88539-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="88539-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="88539-111">bufferSize [out]</span></span>

<span data-ttu-id="88539-112">Тип: **size_t \***</span><span class="sxs-lookup"><span data-stu-id="88539-112">Type: **size_t\***</span></span>

<span data-ttu-id="88539-113">Указатель на значение **size_t** .</span><span class="sxs-lookup"><span data-stu-id="88539-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="88539-114">Функция отменяет ссылку на указатель и задает для него значение размера (в байтах) выходного буфера, который необходимо выделить, и передать в качестве аргумента *PropertyData* в вызове метода [IsReference.](./nf-dxcore_interface-idxcoreadapter-getproperty.md)</span><span class="sxs-lookup"><span data-stu-id="88539-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="88539-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88539-115">Returns</span></span>

<span data-ttu-id="88539-116">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="88539-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="88539-117">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="88539-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="88539-118">В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="88539-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="88539-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88539-119">Return value</span></span>|<span data-ttu-id="88539-120">Описание</span><span class="sxs-lookup"><span data-stu-id="88539-120">Description</span></span>|
|-|-|
|<span data-ttu-id="88539-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="88539-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="88539-122">Тип свойства, указанный в *свойстве* , не распознается данной операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="88539-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="88539-123">Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="88539-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="88539-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="88539-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="88539-125">Тип свойства, указанный в *свойстве* , не поддерживается адаптером.</span><span class="sxs-lookup"><span data-stu-id="88539-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="88539-126">Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="88539-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="88539-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="88539-127">E_POINTER</span></span>|<span data-ttu-id="88539-128">`nullptr` был предоставлен для *bufferSize*.</span><span class="sxs-lookup"><span data-stu-id="88539-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="88539-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88539-129">Remarks</span></span>

<span data-ttu-id="88539-130">Вы можете вызвать **жетпропертисизе** на адаптере, который больше не является допустимым &mdash; , функция не завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="88539-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="88539-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88539-131">See also</span></span>

<span data-ttu-id="88539-132">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="88539-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>