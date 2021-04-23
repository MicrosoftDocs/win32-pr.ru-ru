---
description: Класс Квидеотрансформфилтер разработан в основном как базовый класс для фильтров распаковки AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Класс Квидеотрансформфилтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895166"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="a49df-103">Класс Квидеотрансформфилтер</span><span class="sxs-lookup"><span data-stu-id="a49df-103">CVideoTransformFilter class</span></span>

![Иерархия классов квидеотрансформфилтер](images/vtsip01.png)

<span data-ttu-id="a49df-105">`CVideoTransformFilter`Класс разработан в основном как базовый класс для фильтров распаковки AVI.</span><span class="sxs-lookup"><span data-stu-id="a49df-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="a49df-106">Этот класс добавляет поддержку контроля качества к классу [**ктрансформфилтер**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="a49df-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="a49df-107">Метод **Receive** фильтра может принимать решение о перетаскивании кадров на основе сообщений об качествах от модуля подготовки отчетов и измерений производительности, собираемых фильтром во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="a49df-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="a49df-108">Если фильтр удаляет кадр, кадры по-своему удаляются, пока не достигнет следующего ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="a49df-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="a49df-109">Для потоков MPEG фильтр не различает фреймы B и кадры P.</span><span class="sxs-lookup"><span data-stu-id="a49df-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="a49df-110">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="a49df-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="a49df-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a49df-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a49df-112">**m \_ бкуалитичанжед**</span><span class="sxs-lookup"><span data-stu-id="a49df-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="a49df-113">Указывает, содержит ли фильтр кадры.</span><span class="sxs-lookup"><span data-stu-id="a49df-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="a49df-114">**m \_ бскиппинг**</span><span class="sxs-lookup"><span data-stu-id="a49df-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="a49df-115">Указывает, выполняется ли в данный момент фильтр для удаления кадров.</span><span class="sxs-lookup"><span data-stu-id="a49df-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="a49df-116">**m \_ итравгдекоде**</span><span class="sxs-lookup"><span data-stu-id="a49df-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="a49df-117">Среднее время, затраченное на декодирование кадра.</span><span class="sxs-lookup"><span data-stu-id="a49df-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="a49df-118">**m \_ итрлате**</span><span class="sxs-lookup"><span data-stu-id="a49df-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="a49df-119">Указывает, насколько позднее поступают образцы в модуль подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="a49df-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="a49df-120">**m \_ нфрамессинцекэйфраме**</span><span class="sxs-lookup"><span data-stu-id="a49df-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="a49df-121">Число кадров, полученных фильтром с момента последнего ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="a49df-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="a49df-122">**m \_ нкэйфрамепериод**</span><span class="sxs-lookup"><span data-stu-id="a49df-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="a49df-123">Самый крупный наблюдаемый интервал между опорными кадрами.</span><span class="sxs-lookup"><span data-stu-id="a49df-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="a49df-124">**m \_ нваитфоркэй**</span><span class="sxs-lookup"><span data-stu-id="a49df-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="a49df-125">Текущее максимальное число удаляемых разностных кадров.</span><span class="sxs-lookup"><span data-stu-id="a49df-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="a49df-126">**m \_ тдекодестарт**</span><span class="sxs-lookup"><span data-stu-id="a49df-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="a49df-127">Время, затраченное на декодирование последнего образца.</span><span class="sxs-lookup"><span data-stu-id="a49df-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="a49df-128">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="a49df-128">Protected Methods</span></span>                                                               | <span data-ttu-id="a49df-129">Описание</span><span class="sxs-lookup"><span data-stu-id="a49df-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="a49df-130">**абортплайбакк**</span><span class="sxs-lookup"><span data-stu-id="a49df-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="a49df-131">Используется для сигнализации об ошибке потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="a49df-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="a49df-132">**алтеркуалити**</span><span class="sxs-lookup"><span data-stu-id="a49df-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="a49df-133">Уведомляет фильтр о запросе изменения качества.</span><span class="sxs-lookup"><span data-stu-id="a49df-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="a49df-134">**Получать**</span><span class="sxs-lookup"><span data-stu-id="a49df-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="a49df-135">Получает пример носителя, обрабатывает его и доставляет образец вывода для подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="a49df-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="a49df-136">**шаулдскипфраме**</span><span class="sxs-lookup"><span data-stu-id="a49df-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="a49df-137">Определяет, должен ли фильтр удалять указанный образец.</span><span class="sxs-lookup"><span data-stu-id="a49df-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="a49df-138">**стартстреаминг**</span><span class="sxs-lookup"><span data-stu-id="a49df-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="a49df-139">Вызывается, когда фильтр переключается в состояние паузы.</span><span class="sxs-lookup"><span data-stu-id="a49df-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="a49df-140">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="a49df-140">Public Methods</span></span>                                                                  | <span data-ttu-id="a49df-141">Описание</span><span class="sxs-lookup"><span data-stu-id="a49df-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="a49df-142">**квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="a49df-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="a49df-143">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="a49df-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="a49df-144">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="a49df-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="a49df-145">Завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="a49df-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



