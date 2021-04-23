---
description: Метод Исендофстреамделиверед запрашивает, \_ доставлено ли событие EC Complete диспетчеру графа фильтров.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Кбасерендерер. Исендофстреамделиверед, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668866"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a><span data-ttu-id="c7e30-103">Кбасерендерер. Исендофстреамделиверед, метод</span><span class="sxs-lookup"><span data-stu-id="c7e30-103">CBaseRenderer.IsEndOfStreamDelivered method</span></span>

<span data-ttu-id="c7e30-104">`IsEndOfStreamDelivered`Метод запрашивает, \_ доставлено ли событие EC Complete диспетчеру графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="c7e30-104">The `IsEndOfStreamDelivered` method queries whether the EC\_COMPLETE event has been delivered to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7e30-105">Syntax</span></span>


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a><span data-ttu-id="c7e30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7e30-106">Parameters</span></span>

<span data-ttu-id="c7e30-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c7e30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7e30-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7e30-108">Return value</span></span>

<span data-ttu-id="c7e30-109">Возвращает флаг [**\_ беосделиверед кбасерендерер:: m**](cbaserenderer-m-beosdelivered.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e30-109">Returns the [**CBaseRenderer::m\_bEOSDelivered**](cbaserenderer-m-beosdelivered.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e30-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c7e30-110">Requirements</span></span>



| <span data-ttu-id="c7e30-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c7e30-111">Requirement</span></span> | <span data-ttu-id="c7e30-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c7e30-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e30-113">Header</span><span class="sxs-lookup"><span data-stu-id="c7e30-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c7e30-114"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e30-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7e30-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7e30-115">Library</span></span><br/> | <dl> <span data-ttu-id="c7e30-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e30-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e30-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7e30-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e30-118">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="c7e30-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




