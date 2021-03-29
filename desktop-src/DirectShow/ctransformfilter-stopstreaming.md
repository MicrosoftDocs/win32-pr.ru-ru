---
description: Метод Стопстреаминг вызывается, когда фильтр переключается в состояние Stopped.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Ктрансформфилтер. Стопстреаминг, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657609"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="a14be-103">Ктрансформфилтер. Стопстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="a14be-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="a14be-104">`StopStreaming`Метод вызывается, когда фильтр переключается в состояние Stopped.</span><span class="sxs-lookup"><span data-stu-id="a14be-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a14be-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="a14be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a14be-106">Parameters</span></span>

<span data-ttu-id="a14be-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a14be-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a14be-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a14be-108">Return value</span></span>

<span data-ttu-id="a14be-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a14be-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a14be-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a14be-110">Remarks</span></span>

<span data-ttu-id="a14be-111">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="a14be-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14be-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a14be-112">Requirements</span></span>



| <span data-ttu-id="a14be-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a14be-113">Requirement</span></span> | <span data-ttu-id="a14be-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a14be-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14be-115">Header</span><span class="sxs-lookup"><span data-stu-id="a14be-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a14be-116"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a14be-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a14be-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a14be-117">Library</span></span><br/> | <dl> <span data-ttu-id="a14be-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a14be-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14be-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a14be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14be-120">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="a14be-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




