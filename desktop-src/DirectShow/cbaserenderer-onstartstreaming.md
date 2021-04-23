---
description: Метод Онстартстреаминг вызывается, когда фильтр начинает потоковую передачу.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Кбасерендерер. Онстартстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657293"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="ca659-103">Кбасерендерер. Онстартстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="ca659-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="ca659-104">`OnStartStreaming`Метод вызывается, когда фильтр начинает потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="ca659-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca659-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="ca659-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca659-106">Parameters</span></span>

<span data-ttu-id="ca659-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ca659-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca659-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca659-108">Return value</span></span>

<span data-ttu-id="ca659-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ca659-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca659-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca659-110">Remarks</span></span>

<span data-ttu-id="ca659-111">Метод [**кбасерендерер:: стартстреаминг**](cbaserenderer-startstreaming.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="ca659-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="ca659-112">Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="ca659-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca659-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ca659-113">Requirements</span></span>



| <span data-ttu-id="ca659-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ca659-114">Requirement</span></span> | <span data-ttu-id="ca659-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ca659-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca659-116">Header</span><span class="sxs-lookup"><span data-stu-id="ca659-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ca659-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca659-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca659-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca659-118">Library</span></span><br/> | <dl> <span data-ttu-id="ca659-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ca659-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca659-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca659-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca659-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="ca659-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




