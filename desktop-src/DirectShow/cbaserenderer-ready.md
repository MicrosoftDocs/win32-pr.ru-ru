---
description: Метод Ready сигнализирует о завершении перехода состояния.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Метод Кбасерендерер. ready (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658050"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="b2629-103">Кбасерендерер. ready, метод</span><span class="sxs-lookup"><span data-stu-id="b2629-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="b2629-104">`Ready`Метод сигнализирует о завершении перехода состояния.</span><span class="sxs-lookup"><span data-stu-id="b2629-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2629-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2629-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="b2629-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2629-106">Parameters</span></span>

<span data-ttu-id="b2629-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b2629-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2629-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2629-108">Return value</span></span>

<span data-ttu-id="b2629-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b2629-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2629-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2629-110">Remarks</span></span>

<span data-ttu-id="b2629-111">Этот метод приводит к тому, что метод [**кбасерендерер::**](cbaserenderer-getstate.md) noreturn возвращает значение S \_ OK, что означает, что фильтр завершил переход в текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="b2629-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="b2629-112">Фильтр вызывает этот метод при каждом завершении смены состояния.</span><span class="sxs-lookup"><span data-stu-id="b2629-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2629-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b2629-113">Requirements</span></span>



| <span data-ttu-id="b2629-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b2629-114">Requirement</span></span> | <span data-ttu-id="b2629-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b2629-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2629-116">Header</span><span class="sxs-lookup"><span data-stu-id="b2629-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b2629-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2629-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2629-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2629-118">Library</span></span><br/> | <dl> <span data-ttu-id="b2629-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b2629-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2629-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2629-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2629-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="b2629-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="b2629-122">**Кбасерендерер:: Чеккреади**</span><span class="sxs-lookup"><span data-stu-id="b2629-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="b2629-123">**Кбасерендерер:: NotReady**</span><span class="sxs-lookup"><span data-stu-id="b2629-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




