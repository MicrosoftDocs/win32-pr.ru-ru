---
description: 'Метод Стартстреаминг вызывается, когда фильтр переключается в состояние паузы. Этот метод переопределяет метод Ктрансформфилтер:: Стартстреаминг.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Квидеотрансформфилтер. Стартстреаминг, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675035"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="580a7-104">Квидеотрансформфилтер. Стартстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="580a7-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="580a7-105">`StartStreaming`Метод вызывается, когда фильтр переключается в состояние паузы.</span><span class="sxs-lookup"><span data-stu-id="580a7-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="580a7-106">Этот метод переопределяет метод [**ктрансформфилтер:: стартстреаминг**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="580a7-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="580a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="580a7-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="580a7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="580a7-108">Parameters</span></span>

<span data-ttu-id="580a7-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="580a7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="580a7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="580a7-110">Return value</span></span>

<span data-ttu-id="580a7-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="580a7-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="580a7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="580a7-112">Remarks</span></span>

<span data-ttu-id="580a7-113">Этот метод сбрасывает всю статистику производительности.</span><span class="sxs-lookup"><span data-stu-id="580a7-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="580a7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="580a7-114">Requirements</span></span>



| <span data-ttu-id="580a7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="580a7-115">Requirement</span></span> | <span data-ttu-id="580a7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="580a7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580a7-117">Header</span><span class="sxs-lookup"><span data-stu-id="580a7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="580a7-118"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="580a7-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="580a7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="580a7-119">Library</span></span><br/> | <dl> <span data-ttu-id="580a7-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="580a7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580a7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="580a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580a7-122">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="580a7-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




