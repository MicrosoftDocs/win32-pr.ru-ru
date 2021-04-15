---
description: Класс Крендерединпутпин является базовым классом для реализации входного ПИН-кода в модуле подготовки отчетов.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Класс Крендерединпутпин (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668654"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="5be9d-103">Класс Крендерединпутпин</span><span class="sxs-lookup"><span data-stu-id="5be9d-103">CRenderedInputPin class</span></span>

![Иерархия классов крендерединпутпин](images/rbase04.png)

<span data-ttu-id="5be9d-105">Класс **крендерединпутпин** является базовым классом для реализации входного ПИН-кода в модуле подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="5be9d-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="5be9d-106">Этот класс предназначен для фильтров модуля подготовки отчетов, которые не являются производными от класса [**кбасерендерер**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="5be9d-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="5be9d-107">(Фильтры, производные от **кбасерендерер** , должны использовать класс [**крендереринпутпин**](crendererinputpin.md) для входного ПИН-кода.)</span><span class="sxs-lookup"><span data-stu-id="5be9d-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="5be9d-108">Чтобы использовать этот класс, необходимо выполнить по крайней мере следующее:</span><span class="sxs-lookup"><span data-stu-id="5be9d-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="5be9d-109">Объявите новый класс ПИН-кода, наследующий **крендерединпутпин**.</span><span class="sxs-lookup"><span data-stu-id="5be9d-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="5be9d-110">В классе ПИН-кода объявите объект критической секции для хранения блокировки потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5be9d-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="5be9d-111">Для этой цели можно использовать класс [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="5be9d-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="5be9d-112">Дополнительные сведения см. в разделе [потоки и критические разделы](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="5be9d-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="5be9d-113">Переопределите [**крендерединпутпин:: EndOfStream**](crenderedinputpin-endofstream.md) для удержания потоковой блокировки.</span><span class="sxs-lookup"><span data-stu-id="5be9d-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="5be9d-114">Реализуйте методы [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**Кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md)и [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="5be9d-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="5be9d-115">В фильтре реализуйте [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) , чтобы вернуть экземпляр класса ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5be9d-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="5be9d-116">Этот класс можно использовать в модуле подготовки отчетов, который имеет более одного входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5be9d-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="5be9d-117">Этот класс наследует класс [**кбасеинпутпин**](cbaseinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="5be9d-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="5be9d-118">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="5be9d-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="5be9d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5be9d-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5be9d-120">**m \_ батендофстреам**</span><span class="sxs-lookup"><span data-stu-id="5be9d-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="5be9d-121">Указывает, был ли достигнут конец потока.</span><span class="sxs-lookup"><span data-stu-id="5be9d-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="5be9d-122">**m \_ бкомплетенотифиед**</span><span class="sxs-lookup"><span data-stu-id="5be9d-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="5be9d-123">Указывает, отправил ли ПИН-код событие [**\_ завершения EC**](ec-complete.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="5be9d-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="5be9d-124">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="5be9d-124">Public Methods</span></span>                                                        | <span data-ttu-id="5be9d-125">Описание</span><span class="sxs-lookup"><span data-stu-id="5be9d-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="5be9d-126">**Активен**</span><span class="sxs-lookup"><span data-stu-id="5be9d-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="5be9d-127">Уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="5be9d-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="5be9d-128">**крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="5be9d-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="5be9d-129">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5be9d-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="5be9d-130">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="5be9d-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="5be9d-131">Уведомляет ПИН-код о том, что теперь фильтр работает.</span><span class="sxs-lookup"><span data-stu-id="5be9d-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="5be9d-132">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="5be9d-132">IPin Methods</span></span>                                                          | <span data-ttu-id="5be9d-133">Описание</span><span class="sxs-lookup"><span data-stu-id="5be9d-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="5be9d-134">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="5be9d-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="5be9d-135">Завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="5be9d-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="5be9d-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="5be9d-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="5be9d-137">Уведомляет ПИН-код о том, что дополнительные данные не ожидаются до тех пор, пока фильтр не получит новую команду Run.</span><span class="sxs-lookup"><span data-stu-id="5be9d-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="5be9d-138">Требования</span><span class="sxs-lookup"><span data-stu-id="5be9d-138">Requirements</span></span>



| <span data-ttu-id="5be9d-139">Требование</span><span class="sxs-lookup"><span data-stu-id="5be9d-139">Requirement</span></span> | <span data-ttu-id="5be9d-140">Значение</span><span class="sxs-lookup"><span data-stu-id="5be9d-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5be9d-141">Header</span><span class="sxs-lookup"><span data-stu-id="5be9d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="5be9d-142"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5be9d-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5be9d-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5be9d-143">Library</span></span><br/> | <dl> <span data-ttu-id="5be9d-144"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5be9d-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




