---
description: Метод Жетсетупдата извлекает данные регистрации для фильтра.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Кбасефилтер. Жетсетупдата, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657806"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="5e5fb-103">Кбасефилтер. Жетсетупдата, метод</span><span class="sxs-lookup"><span data-stu-id="5e5fb-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="5e5fb-104">`GetSetupData`Метод получает данные регистрации для фильтра.</span><span class="sxs-lookup"><span data-stu-id="5e5fb-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="5e5fb-105">Этот метод устарел.</span><span class="sxs-lookup"><span data-stu-id="5e5fb-105">This method is obsolete.</span></span> <span data-ttu-id="5e5fb-106">Он вызывается методами [**кбасефилтер:: Register**](cbasefilter-register.md) и [**кбасефилтер:: Unregister**](cbasefilter-unregister.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5fb-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e5fb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e5fb-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="5e5fb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e5fb-108">Parameters</span></span>

<span data-ttu-id="5e5fb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5e5fb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e5fb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e5fb-110">Return value</span></span>

<span data-ttu-id="5e5fb-111">Возвращает указатель на структуру [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) , содержащую сведения о регистрации для фильтра.</span><span class="sxs-lookup"><span data-stu-id="5e5fb-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5fb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e5fb-112">Remarks</span></span>

<span data-ttu-id="5e5fb-113">Базовый класс возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5e5fb-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5fb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5e5fb-114">Requirements</span></span>



| <span data-ttu-id="5e5fb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5e5fb-115">Requirement</span></span> | <span data-ttu-id="5e5fb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5e5fb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5fb-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e5fb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e5fb-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5fb-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5e5fb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e5fb-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e5fb-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5fb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5fb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e5fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5fb-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="5e5fb-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




