---
description: Контроль качества по умолчанию
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Контроль качества по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072141"
---
# <a name="default-quality-control"></a><span data-ttu-id="1f137-103">Контроль качества по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1f137-103">Default Quality Control</span></span>

<span data-ttu-id="1f137-104">[Базовые классы DirectShow](directshow-base-classes.md) реализуют некоторые поведения по умолчанию для контроля качества видео.</span><span class="sxs-lookup"><span data-stu-id="1f137-104">The [DirectShow Base Classes](directshow-base-classes.md) implement some default behaviors for video quality control.</span></span>

<span data-ttu-id="1f137-105">Сообщения качества запускаются модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="1f137-105">Quality messages start at the renderer.</span></span> <span data-ttu-id="1f137-106">Базовым классом для модулей подготовки видео является [**кбасевидеорендерер**](cbasevideorenderer.md), который имеет следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="1f137-106">The base class for video renderers is [**CBaseVideoRenderer**](cbasevideorenderer.md), which has the following behavior:</span></span>

1.  <span data-ttu-id="1f137-107">Когда модуль подготовки отчетов получает пример, он сравнивает метку времени в образце с текущим временем ссылки.</span><span class="sxs-lookup"><span data-stu-id="1f137-107">When the video renderer receives a sample, it compares the time stamp on the sample with the current reference time.</span></span>
2.  <span data-ttu-id="1f137-108">Модуль подготовки видео создает качественное сообщение.</span><span class="sxs-lookup"><span data-stu-id="1f137-108">The video renderer generates a quality message.</span></span> <span data-ttu-id="1f137-109">В базовом классе элемент **пропорции** сообщения Quality ограничен диапазоном 500 (50%) до 2000 (200%).</span><span class="sxs-lookup"><span data-stu-id="1f137-109">In the base class, the **Proportion** member of the quality message is limited to a range of 500 (50%) to 2000 (200%).</span></span> <span data-ttu-id="1f137-110">Значения за пределами этого диапазона могут привести к внезапному изменению качества.</span><span class="sxs-lookup"><span data-stu-id="1f137-110">Values outside this range could result in abrupt quality changes.</span></span>
3.  <span data-ttu-id="1f137-111">По умолчанию модуль подготовки отчетов отправляет сообщение с качеством на вышестоящий выход (ПИН-код, подключенный к входному ПИН-коду).</span><span class="sxs-lookup"><span data-stu-id="1f137-111">By default, the video renderer sends the quality message to the upstream output pin (the pin connected to its input pin).</span></span> <span data-ttu-id="1f137-112">Приложения могут переопределить это поведение, вызвав метод **сетсинк** .</span><span class="sxs-lookup"><span data-stu-id="1f137-112">Applications can override this behavior by calling the **SetSink** method.</span></span>

<span data-ttu-id="1f137-113">То, что происходит дальше, зависит от вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="1f137-113">What happens next depends on the upstream filter.</span></span> <span data-ttu-id="1f137-114">Как правило, это фильтр преобразования.</span><span class="sxs-lookup"><span data-stu-id="1f137-114">Typically, this is a transform filter.</span></span> <span data-ttu-id="1f137-115">Базовый класс для фильтров преобразований — [**ктрансформфилтер**](ctransformfilter.md), который использует классы [**ктрансформинпутпин**](ctransforminputpin.md) и [**ктрансформаутпутпин**](ctransformoutputpin.md) для реализации входных и выходных закрепления.</span><span class="sxs-lookup"><span data-stu-id="1f137-115">The base class for transform filters is [**CTransformFilter**](ctransformfilter.md), which uses the [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) classes to implement input and output pins.</span></span> <span data-ttu-id="1f137-116">Вместе эти классы имеют следующие особенности.</span><span class="sxs-lookup"><span data-stu-id="1f137-116">Together, these classes have the following behavior:</span></span>

1.  <span data-ttu-id="1f137-117">Метод [**ктрансформаутпутпин:: notify**](ctransformoutputpin-notify.md) вызывает [**Ктрансформфилтер:: алтеркуалити**](ctransformfilter-alterquality.md), закрытый метод для базового класса Filter.</span><span class="sxs-lookup"><span data-stu-id="1f137-117">The [**CTransformOutputPin::Notify**](ctransformoutputpin-notify.md) method calls [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md), a private method on the filter base class.</span></span>
2.  <span data-ttu-id="1f137-118">Производные фильтры могут переопределять **алтеркуалити** для работы с сообщением качества.</span><span class="sxs-lookup"><span data-stu-id="1f137-118">Derived filters can override **AlterQuality** to handle the quality message.</span></span> <span data-ttu-id="1f137-119">По умолчанию **алтеркуалити** игнорирует сообщение Quality.</span><span class="sxs-lookup"><span data-stu-id="1f137-119">By default, **AlterQuality** ignores the quality message.</span></span>
3.  <span data-ttu-id="1f137-120">Если **алтеркуалити** не обрабатывает сообщение качества, то выходной ПИН-код вызывает [**Кбасеинпутпин::P асснотифи**](cbaseinputpin-passnotify.md), закрытый метод для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="1f137-120">If **AlterQuality** does not handle the quality message, the output pin calls [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md), a private method on the filter's input pin.</span></span>
4.  <span data-ttu-id="1f137-121">**Пасснотифи** передает качественное сообщение в соответствующее место — на следующий вышестоящий ПИН-код или пользовательский диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="1f137-121">**PassNotify** passes the quality message to the appropriate place—the next upstream output pin, or a custom quality manager.</span></span>

<span data-ttu-id="1f137-122">Если ни один из фильтров преобразований не обрабатывает сообщение качества, сообщение в конечном итоге достигает выходного ПИН-кода в фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="1f137-122">Assuming that no transform filter handles the quality message, the message eventually reaches the output pin on the source filter.</span></span> <span data-ttu-id="1f137-123">В базовых классах [**кбасепин:: notify**](cbasepin-notify.md) возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="1f137-123">In the base classes, [**CBasePin::Notify**](cbasepin-notify.md) returns E\_NOTIMPL.</span></span> <span data-ttu-id="1f137-124">Как конкретный фильтр источника обрабатывает сообщения о качествах, зависит от характера источника.</span><span class="sxs-lookup"><span data-stu-id="1f137-124">How a particular source filter handles quality messages depends on the nature of the source.</span></span> <span data-ttu-id="1f137-125">Некоторые источники, такие как запись видео в реальном времени, не могут выполнять осмысленное управление качеством.</span><span class="sxs-lookup"><span data-stu-id="1f137-125">Some sources, such as live video capture, cannot perform meaningful quality control.</span></span> <span data-ttu-id="1f137-126">Другие источники могут регулировать скорость, с которой они доставляют образцы.</span><span class="sxs-lookup"><span data-stu-id="1f137-126">Other sources can adjust the rate at which they deliver samples.</span></span>

<span data-ttu-id="1f137-127">На следующей схеме показано поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f137-127">The following diagram illustrates the default behavior.</span></span>

![контроль качества в базовых классах](images/quality-control.png)

<span data-ttu-id="1f137-129">Базовый модуль подготовки видео реализует **икуалитиконтрол:: notify**, что означает, что вы можете передавать качественные сообщения в сам модуль подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="1f137-129">The base video renderer implements **IQualityControl::Notify**, which means you can pass quality messages to the renderer itself.</span></span> <span data-ttu-id="1f137-130">Если для элемента **пропорции** задано значение меньше 1000, модуль подготовки отчетов вставляет период ожидания между каждым отображаемым кадром, в результате замедляет работу модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="1f137-130">If you set the **Proportion** member to a value less than 1000, the video renderer inserts a wait period between each frame that it renders, in effect slowing down the renderer.</span></span> <span data-ttu-id="1f137-131">(Например, это можно сделать, чтобы сократить использование системы.) Дополнительные сведения см. в разделе [**кбасевидеорендерер:: сроттлеваит**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="1f137-131">(You might do this to reduce system usage, for example.) For more information, see [**CBaseVideoRenderer::ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span> <span data-ttu-id="1f137-132">Установка для элемента **пропорций** значения больше 1000 не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="1f137-132">Setting the **Proportion** member to a value greater than 1000 has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f137-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1f137-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f137-134">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="1f137-134">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 



