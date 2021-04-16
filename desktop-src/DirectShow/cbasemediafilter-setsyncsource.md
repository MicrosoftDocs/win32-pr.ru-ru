---
description: 'Метод Сетсинксаурце устанавливает ссылочный таймер для объекта. Этот метод реализует метод Имедиафилтер:: Сетсинксаурце.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Кбасемедиафилтер. Сетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656924"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="0eb43-104">Кбасемедиафилтер. Сетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="0eb43-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="0eb43-105">`SetSyncSource`Метод задает время ссылки для объекта.</span><span class="sxs-lookup"><span data-stu-id="0eb43-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="0eb43-106">Этот метод реализует метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="0eb43-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eb43-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="0eb43-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0eb43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eb43-109">*пклокк*</span><span class="sxs-lookup"><span data-stu-id="0eb43-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="0eb43-110">Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0eb43-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eb43-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0eb43-111">Return value</span></span>

<span data-ttu-id="0eb43-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0eb43-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb43-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0eb43-113">Requirements</span></span>



| <span data-ttu-id="0eb43-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0eb43-114">Requirement</span></span> | <span data-ttu-id="0eb43-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0eb43-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb43-116">Header</span><span class="sxs-lookup"><span data-stu-id="0eb43-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0eb43-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0eb43-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0eb43-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0eb43-118">Library</span></span><br/> | <dl> <span data-ttu-id="0eb43-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0eb43-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eb43-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0eb43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb43-121">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="0eb43-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




