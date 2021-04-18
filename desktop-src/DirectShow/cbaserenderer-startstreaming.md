---
description: Метод Стартстреаминг инициирует потоковую передачу, когда фильтр переключается в состояние выполнения.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Кбасерендерер. Стартстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669340"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="a4dc5-103">Кбасерендерер. Стартстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="a4dc5-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="a4dc5-104">`StartStreaming`Метод инициирует потоковую передачу, когда фильтр переключается в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4dc5-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4dc5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4dc5-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="a4dc5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4dc5-106">Parameters</span></span>

<span data-ttu-id="a4dc5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a4dc5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4dc5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4dc5-108">Return value</span></span>

<span data-ttu-id="a4dc5-109">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4dc5-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4dc5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4dc5-110">Remarks</span></span>

<span data-ttu-id="a4dc5-111">Если фильтр имеет образец, он планирует подготовку к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a4dc5-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="a4dc5-112">В противном случае, если имеется ожидающее уведомление конца потока, фильтр отправляет событие [**\_ завершения EC**](ec-complete.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="a4dc5-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="a4dc5-113">Этот метод вызывает метод [**кбасерендерер:: онстартстреаминг**](cbaserenderer-onstartstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="a4dc5-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="a4dc5-114">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="a4dc5-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4dc5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a4dc5-115">Requirements</span></span>



| <span data-ttu-id="a4dc5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a4dc5-116">Requirement</span></span> | <span data-ttu-id="a4dc5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a4dc5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4dc5-118">Header</span><span class="sxs-lookup"><span data-stu-id="a4dc5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a4dc5-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4dc5-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4dc5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4dc5-120">Library</span></span><br/> | <dl> <span data-ttu-id="a4dc5-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a4dc5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4dc5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4dc5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4dc5-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="a4dc5-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




