---
description: Этот класс реализует интерфейс Иамстреамконтрол для входных и выходных закрепления.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Класс Кбасестреамконтрол (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657154"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="ba9ba-103">Класс Кбасестреамконтрол</span><span class="sxs-lookup"><span data-stu-id="ba9ba-103">CBaseStreamControl class</span></span>

![Иерархия классов кбасестреамконтрол](images/strmctl1.png)

<span data-ttu-id="ba9ba-105">Этот класс реализует интерфейс [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) для входных и выходных закрепления.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="ba9ba-106">Он обеспечивает контроль над запуском и остановкой отдельного ПИН-кода в фильтре.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="ba9ba-107">ПИН-код, который поддерживает **иамстреамконтрол** , должен наследовать от этого базового класса.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="ba9ba-108">Ниже приведено типичное объявление входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="ba9ba-109">Обязательно Переопределите **нонделегатингкуеринтефаце** , чтобы предоставить **иамстреамконтрол**.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="ba9ba-110">Дополнительные сведения см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ba9ba-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="ba9ba-111">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="ba9ba-111">Public Methods</span></span>                                                        | <span data-ttu-id="ba9ba-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ba9ba-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba9ba-113">**кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="ba9ba-114">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="ba9ba-115">**~ Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="ba9ba-116">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="ba9ba-117">**чеккстреамстате**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="ba9ba-118">Определяет, следует ли доставлять или отменять образец носителя.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="ba9ba-119">**Очистки**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="ba9ba-120">Уведомляет базовый класс о том, что ПИН-код запущен или прекратил запись на диск.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="ba9ba-121">**нотифифилтерстате**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="ba9ba-122">Уведомляет ПИН-код при изменении состояния фильтра.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="ba9ba-123">**сетфилтерграф**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="ba9ba-124">Указывает приемник событий для событий потокового управления.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="ba9ba-125">**сетсинксаурце**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="ba9ba-126">Уведомляет базовый класс о текущем ссылочном времени.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="ba9ba-127">Методы Иамстреамконтрол</span><span class="sxs-lookup"><span data-stu-id="ba9ba-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="ba9ba-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ba9ba-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="ba9ba-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="ba9ba-130">Извлекает сведения о текущих параметрах управления потоком, включая время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="ba9ba-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="ba9ba-132">Информирует ПИН-код о том, когда начать доставку данных.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="ba9ba-133">**Предложения**</span><span class="sxs-lookup"><span data-stu-id="ba9ba-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="ba9ba-134">Информирует ПИН-код, когда следует отказаться от доставки данных.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="ba9ba-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba9ba-135">Remarks</span></span>

<span data-ttu-id="ba9ba-136">Этот класс требует наличия ПИН-кода и фильтра владельца для уведомления класса при возникновении различных событий, таких как фильтр присоединения к графу или получение нового ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="ba9ba-137">Необходимо вызвать следующие методы класса:</span><span class="sxs-lookup"><span data-stu-id="ba9ba-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="ba9ba-138">В методе [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) фильтра вызовите метод [**Кбасестреамконтрол:: сетсинксаурце**](cbasestreamcontrol-setsyncsource.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ba-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="ba9ba-139">Этот метод уведомляет класс текущего ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="ba9ba-140">В методе [**кбасефилтер:: жоинфилтерграф**](cbasefilter-joinfiltergraph.md) фильтра вызовите метод [**Кбасестреамконтрол:: сетфилтерграф**](cbasestreamcontrol-setfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ba-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="ba9ba-141">Этот метод предоставляет классу указатель на диспетчер графа фильтров, чтобы класс мог отправить правильные события управления потоком.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="ba9ba-142">Каждый раз, когда фильтр изменяет состояние (для запуска, приостановки или остановки), вызовите метод [**кбасестреамконтрол:: нотифифилтерстате**](cbasestreamcontrol-notifyfilterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ba-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="ba9ba-143">В методах [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) и [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) закрепления вызовите метод [**кбасестреамконтрол:: Flush**](cbasestreamcontrol-flushing.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ba-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="ba9ba-144">`CBaseStreamControl`Для определения того, какие образцы должны быть доставлены, а какие — должны быть удалены, в классе используется ссылочное время графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="ba9ba-145">В методе [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ПИН-кода вызовите метод [**Кбасестреамконтрол:: чеккстреамстате**](cbasestreamcontrol-checkstreamstate.md) с указателем на пример входящего носителя.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="ba9ba-146">Если метод возвращает поток значений \_ , доставляет пример нисходящий.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="ba9ba-147">В противном случае удалите его.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba9ba-148">Требования</span><span class="sxs-lookup"><span data-stu-id="ba9ba-148">Requirements</span></span>



| <span data-ttu-id="ba9ba-149">Требование</span><span class="sxs-lookup"><span data-stu-id="ba9ba-149">Requirement</span></span> | <span data-ttu-id="ba9ba-150">Значение</span><span class="sxs-lookup"><span data-stu-id="ba9ba-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9ba-151">Header</span><span class="sxs-lookup"><span data-stu-id="ba9ba-151">Header</span></span><br/>  | <dl> <span data-ttu-id="ba9ba-152"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba9ba-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba9ba-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba9ba-153">Library</span></span><br/> | <dl> <span data-ttu-id="ba9ba-154"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ba9ba-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




