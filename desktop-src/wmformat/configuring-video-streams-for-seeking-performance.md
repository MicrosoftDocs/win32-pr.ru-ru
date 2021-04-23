---
title: Настройка потоков видео для поиска производительности
description: Настройка потоков видео для поиска производительности
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- потоки, Настройка потоков видео
- кодеки, Настройка потоков видео
- видеопотоки, Настройка
- потоки видео, производительность
- производительность, потоки видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788718"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="1c409-108">Настройка потоков видео для поиска производительности</span><span class="sxs-lookup"><span data-stu-id="1c409-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="1c409-109">Некоторые приложения воспроизведения выполняют много операций поиска в отдельных потоках.</span><span class="sxs-lookup"><span data-stu-id="1c409-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="1c409-110">Поиск — это область, в которой производительность может сильно различаться в зависимости от параметров потока.</span><span class="sxs-lookup"><span data-stu-id="1c409-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="1c409-111">Если известно, что содержимое необходимо оптимизировать для быстрого поиска, можно настроить конфигурацию потока для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="1c409-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="1c409-112">Крупнейшим фактором, влияющим на скорость операций поиска в видео, является пространство ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="1c409-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="1c409-113">Так как каждый кадр между ключевыми кадрами необходимо воссоздать на основе кадров, которые поступают перед ним, то широкое количество ключевых кадров значительно превышает время поиска.</span><span class="sxs-lookup"><span data-stu-id="1c409-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="1c409-114">Например, если видеопоток с 30 кадрами в секунду имеет максимальный интервал между ключевыми кадрами (10 секунд), между ними есть потенциально 300 кадров.</span><span class="sxs-lookup"><span data-stu-id="1c409-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="1c409-115">Если перейти к последнему [*разностному кадру*](wmformat-glossary.md), то для распаковки фрейма необходимо перестроить кадры 299.</span><span class="sxs-lookup"><span data-stu-id="1c409-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="1c409-116">Если процесс реконструкции кадров занял .01 секунду, Поиск займет почти 3 секунды.</span><span class="sxs-lookup"><span data-stu-id="1c409-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="1c409-117">Если требуется повысить эффективность поиска, может помочь уменьшение интервала между ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="1c409-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="1c409-118">Однако если задать слишком близкое сочетание ключевых кадров, вы можете потерять качество.</span><span class="sxs-lookup"><span data-stu-id="1c409-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="1c409-119">Можно задать максимальный интервал между ключевыми кадрами, вызвав [**ивмвидеомедиапропс:: сетмакскэйфрамеспаЦинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span><span class="sxs-lookup"><span data-stu-id="1c409-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="1c409-120">Рекомендуемые значения, зависящие от скорости потока, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c409-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="1c409-121">Эти значения обеспечивают хорошее распределение производительности и качества.</span><span class="sxs-lookup"><span data-stu-id="1c409-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="1c409-122">Пакет SDK не ограничивает время между опорными кадрами.</span><span class="sxs-lookup"><span data-stu-id="1c409-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="1c409-123">Как правило, время, превышающее 30 секунд, может негативно сказаться на времени поиска, когда содержимое передается по сети и когда оно воспроизводится локально.</span><span class="sxs-lookup"><span data-stu-id="1c409-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="1c409-124">Скорость потока</span><span class="sxs-lookup"><span data-stu-id="1c409-124">Bit rate</span></span>             | <span data-ttu-id="1c409-125">Рекомендуемый максимальный интервал между рамками</span><span class="sxs-lookup"><span data-stu-id="1c409-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="1c409-126">22 кбит/с до 300 кбит/с</span><span class="sxs-lookup"><span data-stu-id="1c409-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="1c409-127">8 секунд</span><span class="sxs-lookup"><span data-stu-id="1c409-127">8 seconds</span></span>                           |
| <span data-ttu-id="1c409-128">300 кбит/с 600 кбит/с</span><span class="sxs-lookup"><span data-stu-id="1c409-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="1c409-129">6 секунд</span><span class="sxs-lookup"><span data-stu-id="1c409-129">6 seconds</span></span>                           |
| <span data-ttu-id="1c409-130">600 кбит/с – 2 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="1c409-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="1c409-131">4 секунды</span><span class="sxs-lookup"><span data-stu-id="1c409-131">4 seconds</span></span>                           |
| <span data-ttu-id="1c409-132">2 Мбит/с и выше</span><span class="sxs-lookup"><span data-stu-id="1c409-132">2 Mbps and higher</span></span>    | <span data-ttu-id="1c409-133">3 секунды</span><span class="sxs-lookup"><span data-stu-id="1c409-133">3 seconds</span></span>                           |



 

<span data-ttu-id="1c409-134">Дополнительные сведения о получении наилучшей производительности при поиске видеофайлов см. [в статье получение наилучшей производительности для поиска видео](getting-the-best-video-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="1c409-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c409-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1c409-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c409-136">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="1c409-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




