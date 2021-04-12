---
title: Изменение размера видео
description: Изменение размера видео
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK, изменение размера видео
- Windows Media Format SDK, изменение размера видео
- Расширенный формат систем (ASF), изменение размера видео
- ASF (расширенный формат систем), изменение размера видео
- Расширенный формат систем (ASF), изменение размера видео
- ASF (Расширенный системный формат), изменение размера видео
- изменение размера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253051"
---
# <a name="video-resizing"></a><span data-ttu-id="66409-110">Изменение размера видео</span><span class="sxs-lookup"><span data-stu-id="66409-110">Video Resizing</span></span>

<span data-ttu-id="66409-111">При определении параметров видеопотока необходимо указать ширину и высоту для кадров видео.</span><span class="sxs-lookup"><span data-stu-id="66409-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="66409-112">Этот размер видео определяет размер кадров видео, закодированных в разделе данных файла.</span><span class="sxs-lookup"><span data-stu-id="66409-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="66409-113">Однако размер видео в профиле не определяет и не ограничивает размер входного носителя, который вы поставляете в модуль записи, или размер выходного носителя, полученного от читателя.</span><span class="sxs-lookup"><span data-stu-id="66409-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="66409-114">Модуль записи может изменять размер кадров видео в соответствии с потребностями приложения.</span><span class="sxs-lookup"><span data-stu-id="66409-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="66409-115">Размер изображения видео можно рассматривать как три этапа: размер входного видео, размер потокового видео и размер выходного видео.</span><span class="sxs-lookup"><span data-stu-id="66409-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="66409-116">Размер входного видео — это размер кадров, которые передаются в качестве образцов объекту модуля записи.</span><span class="sxs-lookup"><span data-stu-id="66409-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="66409-117">Этот размер определяется как одно из обязательных свойств входного видео.</span><span class="sxs-lookup"><span data-stu-id="66409-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="66409-118">Дополнительные сведения о входных свойствах см. [в разделе Перечисление входных форматов](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="66409-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="66409-119">Размер потока видео — это размер кадров в разделе данных ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="66409-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="66409-120">Этот размер определяется как один из требуемых параметров конфигурации потока в профиле.</span><span class="sxs-lookup"><span data-stu-id="66409-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="66409-121">При записи файла, а размер входного видео отличается от размера потока видео, модуль записи изменяет размер кадров при кодировании.</span><span class="sxs-lookup"><span data-stu-id="66409-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="66409-122">Дополнительные сведения о свойствах потока видео см. в разделе [Настройка потоков видео](configuring-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="66409-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="66409-123">Размер выходных видео — это размер кадров, доставляемых модулем чтения или синхронным модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="66409-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="66409-124">Этот размер определяется как одно из требуемых свойств вывода видео.</span><span class="sxs-lookup"><span data-stu-id="66409-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="66409-125">При чтении файла, а размер выходного видео отличается от размера потока видео, читатель изменяет размер кадров при декодировании.</span><span class="sxs-lookup"><span data-stu-id="66409-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="66409-126">Нельзя задать размер видео в потоке на нечетное число пикселей в ширину.</span><span class="sxs-lookup"><span data-stu-id="66409-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="66409-127">Если задать для ширины потока видео нечетное значение, то либо профиль не будет приниматься модулем записи, либо полученное видео будет закодировано черной линией на одну сторону, чтобы сделать разницу.</span><span class="sxs-lookup"><span data-stu-id="66409-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="66409-128">При изменении размера видео следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="66409-128">You should take care when resizing video.</span></span> <span data-ttu-id="66409-129">Изображения, как правило, лучше выглядят по своему исходному разрешению.</span><span class="sxs-lookup"><span data-stu-id="66409-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="66409-130">Изменение размера изображений часто может вызвать искажение и сделать текст неразборчива.</span><span class="sxs-lookup"><span data-stu-id="66409-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="66409-131">Если вы сжимаете видео с низкой скоростью, вы также обнаружите, что изменение размера искажений может привести к серьезным артефактам сжатия.</span><span class="sxs-lookup"><span data-stu-id="66409-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="66409-132">Экранный кодек Windows Media видео 9 не поддерживает изменение размера.</span><span class="sxs-lookup"><span data-stu-id="66409-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66409-133">См. также</span><span class="sxs-lookup"><span data-stu-id="66409-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66409-134">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="66409-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="66409-135">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="66409-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="66409-136">**Работа с выходами**</span><span class="sxs-lookup"><span data-stu-id="66409-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




