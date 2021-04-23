---
title: Использование обратного преобразования видео
description: Использование обратного преобразования видео
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, обратная чересстрочности
- Windows Media Format SDK, чересстрочности
- Расширенный формат систем (ASF), обратный чересстрочности
- ASF (Расширенный системный формат), обратный чересстрочности
- Расширенный системный формат (ASF), чересстрочности
- ASF (Расширенный системный формат), чересстрочности
- Обратная чересстрочности
- чересстрочности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105691478"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="f9c32-111">Использование обратного преобразования видео</span><span class="sxs-lookup"><span data-stu-id="f9c32-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="f9c32-112">Чересстрочности — это процесс преобразования пленки с 24 кадрами в секунду на видео с 60 полями (половинными кадрами) в секунду.</span><span class="sxs-lookup"><span data-stu-id="f9c32-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="f9c32-113">Этот процесс помещает изображения из каждого кадра пленки в несколько полей видео.</span><span class="sxs-lookup"><span data-stu-id="f9c32-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="f9c32-114">При цифровой кодировке видео, созданного на основе пленки с помощью чересстрочности, процесс сжатия может вызвать артефакты движения и другие ухудшения качества.</span><span class="sxs-lookup"><span data-stu-id="f9c32-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="f9c32-115">Чтобы не влиять на качество цифрового вывода, кодек Windows Media Video 9 поддерживает инверсный чересстрочности.</span><span class="sxs-lookup"><span data-stu-id="f9c32-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="f9c32-116">При использовании обратного чересстрочности кодек восстанавливает исходные 24 пленки в секунду из входного видео перед кодированием содержимого.</span><span class="sxs-lookup"><span data-stu-id="f9c32-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="f9c32-117">Чтобы использовать обратный чересстрочности, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9c32-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="f9c32-118">Используйте профиль с потоком видео в 24 кадра в секунду.</span><span class="sxs-lookup"><span data-stu-id="f9c32-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="f9c32-119">Сведения о конфигурации полей входного видео.</span><span class="sxs-lookup"><span data-stu-id="f9c32-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="f9c32-120">Чтобы использовать обратный чересстрочности для входных данных в модуль записи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9c32-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="f9c32-121">Настройте модуль записи обычным образом.</span><span class="sxs-lookup"><span data-stu-id="f9c32-121">Set up the writer as usual.</span></span> <span data-ttu-id="f9c32-122">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="f9c32-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="f9c32-123">Прежде чем начать писать образцы, получите указатель на интерфейс [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , вызвав **Ивмвритер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f9c32-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="f9c32-124">Укажите поток для реконструирования, вызвав [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) для требуемого входного номера.</span><span class="sxs-lookup"><span data-stu-id="f9c32-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="f9c32-125">Передайте g \_ всздеинтерлацемоде в качестве значения параметра, а WM \_ DM \_ unчересстрочную развертка \_ инверсетелеЦине.</span><span class="sxs-lookup"><span data-stu-id="f9c32-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="f9c32-126">Снова вызовите **сетинпутсеттинг** , чтобы задать g \_ всзинитиалпаттернфоринверсетелеЦине.</span><span class="sxs-lookup"><span data-stu-id="f9c32-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="f9c32-127">Запишите файл обычным образом.</span><span class="sxs-lookup"><span data-stu-id="f9c32-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9c32-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f9c32-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9c32-129">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="f9c32-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="f9c32-130">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="f9c32-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="f9c32-131">**Интерфейс IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="f9c32-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




