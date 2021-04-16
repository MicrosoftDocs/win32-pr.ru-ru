---
description: Класс Ценумпинс реализует перечислитель для ПИН-кодов.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Класс Ценумпинс (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657578"
---
# <a name="cenumpins-class"></a><span data-ttu-id="f02dd-103">Класс Ценумпинс</span><span class="sxs-lookup"><span data-stu-id="f02dd-103">CEnumPins class</span></span>

![Иерархия классов ценумпинс](images/filter03.png)

<span data-ttu-id="f02dd-105">`CEnumPins`Класс реализует перечислитель для ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="f02dd-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="f02dd-106">Этот класс реализует интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="f02dd-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="f02dd-107">Он вызывает следующие методы [**кбасефилтер**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="f02dd-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="f02dd-108">[**Кбасефилтер:: жетпин**](cbasefilter-getpin.md): получает ПИН-код для фильтра, на который ссылается индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="f02dd-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="f02dd-109">[**Кбасефилтер:: жетпинкаунт**](cbasefilter-getpincount.md)— получает общее количество ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="f02dd-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="f02dd-110">[**Кбасефилтер:: жетпинверсион**](cbasefilter-getpinversion.md): определяет, изменились ли ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="f02dd-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="f02dd-111">Если фильтр динамически создает или уничтожает ПИН-коды, то при каждом изменении ПИН увеличивается ее версия.</span><span class="sxs-lookup"><span data-stu-id="f02dd-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="f02dd-112">При изменении номера версии объект перечислителя больше не синхронизируется с фильтром.</span><span class="sxs-lookup"><span data-stu-id="f02dd-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="f02dd-113">После того как перечислитель не синхронизирован, методы в `CEnumPins` возвращают \_ \_ \_ \_ Несинхронизированное перечисление в VFW E \_ .</span><span class="sxs-lookup"><span data-stu-id="f02dd-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="f02dd-114">Вызовите метод [**ценумпинс:: Reset**](cenumpins-reset.md) для повторной синхронизации перечислителя.</span><span class="sxs-lookup"><span data-stu-id="f02dd-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="f02dd-115">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="f02dd-115">Public Methods</span></span>                             | <span data-ttu-id="f02dd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f02dd-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="f02dd-117">**ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="f02dd-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="f02dd-118">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f02dd-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="f02dd-119">**~ Ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="f02dd-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="f02dd-120">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="f02dd-120">Destructor method.</span></span> <span data-ttu-id="f02dd-121">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f02dd-121">Virtual.</span></span>                                     |
| <span data-ttu-id="f02dd-122">Методы Иенумпинс</span><span class="sxs-lookup"><span data-stu-id="f02dd-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="f02dd-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f02dd-123">Description</span></span>                                                     |
| [<span data-ttu-id="f02dd-124">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="f02dd-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="f02dd-125">Создает копию перечислителя с тем же состоянием перечисления.</span><span class="sxs-lookup"><span data-stu-id="f02dd-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="f02dd-126">**Далее**</span><span class="sxs-lookup"><span data-stu-id="f02dd-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="f02dd-127">Извлекает указанное число ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="f02dd-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="f02dd-128">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="f02dd-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="f02dd-129">Сбрасывает последовательность перечисления в начало.</span><span class="sxs-lookup"><span data-stu-id="f02dd-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="f02dd-130">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="f02dd-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="f02dd-131">Пропускает указанное число ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="f02dd-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="f02dd-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f02dd-132">Requirements</span></span>



| <span data-ttu-id="f02dd-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f02dd-133">Requirement</span></span> | <span data-ttu-id="f02dd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f02dd-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02dd-135">Header</span><span class="sxs-lookup"><span data-stu-id="f02dd-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f02dd-136"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f02dd-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f02dd-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f02dd-137">Library</span></span><br/> | <dl> <span data-ttu-id="f02dd-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f02dd-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




