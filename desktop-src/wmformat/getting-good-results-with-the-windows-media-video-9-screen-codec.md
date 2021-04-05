---
title: Получение хороших результатов с помощью экранного видеокодека Windows Media видео 9
description: Получение хороших результатов с помощью экранного видеокодека Windows Media видео 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media Format SDK, экранный кодек Windows Media Video 9
- Улучшенный системный формат (ASF), экранный кодек Windows Media видео 9
- ASF (Расширенный системный формат), экранный кодек Windows Media видео 9
- кодеки, экран Windows Media видео 9
- Экранный кодек Windows Media Video 9, результаты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987212"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a><span data-ttu-id="43227-108">Получение хороших результатов с помощью экранного видеокодека Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="43227-108">Getting Good Results with the Windows Media Video 9 Screen Codec</span></span>

<span data-ttu-id="43227-109">Экранный кодек Windows Media Video 9 разработан для создания высокосжатого видео для снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="43227-109">The Windows Media Video 9 Screen codec is designed to produce highly compressed video for screen capture.</span></span> <span data-ttu-id="43227-110">Поскольку большая часть работы с изображением экрана включает довольно простые и статические изображения, высокие уровни сжатия обычно не означают качество изображения.</span><span class="sxs-lookup"><span data-stu-id="43227-110">Because most of the need for screen capture involves fairly simple and static images, the high levels of compression attained do not usually mean a great sacrifice in image quality.</span></span> <span data-ttu-id="43227-111">Однако каждый снимок экрана отличается, и полученное качество изображения может значительно варьироваться в зависимости от обстоятельств.</span><span class="sxs-lookup"><span data-stu-id="43227-111">However, each screen capture is different, and the resulting image quality can vary considerably depending upon the circumstances.</span></span>

<span data-ttu-id="43227-112">Лучшим способом определения параметров профиля для сеанса экранного кодека является кодирование тестового файла с помощью потока переменной с переменным качеством.</span><span class="sxs-lookup"><span data-stu-id="43227-112">The best way to determine the profile settings for a screen codec session is to encode a test file using a quality-based variable bit rate stream.</span></span> <span data-ttu-id="43227-113">Установите нужное значение качества и запишите снимок экрана, как если бы вы записывали окончательный файл.</span><span class="sxs-lookup"><span data-stu-id="43227-113">Set the quality to the value you desire, and encode a screen capture as if you were recording the final file.</span></span> <span data-ttu-id="43227-114">При написании файла воспроизводите его с помощью асинхронного объекта Reader, осуществляя регулярные вызовы [**ивмреадерадванцед:: Statistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span><span class="sxs-lookup"><span data-stu-id="43227-114">When the file is written, play it using the asynchronous reader object, making regular calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span></span> <span data-ttu-id="43227-115">Отслеживая значение элемента **двбандвидс** в структуре [**\_ \_ статистики модуля чтения WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) для каждого вызова, можно определить приблизительную скорость потока, необходимую для достижения желаемого качества.</span><span class="sxs-lookup"><span data-stu-id="43227-115">By monitoring the value of the **dwBandwidth** member of the [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure for each call, you can determine the approximate bit rate required to achieve the quality you want.</span></span> <span data-ttu-id="43227-116">Затем эту скорость можно использовать для кодирования постоянной скорости потока.</span><span class="sxs-lookup"><span data-stu-id="43227-116">You can then use that bit rate for constant bit rate encoding.</span></span>

<span data-ttu-id="43227-117">Если вы обнаружите, что желаемое качество требует более высоких разрядов, чем вы можете использовать для вашего сценария доставки, вы можете воспользоваться следующими методами, чтобы повысить эффективность кодека.</span><span class="sxs-lookup"><span data-stu-id="43227-117">If you discover that the quality you want requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec.</span></span>

-   <span data-ttu-id="43227-118">Используйте меньшее разрешение снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="43227-118">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="43227-119">Если вы захватываете более масштабное разрешение экрана, чем требуется, можно также создать путаницу для средства просмотра, выполнив дополнительные сведения, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="43227-119">Capturing a larger screen resolution than you need can also create confusion for the viewer by presenting more information than is needed.</span></span>
-   <span data-ttu-id="43227-120">Используйте меньше изображений в снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="43227-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="43227-121">Экранный кодек Windows Media Video 9 оптимизирован для кодирования примитивов и текста Windows с высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="43227-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="43227-122">Обычно проблемы возникают из-за точечной графики, которая часто содержит тысячи отдельных цветов.</span><span class="sxs-lookup"><span data-stu-id="43227-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="43227-123">Чем меньше точечных рисунков на экране при захвате, тем лучше будут результаты.</span><span class="sxs-lookup"><span data-stu-id="43227-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="43227-124">Если не удается удалить графику из снимка экрана, существует несколько способов свести к сведению, что точечный рисунок имеет качество изображения:</span><span class="sxs-lookup"><span data-stu-id="43227-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="43227-125">Уменьшите размер рисунка.</span><span class="sxs-lookup"><span data-stu-id="43227-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="43227-126">Уменьшите число отдельных графических объектов, отображаемых на экране одновременно.</span><span class="sxs-lookup"><span data-stu-id="43227-126">Reduce the number of individual graphics that appear on the screen concurrently.</span></span>
    -   <span data-ttu-id="43227-127">Уменьшите объем передвижения изображения.</span><span class="sxs-lookup"><span data-stu-id="43227-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="43227-128">Например, если изображение находится в окне, не задерживайте окно как можно более стационарным.</span><span class="sxs-lookup"><span data-stu-id="43227-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="43227-129">Старайтесь не перемещать указатель мыши над графикой или перетаскивать окна или другие элементы на изображении.</span><span class="sxs-lookup"><span data-stu-id="43227-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>
-   <span data-ttu-id="43227-130">Используйте более низкую [*частоту кадров*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="43227-130">Use a slower [*frame rate*](wmformat-glossary.md).</span></span> <span data-ttu-id="43227-131">Снимки экрана часто могут быть эффективны при очень низких частоте кадров (иногда как минимум 4 или 5 кадров в секунду).</span><span class="sxs-lookup"><span data-stu-id="43227-131">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="43227-132">Сократите скорость звучания сопроводительного звука.</span><span class="sxs-lookup"><span data-stu-id="43227-132">Reduce the bit rate of the accompanying audio.</span></span>

<span data-ttu-id="43227-133">Кроме того, кодек не поддерживает изменение размера прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="43227-133">Also, the codec does not support resizing of the video rectangle.</span></span> <span data-ttu-id="43227-134">Иными словами, если вы попытаетесь использовать кодек для кодирования экрана 800 x 600 на видеопрямоугольнике 640 x 480, полученное видео будет иметь существенные артефакты, которые могут сделать часть текста на экране неразборчива.</span><span class="sxs-lookup"><span data-stu-id="43227-134">In other words, if you try to use the codec to encode a 800 x 600 screen down into to a 640 x 480 video rectangle, the resulting video will have significant artifacts that may make much of the text on the screen illegible.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43227-135">См. также</span><span class="sxs-lookup"><span data-stu-id="43227-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43227-136">**Настройка потоков снимка экрана**</span><span class="sxs-lookup"><span data-stu-id="43227-136">**Configuring Screen Capture Streams**</span></span>](configuring-screen-capture-streams.md)
</dt> <dt>

[<span data-ttu-id="43227-137">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="43227-137">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




