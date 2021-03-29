---
description: Класс Кбасеаутпутпин является абстрактным базовым классом, который реализует выходной ПИН-код.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Класс Кбасеаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657704"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="f560e-103">Класс Кбасеаутпутпин</span><span class="sxs-lookup"><span data-stu-id="f560e-103">CBaseOutputPin class</span></span>

![Иерархия классов кбасеаутпутпин](images/filter06.png)

<span data-ttu-id="f560e-105">`CBaseOutputPin`Класс является абстрактным базовым классом, который реализует выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="f560e-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="f560e-106">Этот класс является производным от [**кбасепин**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="f560e-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="f560e-107">Он отличается от **кбасепин** в следующих отношениях:</span><span class="sxs-lookup"><span data-stu-id="f560e-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="f560e-108">Он подключается только к входным ПИН-данным, поддерживающим интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="f560e-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="f560e-109">Он поддерживает транспорт локальной памяти через интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="f560e-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="f560e-110">Он отклоняет уведомления конца потока, очистки и создания сегментов.</span><span class="sxs-lookup"><span data-stu-id="f560e-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="f560e-111">(Они не должны отправляться на выходной ПИН-код.)</span><span class="sxs-lookup"><span data-stu-id="f560e-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="f560e-112">Он предоставляет методы для доставки образцов в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="f560e-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="f560e-113">Когда ПИН-код подключается, он запрашивает распределитель памяти из входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="f560e-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="f560e-114">При этом создается новый объект распределителя.</span><span class="sxs-lookup"><span data-stu-id="f560e-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="f560e-115">Закрепление вывода отвечает за настройку свойств распределителя.</span><span class="sxs-lookup"><span data-stu-id="f560e-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="f560e-116">Это достигается с помощью чистого виртуального метода [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="f560e-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="f560e-117">Переопределите этот метод в производном классе.</span><span class="sxs-lookup"><span data-stu-id="f560e-117">Override this method in your derived class.</span></span> <span data-ttu-id="f560e-118">Если входной ПИН-код имеет любые требования к буферу, они передаются в метод **деЦидебуфферсизе** .</span><span class="sxs-lookup"><span data-stu-id="f560e-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="f560e-119">Вызовите метод [**кбасеаутпутпин:: жетделиверибуффер**](cbaseoutputpin-getdeliverybuffer.md) , чтобы получить пустой пример носителя.</span><span class="sxs-lookup"><span data-stu-id="f560e-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="f560e-120">Вызовите метод [**кбасеаутпутпин::D еливер**](cbaseoutputpin-deliver.md) , чтобы доставлять образцы в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="f560e-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="f560e-121">Производный класс должен переопределять чистый виртуальный метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) для проверки типа носителя во время подключения ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="f560e-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="f560e-122">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="f560e-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="f560e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f560e-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f560e-124">**m \_ паллокатор**</span><span class="sxs-lookup"><span data-stu-id="f560e-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="f560e-125">Указатель на распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="f560e-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="f560e-126">**m \_ пинпутпин**</span><span class="sxs-lookup"><span data-stu-id="f560e-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="f560e-127">Указатель на входной ПИН-код, подключенный к этому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="f560e-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="f560e-128">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="f560e-128">Public Methods</span></span>                                                  | <span data-ttu-id="f560e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="f560e-129">Description</span></span>                                                                |
| [<span data-ttu-id="f560e-130">**кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="f560e-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="f560e-131">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f560e-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="f560e-132">**комплетеконнект**</span><span class="sxs-lookup"><span data-stu-id="f560e-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="f560e-133">Завершает соединение с входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="f560e-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="f560e-134">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-134">Virtual.</span></span>                           |
| [<span data-ttu-id="f560e-135">**деЦидеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="f560e-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="f560e-136">Выбирает распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="f560e-136">Selects a memory allocator.</span></span> <span data-ttu-id="f560e-137">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="f560e-138">**жетделиверибуффер**</span><span class="sxs-lookup"><span data-stu-id="f560e-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="f560e-139">Извлекает пример носителя, содержащий пустой буфер.</span><span class="sxs-lookup"><span data-stu-id="f560e-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="f560e-140">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-140">Virtual.</span></span>           |
| [<span data-ttu-id="f560e-141">**Доставка**</span><span class="sxs-lookup"><span data-stu-id="f560e-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="f560e-142">Доставляет пример носителя для подключенного входного контакта.</span><span class="sxs-lookup"><span data-stu-id="f560e-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="f560e-143">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-143">Virtual.</span></span>               |
| [<span data-ttu-id="f560e-144">**иниталлокатор**</span><span class="sxs-lookup"><span data-stu-id="f560e-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="f560e-145">Создает распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="f560e-145">Creates a memory allocator.</span></span> <span data-ttu-id="f560e-146">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="f560e-147">**чеккконнект**</span><span class="sxs-lookup"><span data-stu-id="f560e-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="f560e-148">Определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="f560e-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="f560e-149">**бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="f560e-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="f560e-150">Освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="f560e-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="f560e-151">**Активна**</span><span class="sxs-lookup"><span data-stu-id="f560e-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="f560e-152">Уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="f560e-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="f560e-153">**Неактивно**</span><span class="sxs-lookup"><span data-stu-id="f560e-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="f560e-154">Уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="f560e-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="f560e-155">**деливерендофстреам**</span><span class="sxs-lookup"><span data-stu-id="f560e-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="f560e-156">Доставляет уведомление в виде конца потока в подключенный входной ПИН-код. Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="f560e-157">**деливербегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="f560e-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="f560e-158">Запрашивает подключенный входной ПИН-код для начала операции очистки.</span><span class="sxs-lookup"><span data-stu-id="f560e-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="f560e-159">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-159">Virtual.</span></span>      |
| [<span data-ttu-id="f560e-160">**деливерендфлуш**</span><span class="sxs-lookup"><span data-stu-id="f560e-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="f560e-161">Запрашивает подключенный входной ПИН-код для завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="f560e-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="f560e-162">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-162">Virtual.</span></span>        |
| [<span data-ttu-id="f560e-163">**деливерневсегмент**</span><span class="sxs-lookup"><span data-stu-id="f560e-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="f560e-164">Доставляет уведомление о новом сегменте для подключенного входного контакта.</span><span class="sxs-lookup"><span data-stu-id="f560e-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="f560e-165">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="f560e-165">Virtual.</span></span>   |
| <span data-ttu-id="f560e-166">Чистые виртуальные методы</span><span class="sxs-lookup"><span data-stu-id="f560e-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="f560e-167">Описание</span><span class="sxs-lookup"><span data-stu-id="f560e-167">Description</span></span>                                                                |
| [<span data-ttu-id="f560e-168">**деЦидебуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="f560e-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="f560e-169">Устанавливает требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="f560e-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="f560e-170">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="f560e-170">IPin Methods</span></span>                                                    | <span data-ttu-id="f560e-171">Описание</span><span class="sxs-lookup"><span data-stu-id="f560e-171">Description</span></span>                                                                |
| [<span data-ttu-id="f560e-172">**бегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="f560e-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="f560e-173">Начинает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="f560e-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="f560e-174">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="f560e-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="f560e-175">Завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="f560e-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="f560e-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="f560e-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="f560e-177">Уведомляет ПИН-код о том, что дополнительные данные не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="f560e-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="f560e-178">Требования</span><span class="sxs-lookup"><span data-stu-id="f560e-178">Requirements</span></span>



| <span data-ttu-id="f560e-179">Требование</span><span class="sxs-lookup"><span data-stu-id="f560e-179">Requirement</span></span> | <span data-ttu-id="f560e-180">Значение</span><span class="sxs-lookup"><span data-stu-id="f560e-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f560e-181">Header</span><span class="sxs-lookup"><span data-stu-id="f560e-181">Header</span></span><br/>  | <dl> <span data-ttu-id="f560e-182"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f560e-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f560e-183">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f560e-183">Library</span></span><br/> | <dl> <span data-ttu-id="f560e-184"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f560e-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




