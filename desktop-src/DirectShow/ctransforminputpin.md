---
description: Класс Ктрансформинпутпин реализует входной ПИН-код, используемый классом Ктрансформфилтер.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Класс Ктрансформинпутпин (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658037"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="15efb-103">Класс Ктрансформинпутпин</span><span class="sxs-lookup"><span data-stu-id="15efb-103">CTransformInputPin class</span></span>

![Иерархия классов ктрансформинпутпин](images/tfrm01.png)

<span data-ttu-id="15efb-105">`CTransformInputPin`Класс реализует входной ПИН-код, используемый классом [**ктрансформфилтер**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="15efb-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="15efb-106">Как правило, наследование от этого класса не требуется.</span><span class="sxs-lookup"><span data-stu-id="15efb-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="15efb-107">Большинство методов в этом классе вызывают соответствующие методы класса **ктрансформфилтер** , который можно переопределить.</span><span class="sxs-lookup"><span data-stu-id="15efb-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="15efb-108">Если вы наследуете от этого класса, необходимо переопределить метод [**ктрансформфилтер:: жетпин**](ctransformfilter-getpin.md) фильтра для создания экземпляров производного класса.</span><span class="sxs-lookup"><span data-stu-id="15efb-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="15efb-109">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="15efb-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="15efb-110">Описание</span><span class="sxs-lookup"><span data-stu-id="15efb-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="15efb-111">**m \_ птрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="15efb-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="15efb-112">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="15efb-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="15efb-113">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="15efb-113">Public Methods</span></span>                                                       | <span data-ttu-id="15efb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="15efb-114">Description</span></span>                                                                            |
| [<span data-ttu-id="15efb-115">**ктрансформинпутпин**</span><span class="sxs-lookup"><span data-stu-id="15efb-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="15efb-116">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="15efb-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="15efb-117">**чеккконнект**</span><span class="sxs-lookup"><span data-stu-id="15efb-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="15efb-118">Определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="15efb-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="15efb-119">**бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="15efb-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="15efb-120">Освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="15efb-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="15efb-121">**комплетеконнект**</span><span class="sxs-lookup"><span data-stu-id="15efb-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="15efb-122">Завершает подключение к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="15efb-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="15efb-123">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="15efb-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="15efb-124">Определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="15efb-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="15efb-125">**сетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="15efb-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="15efb-126">Задает тип носителя для соединения.</span><span class="sxs-lookup"><span data-stu-id="15efb-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="15efb-127">**чеккстреаминг**</span><span class="sxs-lookup"><span data-stu-id="15efb-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="15efb-128">Определяет, может ли ПИН-код принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="15efb-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="15efb-129">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="15efb-129">Virtual.</span></span>                                |
| [<span data-ttu-id="15efb-130">**куррентмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="15efb-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="15efb-131">Возвращает тип носителя для текущего подключения к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="15efb-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="15efb-132">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="15efb-132">IPin Methods</span></span>                                                         | <span data-ttu-id="15efb-133">Описание</span><span class="sxs-lookup"><span data-stu-id="15efb-133">Description</span></span>                                                                            |
| [<span data-ttu-id="15efb-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="15efb-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="15efb-135">Возвращает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="15efb-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="15efb-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="15efb-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="15efb-137">Уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="15efb-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="15efb-138">**бегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="15efb-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="15efb-139">Начинает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="15efb-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="15efb-140">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="15efb-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="15efb-141">Завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="15efb-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="15efb-142">**невсегмент**</span><span class="sxs-lookup"><span data-stu-id="15efb-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="15efb-143">Уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент.</span><span class="sxs-lookup"><span data-stu-id="15efb-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="15efb-144">Методы Имеминпутпин</span><span class="sxs-lookup"><span data-stu-id="15efb-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="15efb-145">Описание</span><span class="sxs-lookup"><span data-stu-id="15efb-145">Description</span></span>                                                                            |
| [<span data-ttu-id="15efb-146">**Получать**</span><span class="sxs-lookup"><span data-stu-id="15efb-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="15efb-147">Получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="15efb-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="15efb-148">Требования</span><span class="sxs-lookup"><span data-stu-id="15efb-148">Requirements</span></span>



| <span data-ttu-id="15efb-149">Требование</span><span class="sxs-lookup"><span data-stu-id="15efb-149">Requirement</span></span> | <span data-ttu-id="15efb-150">Значение</span><span class="sxs-lookup"><span data-stu-id="15efb-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15efb-151">Header</span><span class="sxs-lookup"><span data-stu-id="15efb-151">Header</span></span><br/>  | <dl> <span data-ttu-id="15efb-152"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15efb-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="15efb-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15efb-153">Library</span></span><br/> | <dl> <span data-ttu-id="15efb-154"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="15efb-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




