---
description: 'Метод Жетпин извлекает ПИН-код. Этот метод реализует чистый виртуальный метод Кбасефилтер:: Жетпин.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Метод Ксаурце. Жетпин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665445"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="c57f4-104">Ксаурце. Жетпин, метод</span><span class="sxs-lookup"><span data-stu-id="c57f4-104">CSource.GetPin method</span></span>

<span data-ttu-id="c57f4-105">`GetPin`Метод извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="c57f4-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="c57f4-106">Этот метод реализует чистый виртуальный метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="c57f4-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c57f4-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="c57f4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c57f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57f4-109">*n*</span><span class="sxs-lookup"><span data-stu-id="c57f4-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="c57f4-110">Номер указанного пин-кода.</span><span class="sxs-lookup"><span data-stu-id="c57f4-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57f4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c57f4-111">Return value</span></span>

<span data-ttu-id="c57f4-112">Возвращает указатель на объект [**кбасепин**](cbasepin.md) , который реализует ПИН-код, или **значение NULL** , если индекс выходит за пределы диапазона.</span><span class="sxs-lookup"><span data-stu-id="c57f4-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57f4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c57f4-113">Requirements</span></span>



| <span data-ttu-id="c57f4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c57f4-114">Requirement</span></span> | <span data-ttu-id="c57f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c57f4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57f4-116">Header</span><span class="sxs-lookup"><span data-stu-id="c57f4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c57f4-117"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c57f4-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c57f4-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c57f4-118">Library</span></span><br/> | <dl> <span data-ttu-id="c57f4-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c57f4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57f4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c57f4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57f4-121">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="c57f4-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




