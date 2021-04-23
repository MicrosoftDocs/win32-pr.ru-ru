---
description: Метод Инкременттипеверсион увеличивает номер версии в наборе предпочтительных типов носителей.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Кбасепин. Инкременттипеверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657977"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="17e62-103">Кбасепин. Инкременттипеверсион, метод</span><span class="sxs-lookup"><span data-stu-id="17e62-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="17e62-104">`IncrementTypeVersion`Метод увеличивает номер версии в наборе предпочтительных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="17e62-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e62-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17e62-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="17e62-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17e62-106">Parameters</span></span>

<span data-ttu-id="17e62-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="17e62-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17e62-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17e62-108">Return value</span></span>

<span data-ttu-id="17e62-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="17e62-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e62-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17e62-110">Remarks</span></span>

<span data-ttu-id="17e62-111">Этот метод увеличивает значение переменной члена [**кбасепин:: m \_ типеверсион**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="17e62-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="17e62-112">Если ПИН-код динамически изменяет список предпочтительных типов мультимедиа, вызывайте этот метод при каждом изменении списка.</span><span class="sxs-lookup"><span data-stu-id="17e62-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="17e62-113">Дополнительные сведения см. в разделе [**кбасепин:: жетмедиатипеверсион**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="17e62-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17e62-114">Требования</span><span class="sxs-lookup"><span data-stu-id="17e62-114">Requirements</span></span>



| <span data-ttu-id="17e62-115">Требование</span><span class="sxs-lookup"><span data-stu-id="17e62-115">Requirement</span></span> | <span data-ttu-id="17e62-116">Значение</span><span class="sxs-lookup"><span data-stu-id="17e62-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e62-117">Header</span><span class="sxs-lookup"><span data-stu-id="17e62-117">Header</span></span><br/>  | <dl> <span data-ttu-id="17e62-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17e62-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="17e62-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17e62-119">Library</span></span><br/> | <dl> <span data-ttu-id="17e62-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="17e62-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e62-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17e62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e62-122">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="17e62-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




