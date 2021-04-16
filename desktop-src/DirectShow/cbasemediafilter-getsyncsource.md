---
description: 'Метод Жетсинксаурце извлекает ссылочное время, которое использует объект. Этот метод реализует метод Имедиафилтер:: Жетсинксаурце.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Кбасемедиафилтер. Жетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656975"
---
# <a name="cbasemediafiltergetsyncsource-method"></a><span data-ttu-id="f59c5-104">Кбасемедиафилтер. Жетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="f59c5-104">CBaseMediaFilter.GetSyncSource method</span></span>

<span data-ttu-id="f59c5-105">`GetSyncSource`Метод получает ссылочное время, которое использует объект.</span><span class="sxs-lookup"><span data-stu-id="f59c5-105">The `GetSyncSource` method retrieves the reference clock that the object is using.</span></span> <span data-ttu-id="f59c5-106">Этот метод реализует метод [**имедиафилтер:: жетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="f59c5-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f59c5-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="f59c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f59c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f59c5-109">*пклокк*</span><span class="sxs-lookup"><span data-stu-id="f59c5-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="f59c5-110">Адрес переменной, которая получает указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов.</span><span class="sxs-lookup"><span data-stu-id="f59c5-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f59c5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f59c5-111">Return value</span></span>

<span data-ttu-id="f59c5-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="f59c5-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="f59c5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f59c5-113">Remarks</span></span>

<span data-ttu-id="f59c5-114">Если объект не использует ссылочный таймер, *\* пклокк* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f59c5-114">If the object is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="f59c5-115">Если метод возвращает значение, если *\* пклокк* не равен **null**, то интерфейс **иреференцеклокк** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="f59c5-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="f59c5-116">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="f59c5-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="f59c5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f59c5-117">Requirements</span></span>



| <span data-ttu-id="f59c5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f59c5-118">Requirement</span></span> | <span data-ttu-id="f59c5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f59c5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59c5-120">Header</span><span class="sxs-lookup"><span data-stu-id="f59c5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f59c5-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f59c5-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f59c5-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f59c5-122">Library</span></span><br/> | <dl> <span data-ttu-id="f59c5-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f59c5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59c5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f59c5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59c5-125">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="f59c5-125">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




