---
description: Метод Жетмедиатипеверсион извлекает номер версии для набора предпочтительных типов мультимедиа.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Кбасепин. Жетмедиатипеверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658105"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="20840-103">Кбасепин. Жетмедиатипеверсион, метод</span><span class="sxs-lookup"><span data-stu-id="20840-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="20840-104">`GetMediaTypeVersion`Метод получает номер версии для набора предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="20840-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="20840-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20840-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="20840-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20840-106">Parameters</span></span>

<span data-ttu-id="20840-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="20840-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20840-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20840-108">Return value</span></span>

<span data-ttu-id="20840-109">Возвращает переменную члена [**кбасепин:: m \_ типеверсион**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="20840-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="20840-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20840-110">Remarks</span></span>

<span data-ttu-id="20840-111">Конструктор **кбасепин** Инициализирует номер версии равным 1.</span><span class="sxs-lookup"><span data-stu-id="20840-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="20840-112">В базовом классе это число никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="20840-112">In the base class, this number never changes.</span></span> <span data-ttu-id="20840-113">Если ПИН-код динамически изменяет свой список предпочтительных типов мультимедиа, он должен увеличивать номер версии при каждом изменении списка.</span><span class="sxs-lookup"><span data-stu-id="20840-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="20840-114">Чтобы увеличить номер версии, вызовите метод [**кбасепин:: инкременттипеверсион**](cbasepin-incrementtypeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="20840-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="20840-115">Перечислитель типа мультимедиа, реализуемый классом [**ценуммедиатипес**](cenummediatypes.md) , использует номер версии для синхронизации с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="20840-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="20840-116">Требования</span><span class="sxs-lookup"><span data-stu-id="20840-116">Requirements</span></span>



| <span data-ttu-id="20840-117">Требование</span><span class="sxs-lookup"><span data-stu-id="20840-117">Requirement</span></span> | <span data-ttu-id="20840-118">Значение</span><span class="sxs-lookup"><span data-stu-id="20840-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20840-119">Header</span><span class="sxs-lookup"><span data-stu-id="20840-119">Header</span></span><br/>  | <dl> <span data-ttu-id="20840-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20840-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20840-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20840-121">Library</span></span><br/> | <dl> <span data-ttu-id="20840-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="20840-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20840-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20840-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20840-124">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="20840-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




