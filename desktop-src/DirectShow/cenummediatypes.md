---
description: Класс Ценуммедиатипес реализует перечислитель для предпочтительных типов мультимедиа.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Класс Ценуммедиатипес (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668827"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="dc50d-103">Класс Ценуммедиатипес</span><span class="sxs-lookup"><span data-stu-id="dc50d-103">CEnumMediaTypes class</span></span>

![Иерархия классов ценуммедиатипес](images/filter04.png)

<span data-ttu-id="dc50d-105">`CEnumMediaTypes`Класс реализует перечислитель для предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc50d-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="dc50d-106">Этот класс реализует интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="dc50d-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="dc50d-107">Он вызывает следующие методы [**кбасепин**](cbasepin.md) :</span><span class="sxs-lookup"><span data-stu-id="dc50d-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="dc50d-108">[**Кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md): Извлекает тип мультимедиа, на который ссылается индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="dc50d-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="dc50d-109">[**Кбасепин:: жетмедиатипеверсион**](cbasepin-getmediatypeversion.md): определяет, изменился ли набор предпочтительных типов.</span><span class="sxs-lookup"><span data-stu-id="dc50d-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="dc50d-110">Каждый раз, когда ПИН-код изменяет свой список предпочтительных типов мультимедиа, этот ПИН-код увеличивает номер версии типа носителя.</span><span class="sxs-lookup"><span data-stu-id="dc50d-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="dc50d-111">В этом случае объект перечислителя больше не синхронизируется с закреплением, а методы класса возвращают VFW \_ E \_ Enum \_ из \_ \_ Sync.</span><span class="sxs-lookup"><span data-stu-id="dc50d-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="dc50d-112">Вызовите метод [**ценуммедиатипес:: Reset**](cenummediatypes-reset.md) для повторной синхронизации перечислителя.</span><span class="sxs-lookup"><span data-stu-id="dc50d-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="dc50d-113">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="dc50d-113">Public Methods</span></span>                                               | <span data-ttu-id="dc50d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dc50d-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="dc50d-115">**ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="dc50d-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="dc50d-116">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="dc50d-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="dc50d-117">**~ Ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="dc50d-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="dc50d-118">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="dc50d-118">Destructor method.</span></span> <span data-ttu-id="dc50d-119">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="dc50d-119">Virtual.</span></span>                                     |
| <span data-ttu-id="dc50d-120">Методы Иенуммедиатипес</span><span class="sxs-lookup"><span data-stu-id="dc50d-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="dc50d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="dc50d-121">Description</span></span>                                                     |
| [<span data-ttu-id="dc50d-122">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="dc50d-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="dc50d-123">Создает копию перечислителя с тем же состоянием перечисления.</span><span class="sxs-lookup"><span data-stu-id="dc50d-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="dc50d-124">**Далее**</span><span class="sxs-lookup"><span data-stu-id="dc50d-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="dc50d-125">Извлекает указанное число типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc50d-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="dc50d-126">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="dc50d-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="dc50d-127">Сбрасывает последовательность перечисления в начало.</span><span class="sxs-lookup"><span data-stu-id="dc50d-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="dc50d-128">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="dc50d-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="dc50d-129">Пропускает указанное число типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc50d-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="dc50d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="dc50d-130">Requirements</span></span>



| <span data-ttu-id="dc50d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="dc50d-131">Requirement</span></span> | <span data-ttu-id="dc50d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="dc50d-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc50d-133">Header</span><span class="sxs-lookup"><span data-stu-id="dc50d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dc50d-134"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc50d-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dc50d-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc50d-135">Library</span></span><br/> | <dl> <span data-ttu-id="dc50d-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dc50d-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




