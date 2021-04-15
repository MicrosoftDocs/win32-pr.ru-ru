---
description: Метод Онстопстреаминг вызывается, когда фильтр останавливает потоковую передачу.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Кбасерендерер. Онстопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669408"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="82676-103">Кбасерендерер. Онстопстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="82676-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="82676-104">`OnStopStreaming`Метод вызывается, когда фильтр останавливает потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="82676-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="82676-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82676-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="82676-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82676-106">Parameters</span></span>

<span data-ttu-id="82676-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="82676-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82676-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82676-108">Return value</span></span>

<span data-ttu-id="82676-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="82676-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="82676-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82676-110">Remarks</span></span>

<span data-ttu-id="82676-111">Метод [**кбасерендерер:: стопстреаминг**](cbaserenderer-stopstreaming.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="82676-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="82676-112">Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="82676-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="82676-113">Требования</span><span class="sxs-lookup"><span data-stu-id="82676-113">Requirements</span></span>



| <span data-ttu-id="82676-114">Требование</span><span class="sxs-lookup"><span data-stu-id="82676-114">Requirement</span></span> | <span data-ttu-id="82676-115">Значение</span><span class="sxs-lookup"><span data-stu-id="82676-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82676-116">Header</span><span class="sxs-lookup"><span data-stu-id="82676-116">Header</span></span><br/>  | <dl> <span data-ttu-id="82676-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82676-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82676-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82676-118">Library</span></span><br/> | <dl> <span data-ttu-id="82676-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="82676-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82676-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82676-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82676-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="82676-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




