---
description: Метод Онваитстарт вызывается, когда фильтр начинает ожидание времени презентации в примере.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Кбасерендерер. Онваитстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669405"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="7b5fd-103">Кбасерендерер. Онваитстарт, метод</span><span class="sxs-lookup"><span data-stu-id="7b5fd-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="7b5fd-104">`OnWaitStart`Метод вызывается, когда фильтр начинает ожидание времени презентации в примере.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b5fd-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="7b5fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b5fd-106">Parameters</span></span>

<span data-ttu-id="7b5fd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b5fd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b5fd-108">Return value</span></span>

<span data-ttu-id="7b5fd-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5fd-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b5fd-110">Remarks</span></span>

<span data-ttu-id="7b5fd-111">Метод [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) вызывает этот метод, когда он начинает ожидание времени презентации в примере.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="7b5fd-112">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="7b5fd-113">Если вы реализуете контроль качества, вы можете переопределить этот метод вместе с методом [**кбасерендерер:: онваитенд**](cbaserenderer-onwaitend.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5fd-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="7b5fd-114">Эти методы можно использовать для наблюдения за производительностью фильтра.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5fd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7b5fd-115">Requirements</span></span>



| <span data-ttu-id="7b5fd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7b5fd-116">Requirement</span></span> | <span data-ttu-id="7b5fd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7b5fd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5fd-118">Header</span><span class="sxs-lookup"><span data-stu-id="7b5fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7b5fd-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b5fd-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b5fd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b5fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="7b5fd-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7b5fd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b5fd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b5fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5fd-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="7b5fd-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




