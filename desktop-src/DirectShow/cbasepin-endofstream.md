---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream. Вызывайте этот метод только для входных ПИН-кодов.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Кбасепин. EndOfStream, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669303"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="58241-105">Кбасепин. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="58241-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="58241-106">`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="58241-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="58241-107">Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="58241-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="58241-108">Вызывайте этот метод только для входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="58241-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="58241-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58241-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="58241-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="58241-110">Parameters</span></span>

<span data-ttu-id="58241-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="58241-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58241-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58241-112">Return value</span></span>

<span data-ttu-id="58241-113">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="58241-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="58241-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58241-114">Remarks</span></span>

<span data-ttu-id="58241-115">Фильтр должен передавать уведомления о завершении потока в подчиненные входные контакты подключенных фильтров.</span><span class="sxs-lookup"><span data-stu-id="58241-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="58241-116">Если фильтр является модулем подготовки отчетов, он должен опубликовать уведомление о событии [**EC \_ Complete**](ec-complete.md) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="58241-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="58241-117">Дополнительные сведения см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="58241-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="58241-118">В базовом классе этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="58241-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="58241-119">Производные классы должны переопределять этот метод.</span><span class="sxs-lookup"><span data-stu-id="58241-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="58241-120">Требования</span><span class="sxs-lookup"><span data-stu-id="58241-120">Requirements</span></span>



| <span data-ttu-id="58241-121">Требование</span><span class="sxs-lookup"><span data-stu-id="58241-121">Requirement</span></span> | <span data-ttu-id="58241-122">Значение</span><span class="sxs-lookup"><span data-stu-id="58241-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58241-123">Header</span><span class="sxs-lookup"><span data-stu-id="58241-123">Header</span></span><br/>  | <dl> <span data-ttu-id="58241-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58241-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="58241-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="58241-125">Library</span></span><br/> | <dl> <span data-ttu-id="58241-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="58241-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58241-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58241-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58241-128">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="58241-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




