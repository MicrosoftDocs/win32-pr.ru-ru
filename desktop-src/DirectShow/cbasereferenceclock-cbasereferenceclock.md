---
description: Метод конструктора.
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
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668923"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="7a527-103">Кбасереференцеклокк. Кбасереференцеклокк, конструктор</span><span class="sxs-lookup"><span data-stu-id="7a527-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="7a527-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="7a527-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a527-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a527-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="7a527-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a527-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="7a527-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7a527-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7a527-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="7a527-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="7a527-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a527-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="7a527-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7a527-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7a527-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="7a527-112">Если объект является агрегатным, передайте указатель на интерфейс IUnknown объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="7a527-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="7a527-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a527-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a527-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="7a527-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7a527-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a527-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="7a527-116">При возникновении ошибки метод возвращает код ошибки в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="7a527-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="7a527-117">Не устанавливайте для этого параметра **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a527-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a527-118">*псчед*</span><span class="sxs-lookup"><span data-stu-id="7a527-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="7a527-119">Указатель на объект [**камсчедуле**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="7a527-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="7a527-120">Если **значение равно NULL**, этот метод создает новый объект **камсчедуле** .</span><span class="sxs-lookup"><span data-stu-id="7a527-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a527-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7a527-121">Requirements</span></span>



| <span data-ttu-id="7a527-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7a527-122">Requirement</span></span> | <span data-ttu-id="7a527-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7a527-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a527-124">Header</span><span class="sxs-lookup"><span data-stu-id="7a527-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7a527-125"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a527-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a527-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a527-126">Library</span></span><br/> | <dl> <span data-ttu-id="7a527-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7a527-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a527-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a527-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a527-129">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="7a527-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




