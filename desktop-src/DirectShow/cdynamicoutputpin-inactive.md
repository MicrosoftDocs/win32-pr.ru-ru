---
description: Неактивный метод уведомляет ПИН-код о том, что фильтр остановлен.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Метод Кдинамикаутпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665081"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="94a36-103">Кдинамикаутпутпин. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="94a36-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="94a36-104">`Inactive`Метод уведомляет ПИН-код о том, что фильтр остановлен.</span><span class="sxs-lookup"><span data-stu-id="94a36-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a36-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94a36-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="94a36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94a36-106">Parameters</span></span>

<span data-ttu-id="94a36-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="94a36-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94a36-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94a36-108">Return value</span></span>

<span data-ttu-id="94a36-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="94a36-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a36-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94a36-110">Remarks</span></span>

<span data-ttu-id="94a36-111">Этот метод переопределяет метод [**кбасеаутпутпин:: Inactive**](cbaseoutputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="94a36-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="94a36-112">Он устанавливает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="94a36-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a36-113">Требования</span><span class="sxs-lookup"><span data-stu-id="94a36-113">Requirements</span></span>



| <span data-ttu-id="94a36-114">Требование</span><span class="sxs-lookup"><span data-stu-id="94a36-114">Requirement</span></span> | <span data-ttu-id="94a36-115">Значение</span><span class="sxs-lookup"><span data-stu-id="94a36-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a36-116">Header</span><span class="sxs-lookup"><span data-stu-id="94a36-116">Header</span></span><br/>  | <dl> <span data-ttu-id="94a36-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94a36-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94a36-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94a36-118">Library</span></span><br/> | <dl> <span data-ttu-id="94a36-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="94a36-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a36-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94a36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a36-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="94a36-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




