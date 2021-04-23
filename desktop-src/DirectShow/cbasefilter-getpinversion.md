---
description: Метод Жетпинверсион извлекает номер версии для набора ПИН-кодов в этом фильтре.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Кбасефилтер. Жетпинверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657807"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="6311b-103">Кбасефилтер. Жетпинверсион, метод</span><span class="sxs-lookup"><span data-stu-id="6311b-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="6311b-104">`GetPinVersion`Метод извлекает номер версии для набора ПИН-кодов в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="6311b-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6311b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6311b-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="6311b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6311b-106">Parameters</span></span>

<span data-ttu-id="6311b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6311b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6311b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6311b-108">Return value</span></span>

<span data-ttu-id="6311b-109">Возвращает переменную члена [**кбасефилтер:: m \_ пинверсион**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="6311b-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6311b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6311b-110">Remarks</span></span>

<span data-ttu-id="6311b-111">Конструктор **кбасефилтер** инициализирует версию ПИН-кода до 1.</span><span class="sxs-lookup"><span data-stu-id="6311b-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="6311b-112">В базовом классе это число никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="6311b-112">In the base class, this number never changes.</span></span> <span data-ttu-id="6311b-113">Если фильтр динамически создает или уничтожает ПИН-коды, он должен увеличивать номер версии ПИН при каждом изменении ПИН.</span><span class="sxs-lookup"><span data-stu-id="6311b-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="6311b-114">Чтобы увеличить номер версии, вызовите метод [**кбасефилтер:: инкрементпинверсион**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="6311b-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="6311b-115">Объект перечислителя PIN-кодов, реализованный классом [**ценумпинс**](cenumpins.md) , использует версию ПИН-кода для синхронизации с фильтром.</span><span class="sxs-lookup"><span data-stu-id="6311b-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6311b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6311b-116">Requirements</span></span>



| <span data-ttu-id="6311b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6311b-117">Requirement</span></span> | <span data-ttu-id="6311b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6311b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6311b-119">Header</span><span class="sxs-lookup"><span data-stu-id="6311b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6311b-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6311b-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6311b-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6311b-121">Library</span></span><br/> | <dl> <span data-ttu-id="6311b-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6311b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6311b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6311b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6311b-124">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="6311b-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




