---
description: Класс Ктрансформаутпутпин реализует выходной ПИН-код, который используется классом Ктрансформфилтер.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Класс Ктрансформаутпутпин (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679923"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="c1630-103">Класс Ктрансформаутпутпин</span><span class="sxs-lookup"><span data-stu-id="c1630-103">CTransformOutputPin class</span></span>

![Иерархия классов ктрансформаутпутпин](images/tfrm02.png)

<span data-ttu-id="c1630-105">`CTransformOutputPin`Класс реализует выходной ПИН-код, используемый классом [**ктрансформфилтер**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="c1630-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="c1630-106">Как правило, наследование от этого класса не требуется.</span><span class="sxs-lookup"><span data-stu-id="c1630-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="c1630-107">Большинство методов в этом классе вызывают соответствующие методы класса **ктрансформфилтер** , который можно переопределить.</span><span class="sxs-lookup"><span data-stu-id="c1630-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="c1630-108">Если вы наследуете от этого класса, необходимо переопределить метод [**ктрансформфилтер:: жетпин**](ctransformfilter-getpin.md) фильтра для создания экземпляров производного класса.</span><span class="sxs-lookup"><span data-stu-id="c1630-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="c1630-109">Этот класс предоставляет интерфейсы **имедиасикинг** и **Имедиапоситион** через объект [**кпоспасссру**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="c1630-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="c1630-110">Он передает все запросы поиска на следующий вышестоящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="c1630-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="c1630-111">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="c1630-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="c1630-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c1630-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="c1630-113">**m \_ птрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="c1630-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="c1630-114">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="c1630-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="c1630-115">Открытые переменные члена</span><span class="sxs-lookup"><span data-stu-id="c1630-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="c1630-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c1630-116">Description</span></span>                                              |
| [<span data-ttu-id="c1630-117">**m \_ ппоситион**</span><span class="sxs-lookup"><span data-stu-id="c1630-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="c1630-118">Вспомогательный объект для передачи команд поиска в восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="c1630-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="c1630-119">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="c1630-119">Public Methods</span></span>                                                           | <span data-ttu-id="c1630-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c1630-120">Description</span></span>                                              |
| [<span data-ttu-id="c1630-121">**ктрансформаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c1630-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="c1630-122">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c1630-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="c1630-123">**~ Ктрансформаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c1630-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="c1630-124">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="c1630-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="c1630-125">**чеккконнект**</span><span class="sxs-lookup"><span data-stu-id="c1630-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="c1630-126">Определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="c1630-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="c1630-127">**бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="c1630-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="c1630-128">Освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="c1630-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="c1630-129">**комплетеконнект**</span><span class="sxs-lookup"><span data-stu-id="c1630-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="c1630-130">Завершает подключение к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="c1630-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="c1630-131">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1630-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="c1630-132">Определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="c1630-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="c1630-133">**сетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1630-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="c1630-134">Задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="c1630-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="c1630-135">**деЦидебуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="c1630-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="c1630-136">Устанавливает требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="c1630-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="c1630-137">**жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1630-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="c1630-138">Извлекает предпочтительный тип мультимедиа по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="c1630-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="c1630-139">**куррентмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1630-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="c1630-140">Возвращает тип носителя для текущего подключения к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="c1630-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="c1630-141">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="c1630-141">IPin Methods</span></span>                                                             | <span data-ttu-id="c1630-142">Описание</span><span class="sxs-lookup"><span data-stu-id="c1630-142">Description</span></span>                                              |
| [<span data-ttu-id="c1630-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="c1630-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="c1630-144">Возвращает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c1630-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="c1630-145">Методы Икуалитиконтрол</span><span class="sxs-lookup"><span data-stu-id="c1630-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="c1630-146">Описание</span><span class="sxs-lookup"><span data-stu-id="c1630-146">Description</span></span>                                              |
| [<span data-ttu-id="c1630-147">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="c1630-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="c1630-148">Уведомляет ПИН-код о том, что запрошено изменение качества.</span><span class="sxs-lookup"><span data-stu-id="c1630-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="c1630-149">Требования</span><span class="sxs-lookup"><span data-stu-id="c1630-149">Requirements</span></span>



| <span data-ttu-id="c1630-150">Требование</span><span class="sxs-lookup"><span data-stu-id="c1630-150">Requirement</span></span> | <span data-ttu-id="c1630-151">Значение</span><span class="sxs-lookup"><span data-stu-id="c1630-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1630-152">Header</span><span class="sxs-lookup"><span data-stu-id="c1630-152">Header</span></span><br/>  | <dl> <span data-ttu-id="c1630-153"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1630-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c1630-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1630-154">Library</span></span><br/> | <dl> <span data-ttu-id="c1630-155"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c1630-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




