---
description: Метод Жетпинкаунт извлекает количество ПИН-кодов.
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657811"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="315fd-103">Кбасефилтер. Жетпинкаунт, метод</span><span class="sxs-lookup"><span data-stu-id="315fd-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="315fd-104">`GetPinCount`Метод получает количество ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="315fd-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="315fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="315fd-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="315fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="315fd-106">Parameters</span></span>

<span data-ttu-id="315fd-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="315fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="315fd-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="315fd-108">Return value</span></span>

<span data-ttu-id="315fd-109">Возвращает число ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="315fd-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="315fd-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="315fd-110">Remarks</span></span>

<span data-ttu-id="315fd-111">Производный класс должен реализовывать этот чистый виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="315fd-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="315fd-112">Возврат количества ПИН-кодов, доступных в данный момент в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="315fd-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="315fd-113">Фильтры могут динамически создавать или удалять ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="315fd-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="315fd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="315fd-114">Requirements</span></span>



| <span data-ttu-id="315fd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="315fd-115">Requirement</span></span> | <span data-ttu-id="315fd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="315fd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="315fd-117">Header</span><span class="sxs-lookup"><span data-stu-id="315fd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="315fd-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="315fd-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="315fd-119">Library</span></span><br/> | <dl> <span data-ttu-id="315fd-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315fd-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="315fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315fd-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="315fd-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




