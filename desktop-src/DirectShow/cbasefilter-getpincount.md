---
description: Кбасефилтер. Жетпинкаунт, метод Жетпинкаунт извлекает количество ПИН-кодов.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Кбасефилтер. Жетпинкаунт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099792"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="02309-103">Кбасефилтер. Жетпинкаунт, метод</span><span class="sxs-lookup"><span data-stu-id="02309-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="02309-104">`GetPinCount`Метод получает количество ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="02309-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="02309-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02309-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="02309-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02309-106">Parameters</span></span>

<span data-ttu-id="02309-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="02309-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02309-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02309-108">Return value</span></span>

<span data-ttu-id="02309-109">Возвращает число ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="02309-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="02309-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="02309-110">Remarks</span></span>

<span data-ttu-id="02309-111">Производный класс должен реализовывать этот чистый виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="02309-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="02309-112">Возврат количества ПИН-кодов, доступных в данный момент в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="02309-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="02309-113">Фильтры могут динамически создавать или удалять ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="02309-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="02309-114">Требования</span><span class="sxs-lookup"><span data-stu-id="02309-114">Requirements</span></span>



| <span data-ttu-id="02309-115">Требование</span><span class="sxs-lookup"><span data-stu-id="02309-115">Requirement</span></span> | <span data-ttu-id="02309-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02309-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02309-117">Header</span><span class="sxs-lookup"><span data-stu-id="02309-117">Header</span></span><br/>  | <dl> <span data-ttu-id="02309-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02309-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02309-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02309-119">Library</span></span><br/> | <dl> <span data-ttu-id="02309-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="02309-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02309-121">См. также</span><span class="sxs-lookup"><span data-stu-id="02309-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02309-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="02309-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




