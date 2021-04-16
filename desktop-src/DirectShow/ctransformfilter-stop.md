---
description: 'Останавливает фильтр. Этот метод реализует метод Имедиафилтер:: останавливаться.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: Метод Ктрансформфилтер. останавливаться (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679630"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="cf709-104">Ктрансформфилтер. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="cf709-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="cf709-105">Останавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="cf709-105">Stops the filter.</span></span> <span data-ttu-id="cf709-106">Этот метод реализует метод [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="cf709-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf709-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf709-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="cf709-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf709-108">Parameters</span></span>

<span data-ttu-id="cf709-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cf709-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf709-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf709-110">Return value</span></span>

<span data-ttu-id="cf709-111">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf709-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf709-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf709-112">Remarks</span></span>

<span data-ttu-id="cf709-113">После того как этот метод отменяет фиксацию обоих распределительов, он вызывает метод [**стопстреаминг**](ctransformfilter-stopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="cf709-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="cf709-114">Метод **стопстреаминг** не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="cf709-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf709-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cf709-115">Requirements</span></span>



| <span data-ttu-id="cf709-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cf709-116">Requirement</span></span> | <span data-ttu-id="cf709-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf709-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf709-118">Header</span><span class="sxs-lookup"><span data-stu-id="cf709-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cf709-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf709-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf709-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf709-120">Library</span></span><br/> | <dl> <span data-ttu-id="cf709-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cf709-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf709-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf709-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf709-123">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="cf709-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




