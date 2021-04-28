---
description: Метод конструктора Кбасереференцеклокк. Кбасереференцеклокк.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Конструктор Кбасереференцеклокк. Кбасереференцеклокк (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119942"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="cc2b1-103">Кбасереференцеклокк. Кбасереференцеклокк, конструктор</span><span class="sxs-lookup"><span data-stu-id="cc2b1-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="cc2b1-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2b1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc2b1-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="cc2b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc2b1-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="cc2b1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cc2b1-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="cc2b1-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="cc2b1-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc2b1-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="cc2b1-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cc2b1-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="cc2b1-112">Если объект является агрегатным, передайте указатель на интерфейс IUnknown объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="cc2b1-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc2b1-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="cc2b1-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cc2b1-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc2b1-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="cc2b1-116">При возникновении ошибки метод возвращает код ошибки в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="cc2b1-117">Не устанавливайте для этого параметра **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc2b1-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc2b1-118">*псчед*</span><span class="sxs-lookup"><span data-stu-id="cc2b1-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="cc2b1-119">Указатель на объект [**камсчедуле**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2b1-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="cc2b1-120">Если **значение равно NULL**, этот метод создает новый объект **камсчедуле** .</span><span class="sxs-lookup"><span data-stu-id="cc2b1-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc2b1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cc2b1-121">Requirements</span></span>



| <span data-ttu-id="cc2b1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cc2b1-122">Requirement</span></span> | <span data-ttu-id="cc2b1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cc2b1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2b1-124">Header</span><span class="sxs-lookup"><span data-stu-id="cc2b1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cc2b1-125"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b1-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc2b1-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc2b1-126">Library</span></span><br/> | <dl> <span data-ttu-id="cc2b1-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc2b1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cc2b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2b1-129">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="cc2b1-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




