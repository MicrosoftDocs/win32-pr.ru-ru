---
description: Класс Кбасерендереринпутпин реализует входной ПИН-код для класса Кбасерендерер. За исключением указанных случаев, методы в этом классе делегируют соответствующие методы класса Кбасерендерер.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Класс Крендереринпутпин (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658005"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="d419a-104">Класс Крендереринпутпин</span><span class="sxs-lookup"><span data-stu-id="d419a-104">CRendererInputPin class</span></span>

![крендереринпут закрепить иерархию классов](images/rbase01.png)

<span data-ttu-id="d419a-106">Класс **кбасерендереринпутпин** реализует входной ПИН-код для класса [**кбасерендерер**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="d419a-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="d419a-107">За исключением указанных случаев, методы в этом классе делегируют соответствующие методы класса **кбасерендерер** .</span><span class="sxs-lookup"><span data-stu-id="d419a-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="d419a-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="d419a-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="d419a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d419a-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d419a-110">**m \_ прендерер**</span><span class="sxs-lookup"><span data-stu-id="d419a-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="d419a-111">Указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="d419a-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="d419a-112">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="d419a-112">Public Methods</span></span>                                                   | <span data-ttu-id="d419a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d419a-113">Description</span></span>                                                                            |
| [<span data-ttu-id="d419a-114">**крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="d419a-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="d419a-115">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d419a-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="d419a-116">**бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="d419a-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="d419a-117">Добавляет настраиваемый код при разрыве соединения.</span><span class="sxs-lookup"><span data-stu-id="d419a-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="d419a-118">**комплетеконнект**</span><span class="sxs-lookup"><span data-stu-id="d419a-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="d419a-119">Завершает соединение.</span><span class="sxs-lookup"><span data-stu-id="d419a-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="d419a-120">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d419a-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="d419a-121">Определяет, может ли ПИН-код поддерживать конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="d419a-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="d419a-122">**Активна**</span><span class="sxs-lookup"><span data-stu-id="d419a-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="d419a-123">Переключает ПИН-код в активный (приостановленный или запущенный) режим.</span><span class="sxs-lookup"><span data-stu-id="d419a-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="d419a-124">**Неактивно**</span><span class="sxs-lookup"><span data-stu-id="d419a-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="d419a-125">Переключает ПИН-код в неактивное состояние и освобождает память распределителя.</span><span class="sxs-lookup"><span data-stu-id="d419a-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="d419a-126">**сетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d419a-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="d419a-127">Задает тип носителя для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d419a-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="d419a-128">**Выделен**</span><span class="sxs-lookup"><span data-stu-id="d419a-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="d419a-129">Извлекает указатель на распределитель памяти по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d419a-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="d419a-130">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="d419a-130">IPin Methods</span></span>                                                     | <span data-ttu-id="d419a-131">Описание</span><span class="sxs-lookup"><span data-stu-id="d419a-131">Description</span></span>                                                                            |
| [<span data-ttu-id="d419a-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="d419a-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="d419a-133">Возвращает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d419a-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="d419a-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d419a-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="d419a-135">Информирует ПИН-код о том, что дополнительные данные не ожидаются до тех пор, пока не будет выполнена новая команда запуска.</span><span class="sxs-lookup"><span data-stu-id="d419a-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="d419a-136">**бегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="d419a-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="d419a-137">Информирует ПИН-код, чтобы начать операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="d419a-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="d419a-138">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="d419a-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="d419a-139">Сообщает ПИН-коду, чтобы завершить операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="d419a-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="d419a-140">Методы Имеминпутпин</span><span class="sxs-lookup"><span data-stu-id="d419a-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="d419a-141">Описание</span><span class="sxs-lookup"><span data-stu-id="d419a-141">Description</span></span>                                                                            |
| [<span data-ttu-id="d419a-142">**Получать**</span><span class="sxs-lookup"><span data-stu-id="d419a-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="d419a-143">Извлекает следующий блок данных из потока.</span><span class="sxs-lookup"><span data-stu-id="d419a-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="d419a-144">Требования</span><span class="sxs-lookup"><span data-stu-id="d419a-144">Requirements</span></span>



| <span data-ttu-id="d419a-145">Требование</span><span class="sxs-lookup"><span data-stu-id="d419a-145">Requirement</span></span> | <span data-ttu-id="d419a-146">Значение</span><span class="sxs-lookup"><span data-stu-id="d419a-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d419a-147">Header</span><span class="sxs-lookup"><span data-stu-id="d419a-147">Header</span></span><br/>  | <dl> <span data-ttu-id="d419a-148"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d419a-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d419a-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d419a-149">Library</span></span><br/> | <dl> <span data-ttu-id="d419a-150"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d419a-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




