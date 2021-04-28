---
description: Ктрансформфилтер. Pause, метод Pause приостанавливает фильтр. Этот метод реализует метод Имедиафилтер::P Аусе.
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Метод Ктрансформфилтер. Pause (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095102"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="f8b13-104">Ктрансформфилтер. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="f8b13-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="f8b13-105">`Pause`Метод приостанавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="f8b13-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="f8b13-106">Этот метод реализует метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="f8b13-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b13-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8b13-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="f8b13-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8b13-108">Parameters</span></span>

<span data-ttu-id="f8b13-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f8b13-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8b13-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8b13-110">Return value</span></span>

<span data-ttu-id="f8b13-111">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8b13-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b13-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8b13-112">Remarks</span></span>

<span data-ttu-id="f8b13-113">Этот метод вызывает метод [**стартстреаминг**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="f8b13-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="f8b13-114">Метод **стартстреаминг** не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="f8b13-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b13-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f8b13-115">Requirements</span></span>



| <span data-ttu-id="f8b13-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f8b13-116">Requirement</span></span> | <span data-ttu-id="f8b13-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f8b13-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b13-118">Header</span><span class="sxs-lookup"><span data-stu-id="f8b13-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f8b13-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b13-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8b13-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8b13-120">Library</span></span><br/> | <dl> <span data-ttu-id="f8b13-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b13-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b13-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f8b13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b13-123">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="f8b13-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




