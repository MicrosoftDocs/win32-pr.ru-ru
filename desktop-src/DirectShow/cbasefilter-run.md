---
description: 'Метод Run запускает фильтр. Этот метод реализует метод Имедиафилтер:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Метод Кбасефилтер. Run (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657157"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="13f59-104">Кбасефилтер. Run, метод</span><span class="sxs-lookup"><span data-stu-id="13f59-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="13f59-105">`Run`Метод выполняет фильтр.</span><span class="sxs-lookup"><span data-stu-id="13f59-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="13f59-106">Этот метод реализует метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="13f59-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13f59-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="13f59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13f59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f59-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="13f59-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="13f59-110">Время в ссылке, соответствующее времени потока 0.</span><span class="sxs-lookup"><span data-stu-id="13f59-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13f59-111">Return value</span></span>

<span data-ttu-id="13f59-112">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="13f59-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f59-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13f59-113">Remarks</span></span>

<span data-ttu-id="13f59-114">Если фильтр остановлен, этот метод приостанавливает фильтр, вызывая метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="13f59-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="13f59-115">Затем он вызывает метод [**кбасепин:: Run**](cbasepin-run.md) для каждого подключенного контакта фильтра.</span><span class="sxs-lookup"><span data-stu-id="13f59-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="13f59-116">Наконец, он устанавливает переменную члена [**\_ состояния кбасефилтер:: m**](cbasefilter-m-state.md) в состояние \_ работает.</span><span class="sxs-lookup"><span data-stu-id="13f59-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="13f59-117">Время потока вычисляется как текущее время ссылки минус *тстарт*.</span><span class="sxs-lookup"><span data-stu-id="13f59-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="13f59-118">Пример носителя с нулевой меткой времени должен быть визуализирован во время *тстарт*.</span><span class="sxs-lookup"><span data-stu-id="13f59-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f59-119">Требования</span><span class="sxs-lookup"><span data-stu-id="13f59-119">Requirements</span></span>



| <span data-ttu-id="13f59-120">Требование</span><span class="sxs-lookup"><span data-stu-id="13f59-120">Requirement</span></span> | <span data-ttu-id="13f59-121">Значение</span><span class="sxs-lookup"><span data-stu-id="13f59-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f59-122">Header</span><span class="sxs-lookup"><span data-stu-id="13f59-122">Header</span></span><br/>  | <dl> <span data-ttu-id="13f59-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13f59-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="13f59-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13f59-124">Library</span></span><br/> | <dl> <span data-ttu-id="13f59-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="13f59-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f59-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13f59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f59-127">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="13f59-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




