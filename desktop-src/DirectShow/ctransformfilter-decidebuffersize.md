---
description: Метод ДеЦидебуфферсизе задает требования к буферу выходного контакта.
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
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657431"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="2eae4-103">Ктрансформфилтер. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="2eae4-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="2eae4-104">`DecideBufferSize`Метод задает требования к буферу выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="2eae4-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eae4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eae4-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2eae4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eae4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eae4-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="2eae4-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="2eae4-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) на распределителье выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="2eae4-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="2eae4-109">*ппропинпутрекуест*</span><span class="sxs-lookup"><span data-stu-id="2eae4-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="2eae4-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу из нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2eae4-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eae4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eae4-111">Return value</span></span>

<span data-ttu-id="2eae4-112">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2eae4-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eae4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2eae4-113">Remarks</span></span>

<span data-ttu-id="2eae4-114">Метод [**ктрансформаутпутпин::D еЦидебуфферсизе**](ctransformoutputpin-decidebuffersize.md) для выходного контакта вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="2eae4-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="2eae4-115">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="2eae4-115">The derived class must implement this method.</span></span> <span data-ttu-id="2eae4-116">Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="2eae4-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2eae4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2eae4-117">Requirements</span></span>



| <span data-ttu-id="2eae4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2eae4-118">Requirement</span></span> | <span data-ttu-id="2eae4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2eae4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eae4-120">Header</span><span class="sxs-lookup"><span data-stu-id="2eae4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2eae4-121"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2eae4-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2eae4-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2eae4-122">Library</span></span><br/> | <dl> <span data-ttu-id="2eae4-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2eae4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eae4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eae4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eae4-125">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="2eae4-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




