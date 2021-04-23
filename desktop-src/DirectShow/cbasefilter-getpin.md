---
description: Метод Жетпин извлекает ПИН-код. Класс Ценумпинс вызывает этот метод для перечисления ПИН-кодов в фильтре.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Кбасефилтер. Жетпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657434"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="bf14b-104">Кбасефилтер. Жетпин, метод</span><span class="sxs-lookup"><span data-stu-id="bf14b-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="bf14b-105">Метод **жетпин** извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="bf14b-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="bf14b-106">Класс [**ценумпинс**](cenumpins.md) вызывает этот метод для перечисления ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="bf14b-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf14b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf14b-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bf14b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf14b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf14b-109">*n*</span><span class="sxs-lookup"><span data-stu-id="bf14b-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="bf14b-110">Отсчитываемый от нуля индекс ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bf14b-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf14b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf14b-111">Return value</span></span>

<span data-ttu-id="bf14b-112">Возвращает указатель на объект [**кбасепин**](cbasepin.md) , который реализует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="bf14b-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf14b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf14b-113">Remarks</span></span>

<span data-ttu-id="bf14b-114">Этот чистый виртуальный метод необходимо реализовать в производном классе.</span><span class="sxs-lookup"><span data-stu-id="bf14b-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="bf14b-115">Возврат указателя к *n*-ом закрепления фильтра, индексируемого от нуля.</span><span class="sxs-lookup"><span data-stu-id="bf14b-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="bf14b-116">Можно выбрать произвольный порядок индексирования, если порядок фиксирован.</span><span class="sxs-lookup"><span data-stu-id="bf14b-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="bf14b-117">Если фильтр добавляет или удаляет ПИН-коды или изменяется по какой-либо другой причине во время выполнения, вызовите метод [**кбасефилтер:: инкрементпинверсион**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="bf14b-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf14b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bf14b-118">Requirements</span></span>



| <span data-ttu-id="bf14b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bf14b-119">Requirement</span></span> | <span data-ttu-id="bf14b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bf14b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf14b-121">Header</span><span class="sxs-lookup"><span data-stu-id="bf14b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bf14b-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf14b-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf14b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf14b-123">Library</span></span><br/> | <dl> <span data-ttu-id="bf14b-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf14b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf14b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf14b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf14b-126">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="bf14b-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




