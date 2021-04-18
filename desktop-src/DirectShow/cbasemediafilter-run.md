---
description: 'Метод Run запускает объект. Этот метод реализует метод Имедиафилтер:: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Метод Кбасемедиафилтер. Run (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656925"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="6ccae-104">Кбасемедиафилтер. Run, метод</span><span class="sxs-lookup"><span data-stu-id="6ccae-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="6ccae-105">`Run`Метод выполняет объект.</span><span class="sxs-lookup"><span data-stu-id="6ccae-105">The `Run` method runs the object.</span></span> <span data-ttu-id="6ccae-106">Этот метод реализует метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="6ccae-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ccae-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="6ccae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ccae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccae-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="6ccae-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccae-110">Время в ссылке, соответствующее времени потока 0.</span><span class="sxs-lookup"><span data-stu-id="6ccae-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ccae-111">Return value</span></span>

<span data-ttu-id="6ccae-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6ccae-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ccae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ccae-113">Remarks</span></span>

<span data-ttu-id="6ccae-114">Если объект остановлен, этот метод приостанавливает работу объекта, вызывая метод [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="6ccae-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="6ccae-115">Затем он задает для переменной члена [**\_ состояния кбасемедиафилтер:: m**](cbasemediafilter-m-state.md) состояние \_ работает.</span><span class="sxs-lookup"><span data-stu-id="6ccae-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="6ccae-116">Время потока вычисляется как текущее время ссылки минус *тстарт*.</span><span class="sxs-lookup"><span data-stu-id="6ccae-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="6ccae-117">Пример носителя с нулевой меткой времени должен быть визуализирован во время *тстарт*.</span><span class="sxs-lookup"><span data-stu-id="6ccae-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccae-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6ccae-118">Requirements</span></span>



| <span data-ttu-id="6ccae-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6ccae-119">Requirement</span></span> | <span data-ttu-id="6ccae-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6ccae-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccae-121">Header</span><span class="sxs-lookup"><span data-stu-id="6ccae-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6ccae-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccae-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ccae-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ccae-123">Library</span></span><br/> | <dl> <span data-ttu-id="6ccae-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccae-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ccae-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ccae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccae-126">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="6ccae-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




