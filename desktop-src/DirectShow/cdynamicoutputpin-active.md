---
description: Кдинамикаутпутпин. Active Method — активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Метод Кдинамикаутпутпин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099332"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="0ff74-103">Кдинамикаутпутпин. активный метод</span><span class="sxs-lookup"><span data-stu-id="0ff74-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="0ff74-104">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="0ff74-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ff74-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="0ff74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ff74-106">Parameters</span></span>

<span data-ttu-id="0ff74-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ff74-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ff74-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ff74-108">Return value</span></span>

<span data-ttu-id="0ff74-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ff74-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0ff74-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0ff74-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0ff74-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0ff74-111">Return code</span></span>                                                                            | <span data-ttu-id="0ff74-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0ff74-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ff74-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff74-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0ff74-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0ff74-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ff74-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff74-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0ff74-116">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="0ff74-116">Failure.</span></span> <span data-ttu-id="0ff74-117">[**Кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md) не был вызван.</span><span class="sxs-lookup"><span data-stu-id="0ff74-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ff74-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="0ff74-118">Remarks</span></span>

<span data-ttu-id="0ff74-119">Этот метод переопределяет метод [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff74-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="0ff74-120">Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff74-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="0ff74-121">Если фильтр-владелец не вызвал **сетконфигинфо**, этот метод возвращает значение E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="0ff74-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff74-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0ff74-122">Requirements</span></span>



| <span data-ttu-id="0ff74-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0ff74-123">Requirement</span></span> | <span data-ttu-id="0ff74-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0ff74-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff74-125">Header</span><span class="sxs-lookup"><span data-stu-id="0ff74-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff74-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff74-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ff74-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ff74-127">Library</span></span><br/> | <dl> <span data-ttu-id="0ff74-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff74-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff74-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0ff74-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff74-130">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="0ff74-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




