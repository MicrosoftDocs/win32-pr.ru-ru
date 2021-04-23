---
description: Метод Комплетеконнект завершает соединение с входным закреплением.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Кдинамикаутпутпин. Комплетеконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658077"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="c1a2a-103">Кдинамикаутпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="c1a2a-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="c1a2a-104">`CompleteConnect`Метод завершает соединение с входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="c1a2a-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1a2a-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c1a2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1a2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a2a-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="c1a2a-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c1a2a-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="c1a2a-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a2a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1a2a-109">Return value</span></span>

<span data-ttu-id="c1a2a-110">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="c1a2a-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a2a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1a2a-111">Remarks</span></span>

<span data-ttu-id="c1a2a-112">Этот метод переопределяет метод [**кбасеаутпутпин:: комплетеконнект**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a2a-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="c1a2a-113">Для поддержки динамического повторного подключения этот метод фиксирует распределитель, если фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="c1a2a-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="c1a2a-114">В базовом классе соединения могут происходить только в том случае, если фильтр остановлен, поэтому распределитель всегда фиксируется в методе [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a2a-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a2a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c1a2a-115">Requirements</span></span>



| <span data-ttu-id="c1a2a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c1a2a-116">Requirement</span></span> | <span data-ttu-id="c1a2a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c1a2a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a2a-118">Header</span><span class="sxs-lookup"><span data-stu-id="c1a2a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c1a2a-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1a2a-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c1a2a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1a2a-120">Library</span></span><br/> | <dl> <span data-ttu-id="c1a2a-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c1a2a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a2a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1a2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a2a-123">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c1a2a-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




