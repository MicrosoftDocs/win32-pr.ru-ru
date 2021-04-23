---
description: Метод конструктора.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Конструктор Ктрансформфилтер. Ктрансформфилтер (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657451"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="be5be-103">Ктрансформфилтер. Ктрансформфилтер, конструктор</span><span class="sxs-lookup"><span data-stu-id="be5be-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="be5be-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="be5be-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be5be-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="be5be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be5be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5be-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="be5be-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="be5be-108">Строка, содержащая имя отладки фильтра.</span><span class="sxs-lookup"><span data-stu-id="be5be-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="be5be-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="be5be-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="be5be-110">*лпунк*</span><span class="sxs-lookup"><span data-stu-id="be5be-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="be5be-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="be5be-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="be5be-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="be5be-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="be5be-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="be5be-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="be5be-114">*этому*</span><span class="sxs-lookup"><span data-stu-id="be5be-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="be5be-115">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="be5be-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be5be-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be5be-116">Remarks</span></span>

<span data-ttu-id="be5be-117">Конструктор не создает ПИН-коды фильтра.</span><span class="sxs-lookup"><span data-stu-id="be5be-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="be5be-118">Это происходит при первом вызове метода [**жетпин**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="be5be-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="be5be-119">Конструктор инициализирует переменные члена [**m \_ пинпут**](ctransformfilter-m-pinput.md) и [**m \_ паутпут**](ctransformfilter-m-poutput.md) **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="be5be-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5be-120">Требования</span><span class="sxs-lookup"><span data-stu-id="be5be-120">Requirements</span></span>



| <span data-ttu-id="be5be-121">Требование</span><span class="sxs-lookup"><span data-stu-id="be5be-121">Requirement</span></span> | <span data-ttu-id="be5be-122">Значение</span><span class="sxs-lookup"><span data-stu-id="be5be-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5be-123">Header</span><span class="sxs-lookup"><span data-stu-id="be5be-123">Header</span></span><br/>  | <dl> <span data-ttu-id="be5be-124"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be5be-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="be5be-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be5be-125">Library</span></span><br/> | <dl> <span data-ttu-id="be5be-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="be5be-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5be-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be5be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5be-128">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="be5be-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




