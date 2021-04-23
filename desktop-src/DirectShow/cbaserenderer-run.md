---
description: Метод Run запускает фильтр.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Метод Кбасерендерер. Run (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669399"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="842b7-103">Кбасерендерер. Run, метод</span><span class="sxs-lookup"><span data-stu-id="842b7-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="842b7-104">`Run`Метод выполняет фильтр.</span><span class="sxs-lookup"><span data-stu-id="842b7-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="842b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="842b7-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="842b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="842b7-106">Parameters</span></span>

<span data-ttu-id="842b7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="842b7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="842b7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="842b7-108">Return value</span></span>

<span data-ttu-id="842b7-109">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="842b7-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="842b7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="842b7-110">Remarks</span></span>

<span data-ttu-id="842b7-111">Этот метод переопределяет метод [**кбасефилтер:: Run**](cbasefilter-run.md) .</span><span class="sxs-lookup"><span data-stu-id="842b7-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="842b7-112">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="842b7-112">It performs the following actions:</span></span>

-   <span data-ttu-id="842b7-113">Вызывает метод **кбасефилтер:: Run** .</span><span class="sxs-lookup"><span data-stu-id="842b7-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="842b7-114">Фиксирует распределитель.</span><span class="sxs-lookup"><span data-stu-id="842b7-114">Commits the allocator.</span></span> <span data-ttu-id="842b7-115">(См. [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="842b7-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="842b7-116">Если предыдущее состояние было остановлено, фильтр выпустит любой пример, который он удерживает.</span><span class="sxs-lookup"><span data-stu-id="842b7-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="842b7-117">(Образец больше не является допустимым.)</span><span class="sxs-lookup"><span data-stu-id="842b7-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="842b7-118">Вызывает метод [**кбасерендерер:: стартстреаминг**](cbaserenderer-startstreaming.md) и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="842b7-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="842b7-119">Если пример находится в состоянии ожидания, метод **стартстреаминг** планирует его для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="842b7-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="842b7-120">Если фильтр не подключен, он сразу же отправляет событие [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="842b7-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="842b7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="842b7-121">Requirements</span></span>



| <span data-ttu-id="842b7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="842b7-122">Requirement</span></span> | <span data-ttu-id="842b7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="842b7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842b7-124">Header</span><span class="sxs-lookup"><span data-stu-id="842b7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="842b7-125"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="842b7-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="842b7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="842b7-126">Library</span></span><br/> | <dl> <span data-ttu-id="842b7-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="842b7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842b7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="842b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842b7-129">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="842b7-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




