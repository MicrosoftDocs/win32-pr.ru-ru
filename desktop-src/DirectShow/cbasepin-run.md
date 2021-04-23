---
description: Метод Run уведомляет ПИН-код о том, что фильтр выполняется.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Метод Кбасепин. Run (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668542"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="a4180-103">Кбасепин. Run, метод</span><span class="sxs-lookup"><span data-stu-id="a4180-103">CBasePin.Run method</span></span>

<span data-ttu-id="a4180-104">`Run`Метод уведомляет ПИН-код о том, что теперь фильтр работает.</span><span class="sxs-lookup"><span data-stu-id="a4180-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4180-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4180-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="a4180-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4180-107">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="a4180-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a4180-108">Время запуска, переданное методу [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) фильтра.</span><span class="sxs-lookup"><span data-stu-id="a4180-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4180-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4180-109">Return value</span></span>

<span data-ttu-id="a4180-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a4180-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4180-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4180-111">Remarks</span></span>

<span data-ttu-id="a4180-112">Когда фильтр переходит от приостановленного к выполняющемуся, класс [**кбасефилтер**](cbasefilter.md) вызывает этот метод для всех ПИН-кодов фильтра.</span><span class="sxs-lookup"><span data-stu-id="a4180-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="a4180-113">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="a4180-113">This method does nothing in the base class.</span></span> <span data-ttu-id="a4180-114">Производные классы могут переопределять этот метод.</span><span class="sxs-lookup"><span data-stu-id="a4180-114">Derived classes can override this method.</span></span> <span data-ttu-id="a4180-115">Например, ПИН-код может запустить рабочий поток, который доставляет образцы.</span><span class="sxs-lookup"><span data-stu-id="a4180-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="a4180-116">Внутреннее состояние диспетчера графа фильтра не обновляется до тех пор, пока эта функция-член не вернет значение, поэтому не проверяйте состояние из этого метода.</span><span class="sxs-lookup"><span data-stu-id="a4180-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4180-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a4180-117">Requirements</span></span>



| <span data-ttu-id="a4180-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a4180-118">Requirement</span></span> | <span data-ttu-id="a4180-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a4180-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4180-120">Header</span><span class="sxs-lookup"><span data-stu-id="a4180-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a4180-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4180-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4180-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4180-122">Library</span></span><br/> | <dl> <span data-ttu-id="a4180-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a4180-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4180-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4180-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4180-125">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="a4180-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




