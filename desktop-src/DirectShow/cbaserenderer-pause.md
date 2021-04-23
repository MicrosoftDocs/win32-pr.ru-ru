---
description: Метод Pause приостанавливает фильтр.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Метод Кбасерендерер. Pause (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669404"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="cacf5-103">Кбасерендерер. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="cacf5-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="cacf5-104">`Pause`Метод приостанавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="cacf5-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cacf5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cacf5-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="cacf5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cacf5-106">Parameters</span></span>

<span data-ttu-id="cacf5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cacf5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cacf5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cacf5-108">Return value</span></span>

<span data-ttu-id="cacf5-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cacf5-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cacf5-110">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cacf5-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="cacf5-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cacf5-111">Return code</span></span>                                                                             | <span data-ttu-id="cacf5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cacf5-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="cacf5-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cacf5-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cacf5-114">Переход завершен.</span><span class="sxs-lookup"><span data-stu-id="cacf5-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="cacf5-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cacf5-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cacf5-116">Переход не завершен.</span><span class="sxs-lookup"><span data-stu-id="cacf5-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cacf5-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cacf5-117">Remarks</span></span>

<span data-ttu-id="cacf5-118">Этот метод переопределяет метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="cacf5-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="cacf5-119">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cacf5-119">It performs the following steps:</span></span>

-   <span data-ttu-id="cacf5-120">Вызывает метод **кбасефилтер::P Аусе** .</span><span class="sxs-lookup"><span data-stu-id="cacf5-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="cacf5-121">Фиксирует распределитель.</span><span class="sxs-lookup"><span data-stu-id="cacf5-121">Commits the allocator.</span></span> <span data-ttu-id="cacf5-122">(См. [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="cacf5-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="cacf5-123">Если предыдущее состояние было остановлено, фильтр выпустит любой пример, который он удерживает.</span><span class="sxs-lookup"><span data-stu-id="cacf5-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="cacf5-124">(Образец больше не является допустимым.)</span><span class="sxs-lookup"><span data-stu-id="cacf5-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="cacf5-125">Вызывает метод [**кбасерендерер:: комплетестатечанже**](cbaserenderer-completestatechange.md) и возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cacf5-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacf5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cacf5-126">Requirements</span></span>



| <span data-ttu-id="cacf5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cacf5-127">Requirement</span></span> | <span data-ttu-id="cacf5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cacf5-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cacf5-129">Header</span><span class="sxs-lookup"><span data-stu-id="cacf5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cacf5-130"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cacf5-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cacf5-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cacf5-131">Library</span></span><br/> | <dl> <span data-ttu-id="cacf5-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cacf5-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cacf5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cacf5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacf5-134">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="cacf5-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




