---
description: Метод Жетпинкаунт извлекает количество ПИН-кодов в фильтре.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Ктрансформфилтер. Жетпинкаунт, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657758"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="6ec2c-103">Ктрансформфилтер. Жетпинкаунт, метод</span><span class="sxs-lookup"><span data-stu-id="6ec2c-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="6ec2c-104">`GetPinCount`Метод извлекает количество ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ec2c-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="6ec2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ec2c-106">Parameters</span></span>

<span data-ttu-id="6ec2c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ec2c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ec2c-108">Return value</span></span>

<span data-ttu-id="6ec2c-109">Возвращает значение 2.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec2c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ec2c-110">Remarks</span></span>

<span data-ttu-id="6ec2c-111">Этот метод переопределяет метод [**кбасефилтер:: жетпинкаунт**](cbasefilter-getpincount.md) .</span><span class="sxs-lookup"><span data-stu-id="6ec2c-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="6ec2c-112">Класс **ктрансформфилтер** поддерживает ровно один входной ПИН-код и один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec2c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6ec2c-113">Requirements</span></span>



| <span data-ttu-id="6ec2c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6ec2c-114">Requirement</span></span> | <span data-ttu-id="6ec2c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6ec2c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec2c-116">Header</span><span class="sxs-lookup"><span data-stu-id="6ec2c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ec2c-117"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ec2c-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ec2c-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ec2c-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ec2c-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6ec2c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec2c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ec2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec2c-121">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="6ec2c-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




