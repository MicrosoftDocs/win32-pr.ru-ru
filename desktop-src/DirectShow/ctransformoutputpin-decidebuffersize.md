---
description: Ктрансформаутпутпин. ДеЦидебуфферсизе, метод ДеЦидебуфферсизе задает требования к буферу.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Ктрансформаутпутпин. ДеЦидебуфферсизе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084842"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="59ba8-103">Ктрансформаутпутпин. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="59ba8-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="59ba8-104">`DecideBufferSize`Метод задает требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="59ba8-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ba8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59ba8-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="59ba8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59ba8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ba8-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="59ba8-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="59ba8-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="59ba8-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="59ba8-109">*ппропинпутрекуест*</span><span class="sxs-lookup"><span data-stu-id="59ba8-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="59ba8-110">Указатель на [**структуру \_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта.</span><span class="sxs-lookup"><span data-stu-id="59ba8-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ba8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59ba8-111">Return value</span></span>

<span data-ttu-id="59ba8-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59ba8-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ba8-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="59ba8-113">Remarks</span></span>

<span data-ttu-id="59ba8-114">Этот метод переопределяет метод [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="59ba8-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="59ba8-115">Он вызывает чисто виртуальный метод [**ктрансформфилтер::D еЦидебуфферсизе**](ctransformfilter-decidebuffersize.md) для фильтра, который должен реализовываться производным классом фильтра.</span><span class="sxs-lookup"><span data-stu-id="59ba8-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ba8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="59ba8-116">Requirements</span></span>



| <span data-ttu-id="59ba8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="59ba8-117">Requirement</span></span> | <span data-ttu-id="59ba8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="59ba8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ba8-119">Header</span><span class="sxs-lookup"><span data-stu-id="59ba8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="59ba8-120"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59ba8-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59ba8-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59ba8-121">Library</span></span><br/> | <dl> <span data-ttu-id="59ba8-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="59ba8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




