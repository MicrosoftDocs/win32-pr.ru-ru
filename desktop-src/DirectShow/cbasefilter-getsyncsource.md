---
description: 'Метод Жетсинксаурце извлекает ссылочное время, которое использует фильтр. Этот метод реализует метод Имедиафилтер:: Жетсинксаурце.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Кбасефилтер. Жетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657803"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="2375d-104">Кбасефилтер. Жетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="2375d-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="2375d-105">`GetSyncSource`Метод получает ссылочное время, которое использует фильтр.</span><span class="sxs-lookup"><span data-stu-id="2375d-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="2375d-106">Этот метод реализует метод [**имедиафилтер:: жетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="2375d-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2375d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2375d-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="2375d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2375d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2375d-109">*пклокк*</span><span class="sxs-lookup"><span data-stu-id="2375d-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="2375d-110">Адрес переменной, которая получает указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов.</span><span class="sxs-lookup"><span data-stu-id="2375d-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2375d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2375d-111">Return value</span></span>

<span data-ttu-id="2375d-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="2375d-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="2375d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2375d-113">Remarks</span></span>

<span data-ttu-id="2375d-114">Если в фильтре не используется ссылочное время, *\* пклокк* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2375d-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="2375d-115">Если метод возвращает значение, если *\* пклокк* не равен **null**, то интерфейс **иреференцеклокк** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="2375d-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="2375d-116">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="2375d-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="2375d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2375d-117">Requirements</span></span>



| <span data-ttu-id="2375d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2375d-118">Requirement</span></span> | <span data-ttu-id="2375d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2375d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2375d-120">Header</span><span class="sxs-lookup"><span data-stu-id="2375d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2375d-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2375d-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2375d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2375d-122">Library</span></span><br/> | <dl> <span data-ttu-id="2375d-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2375d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2375d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2375d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2375d-125">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="2375d-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




