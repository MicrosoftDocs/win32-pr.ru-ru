---
title: Работа с аудио High-Resolution PCM
description: Работа с аудио High-Resolution PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Расширенный формат систем (ASF), аудиокодек PCM с высоким разрешением
- ASF (Расширенный системный формат), звук PCM с высоким разрешением
- профили, звук PCM с высоким разрешением
- кодеки, звук PCM с высоким разрешением
- Расширенный формат систем (ASF), звук PCM
- ASF (расширенный формат систем), звук PCM
- профили, звук PCM
- кодеки, звук PCM
- звук PCM с высоким разрешением
- Звук PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987625"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="01d96-113">Работа с аудио High-Resolution PCM</span><span class="sxs-lookup"><span data-stu-id="01d96-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="01d96-114">Некоторые форматы входных данных для кодека Windows Media Audio 9 Professional и кодека Windows Media Audio 9 без потерь — это форматы PCM с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="01d96-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="01d96-115">Это форматы PCM, которые содержат более двух каналов или более 16 бит на выборку (звук с более чем двумя каналами, называется также многоканальным аудио).</span><span class="sxs-lookup"><span data-stu-id="01d96-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="01d96-116">Эти форматы настраиваются с помощью структурированного расширения структуры [**вавеформатекс**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , именуемой [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="01d96-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="01d96-117">Структура **вавеформатекстенсибле** включает сведения о каналах, включенных в аудио.</span><span class="sxs-lookup"><span data-stu-id="01d96-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="01d96-118">Эта структура необходима при использовании звука PCM с высоким разрешением, так как некоторые API Windows не будут принимать структуры **вавеформатекс** , содержащие значения высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="01d96-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="01d96-119">Форматы PCM с высоким разрешением содержат 22 байта расширенных данных, которые задаются в элементе **кбсизе** структуры **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="01d96-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="01d96-120">В форматах Windows Media Audio с высоким разрешением не используется структура **вавеформатекстенсибле** , но Расширенные данные добавляются в структуру **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="01d96-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="01d96-121">Аудиокодеки Windows Media поддерживают декодирование только форматов PCM с высоким разрешением, когда приложение работает под управлением Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="01d96-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="01d96-122">В предыдущих версиях Microsoft Windows кодеки производят декодирование в формат с максимальным числом 16 бит на выборку и двумя каналами.</span><span class="sxs-lookup"><span data-stu-id="01d96-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="01d96-123">Кроме того, необходимо указать, что кодек будет декодировать в PCM высокой четкости, установив \_ для параметра g всзенабледискретеаутпут Output значение **true** с помощью метода [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="01d96-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="01d96-124">После выполнения этого вызова выходные данные, перечисленные модулем чтения, будут содержать форматы высокой четкости.</span><span class="sxs-lookup"><span data-stu-id="01d96-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="01d96-125">Для многоканального звука требуется дополнительная настройка.</span><span class="sxs-lookup"><span data-stu-id="01d96-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="01d96-126">Дополнительные сведения см. в разделе [Чтение многоканального звука](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="01d96-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01d96-127">См. также</span><span class="sxs-lookup"><span data-stu-id="01d96-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d96-128">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="01d96-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 