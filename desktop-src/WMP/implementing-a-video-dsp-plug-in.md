---
title: Реализация подключаемого модуля DSP видео
description: Реализация подключаемого модуля DSP видео
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP видео
- подключаемые модули, DSP видео
- подключаемые модули обработки цифровых сигналов, реализация кода
- Подключаемые модули DSP, реализация кода
- подключаемые модули обработки цифровых сигналов, изменение образца кода
- Подключаемые модули DSP, изменение примера кода
- подключаемые модули обработки цифровых сигналов, реализация видео
- Подключаемые модули DSP, реализация видео
- подключаемые модули DSP видео, реализация кода
- подключаемые модули DSP видео, изменение примера кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330435"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="18ed0-113">Реализация подключаемого модуля DSP видео</span><span class="sxs-lookup"><span data-stu-id="18ed0-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="18ed0-114">Видеоадаптеры видеомониторов поддерживают набор видеоформатов.</span><span class="sxs-lookup"><span data-stu-id="18ed0-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="18ed0-115">Цифровые видеокодеки также поддерживают набор видеоформатов.</span><span class="sxs-lookup"><span data-stu-id="18ed0-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="18ed0-116">При попытке воспроизвести определенный видеофайл проигрыватель Windows Media должен выбрать формат для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="18ed0-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="18ed0-117">Проигрыватель пытается найти оптимальное соответствие форматам видеокодека и форматам, поддерживаемым видеоадаптером, то есть, который дает наивысшее качество.</span><span class="sxs-lookup"><span data-stu-id="18ed0-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="18ed0-118">Чтобы создать подключаемый модуль DSP для проигрывателя Windows Media, который обрабатывает видео, сначала необходимо решить, какие форматы видео вы хотите обработать.</span><span class="sxs-lookup"><span data-stu-id="18ed0-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="18ed0-119">Пример подключаемого модуля DSP видео работает со следующими видеоформатами:</span><span class="sxs-lookup"><span data-stu-id="18ed0-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="18ed0-120">NV12</span><span class="sxs-lookup"><span data-stu-id="18ed0-120">NV12</span></span>
-   <span data-ttu-id="18ed0-121">YV12</span><span class="sxs-lookup"><span data-stu-id="18ed0-121">YV12</span></span>
-   <span data-ttu-id="18ed0-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="18ed0-122">YUY2</span></span>
-   <span data-ttu-id="18ed0-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="18ed0-123">UYVY</span></span>
-   <span data-ttu-id="18ed0-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="18ed0-124">RGB32</span></span>
-   <span data-ttu-id="18ed0-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="18ed0-125">RGB24</span></span>
-   <span data-ttu-id="18ed0-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="18ed0-126">RGB555</span></span>
-   <span data-ttu-id="18ed0-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="18ed0-127">RGB565</span></span>

<span data-ttu-id="18ed0-128">Выберите формат, который вы выбрали для обработки.</span><span class="sxs-lookup"><span data-stu-id="18ed0-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="18ed0-129">Вы можете удалить форматы из примера подключаемого модуля, чтобы они не поддерживались дольше, а также добавить код для обработки дополнительных форматов.</span><span class="sxs-lookup"><span data-stu-id="18ed0-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="18ed0-130">В следующих разделах приведены дополнительные сведения, которые необходимо изучить перед созданием подключаемого модуля DSP видео для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18ed0-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="18ed0-131">Согласование формата видео в примере подключаемого модуля DSP видео</span><span class="sxs-lookup"><span data-stu-id="18ed0-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="18ed0-132">Допроцессаутпут в примере подключаемого модуля DSP видео</span><span class="sxs-lookup"><span data-stu-id="18ed0-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="18ed0-133">Обработка видео</span><span class="sxs-lookup"><span data-stu-id="18ed0-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="18ed0-134">См. также</span><span class="sxs-lookup"><span data-stu-id="18ed0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ed0-135">**Реализация кода DSP**</span><span class="sxs-lookup"><span data-stu-id="18ed0-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




