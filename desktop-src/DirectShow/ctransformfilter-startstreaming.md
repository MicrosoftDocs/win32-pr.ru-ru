---
description: Метод Стартстреаминг вызывается, когда фильтр переключается в состояние паузы.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Ктрансформфилтер. Стартстреаминг, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657744"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="e3829-103">Ктрансформфилтер. Стартстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="e3829-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="e3829-104">`StartStreaming`Метод вызывается, когда фильтр переключается в состояние паузы.</span><span class="sxs-lookup"><span data-stu-id="e3829-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3829-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3829-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="e3829-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3829-106">Parameters</span></span>

<span data-ttu-id="e3829-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e3829-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3829-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3829-108">Return value</span></span>

<span data-ttu-id="e3829-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e3829-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3829-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3829-110">Remarks</span></span>

<span data-ttu-id="e3829-111">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="e3829-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3829-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e3829-112">Requirements</span></span>



| <span data-ttu-id="e3829-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e3829-113">Requirement</span></span> | <span data-ttu-id="e3829-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e3829-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3829-115">Header</span><span class="sxs-lookup"><span data-stu-id="e3829-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e3829-116"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3829-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e3829-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3829-117">Library</span></span><br/> | <dl> <span data-ttu-id="e3829-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e3829-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3829-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3829-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3829-120">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="e3829-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




