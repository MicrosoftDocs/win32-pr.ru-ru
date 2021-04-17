---
description: Метод Онваитенд вызывается, когда фильтр выполняется в ожидании времени презентации в примере.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Кбасерендерер. Онваитенд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669406"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="bcdc9-103">Кбасерендерер. Онваитенд, метод</span><span class="sxs-lookup"><span data-stu-id="bcdc9-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="bcdc9-104">`OnWaitEnd`Метод вызывается, когда фильтр выполняется в ожидании времени презентации в примере.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcdc9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcdc9-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="bcdc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcdc9-106">Parameters</span></span>

<span data-ttu-id="bcdc9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcdc9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcdc9-108">Return value</span></span>

<span data-ttu-id="bcdc9-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcdc9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcdc9-110">Remarks</span></span>

<span data-ttu-id="bcdc9-111">Метод [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) вызывает этот метод, когда он завершает ожидание времени презентации в примере.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="bcdc9-112">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="bcdc9-113">Если вы реализуете контроль качества, вы можете переопределить этот метод вместе с методом [**кбасерендерер:: онваитстарт**](cbaserenderer-onwaitstart.md) .</span><span class="sxs-lookup"><span data-stu-id="bcdc9-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="bcdc9-114">Эти методы можно использовать для наблюдения за производительностью фильтра.</span><span class="sxs-lookup"><span data-stu-id="bcdc9-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcdc9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bcdc9-115">Requirements</span></span>



| <span data-ttu-id="bcdc9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bcdc9-116">Requirement</span></span> | <span data-ttu-id="bcdc9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bcdc9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdc9-118">Header</span><span class="sxs-lookup"><span data-stu-id="bcdc9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bcdc9-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc9-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bcdc9-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bcdc9-120">Library</span></span><br/> | <dl> <span data-ttu-id="bcdc9-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcdc9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcdc9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcdc9-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="bcdc9-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




