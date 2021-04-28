---
description: Ктрансформфилтер. ДеЦидебуфферсизе, метод ДеЦидебуфферсизе устанавливает требования к буферу выходного контакта.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Ктрансформфилтер. ДеЦидебуфферсизе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095152"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="2ebe7-103">Ктрансформфилтер. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="2ebe7-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="2ebe7-104">`DecideBufferSize`Метод задает требования к буферу выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebe7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ebe7-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2ebe7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ebe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebe7-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="2ebe7-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="2ebe7-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) на распределителье выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="2ebe7-109">*ппропинпутрекуест*</span><span class="sxs-lookup"><span data-stu-id="2ebe7-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="2ebe7-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу из нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ebe7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ebe7-111">Return value</span></span>

<span data-ttu-id="2ebe7-112">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ebe7-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ebe7-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ebe7-113">Remarks</span></span>

<span data-ttu-id="2ebe7-114">Метод [**ктрансформаутпутпин::D еЦидебуфферсизе**](ctransformoutputpin-decidebuffersize.md) для выходного контакта вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="2ebe7-115">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="2ebe7-115">The derived class must implement this method.</span></span> <span data-ttu-id="2ebe7-116">Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="2ebe7-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebe7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2ebe7-117">Requirements</span></span>



| <span data-ttu-id="2ebe7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2ebe7-118">Requirement</span></span> | <span data-ttu-id="2ebe7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ebe7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebe7-120">Header</span><span class="sxs-lookup"><span data-stu-id="2ebe7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2ebe7-121"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ebe7-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ebe7-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ebe7-122">Library</span></span><br/> | <dl> <span data-ttu-id="2ebe7-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ebe7-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebe7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2ebe7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebe7-125">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="2ebe7-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




