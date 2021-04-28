---
description: Кдинамикаутпутпин. Комплетеконнект, метод Комплетеконнект завершает соединение с входным закреплением.
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
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095742"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="88392-103">Кдинамикаутпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="88392-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="88392-104">`CompleteConnect`Метод завершает соединение с входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="88392-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="88392-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88392-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="88392-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88392-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="88392-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="88392-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="88392-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88392-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88392-109">Return value</span></span>

<span data-ttu-id="88392-110">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="88392-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="88392-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="88392-111">Remarks</span></span>

<span data-ttu-id="88392-112">Этот метод переопределяет метод [**кбасеаутпутпин:: комплетеконнект**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="88392-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="88392-113">Для поддержки динамического повторного подключения этот метод фиксирует распределитель, если фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="88392-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="88392-114">В базовом классе соединения могут происходить только в том случае, если фильтр остановлен, поэтому распределитель всегда фиксируется в методе [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="88392-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88392-115">Требования</span><span class="sxs-lookup"><span data-stu-id="88392-115">Requirements</span></span>



| <span data-ttu-id="88392-116">Требование</span><span class="sxs-lookup"><span data-stu-id="88392-116">Requirement</span></span> | <span data-ttu-id="88392-117">Значение</span><span class="sxs-lookup"><span data-stu-id="88392-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88392-118">Header</span><span class="sxs-lookup"><span data-stu-id="88392-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88392-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88392-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88392-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88392-120">Library</span></span><br/> | <dl> <span data-ttu-id="88392-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="88392-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88392-122">См. также</span><span class="sxs-lookup"><span data-stu-id="88392-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88392-123">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="88392-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




