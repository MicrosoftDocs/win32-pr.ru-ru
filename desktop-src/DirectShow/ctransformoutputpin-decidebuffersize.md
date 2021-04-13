---
description: Метод ДеЦидебуфферсизе задает требования к буферу.
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657727"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="591ed-103">Ктрансформаутпутпин. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="591ed-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="591ed-104">`DecideBufferSize`Метод задает требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="591ed-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="591ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="591ed-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="591ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="591ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="591ed-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="591ed-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="591ed-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="591ed-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="591ed-109">*ппропинпутрекуест*</span><span class="sxs-lookup"><span data-stu-id="591ed-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="591ed-110">Указатель на [**структуру \_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта.</span><span class="sxs-lookup"><span data-stu-id="591ed-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="591ed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="591ed-111">Return value</span></span>

<span data-ttu-id="591ed-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="591ed-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="591ed-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="591ed-113">Remarks</span></span>

<span data-ttu-id="591ed-114">Этот метод переопределяет метод [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="591ed-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="591ed-115">Он вызывает чисто виртуальный метод [**ктрансформфилтер::D еЦидебуфферсизе**](ctransformfilter-decidebuffersize.md) для фильтра, который должен реализовываться производным классом фильтра.</span><span class="sxs-lookup"><span data-stu-id="591ed-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="591ed-116">Требования</span><span class="sxs-lookup"><span data-stu-id="591ed-116">Requirements</span></span>



| <span data-ttu-id="591ed-117">Требование</span><span class="sxs-lookup"><span data-stu-id="591ed-117">Requirement</span></span> | <span data-ttu-id="591ed-118">Значение</span><span class="sxs-lookup"><span data-stu-id="591ed-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="591ed-119">Header</span><span class="sxs-lookup"><span data-stu-id="591ed-119">Header</span></span><br/>  | <dl> <span data-ttu-id="591ed-120"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="591ed-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="591ed-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="591ed-121">Library</span></span><br/> | <dl> <span data-ttu-id="591ed-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="591ed-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




