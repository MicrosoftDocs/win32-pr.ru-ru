---
title: Шаблоны соответствия аудио устройства
description: Шаблоны соответствия аудио устройства
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, шаблоны соответствия устройств
- Расширенный формат систем (ASF), шаблоны соответствия устройств
- ASF (Расширенный системный формат), шаблоны соответствия устройств
- Windows Media Format SDK, шаблоны соответствия аудио устройства
- Расширенный формат систем (ASF), шаблоны соответствия аудио-устройств
- ASF (Расширенный системный формат), шаблоны соответствия аудио-устройств
- Кодек Windows Media Audio 9, шаблон соответствия аудио устройства
- кодеки, кодек Windows Media Audio 9
- шаблоны соответствия устройств, видео
- шаблоны соответствия аудио устройства
- шаблоны, шаблоны соответствия аудиоустройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329896"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="042bf-114">Шаблоны соответствия аудио устройства</span><span class="sxs-lookup"><span data-stu-id="042bf-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="042bf-115">В следующей таблице перечислены шаблоны соответствия устройств и связанные параметры для кодека Windows Media Audio 9 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="042bf-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="042bf-116">Строка шаблона</span><span class="sxs-lookup"><span data-stu-id="042bf-116">Template string</span></span> | <span data-ttu-id="042bf-117">Диапазон скорости в битах</span><span class="sxs-lookup"><span data-stu-id="042bf-117">Bit rate range</span></span>     | <span data-ttu-id="042bf-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="042bf-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042bf-119">L1</span><span class="sxs-lookup"><span data-stu-id="042bf-119">"L1"</span></span>            | <span data-ttu-id="042bf-120">64 кбит/с 160 кбит/с</span><span class="sxs-lookup"><span data-stu-id="042bf-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="042bf-121">Этот шаблон предназначен для устройств с ограниченным звуком.</span><span class="sxs-lookup"><span data-stu-id="042bf-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="042bf-122">L2</span><span class="sxs-lookup"><span data-stu-id="042bf-122">"L2"</span></span>            | <span data-ttu-id="042bf-123"><= 160 кбит/с</span><span class="sxs-lookup"><span data-stu-id="042bf-123"><= 160 Kbps</span></span>     | <span data-ttu-id="042bf-124">Этот шаблон соответствует классу 4 в пакете Windows Media Audioing Kit, который поддерживает всю реализацию декодера Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="042bf-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="042bf-125">Индекс</span><span class="sxs-lookup"><span data-stu-id="042bf-125">"L3"</span></span>            | <span data-ttu-id="042bf-126"><= 384 кбит/с</span><span class="sxs-lookup"><span data-stu-id="042bf-126"><= 384 Kbps</span></span>     | <span data-ttu-id="042bf-127">Этот шаблон соответствует классу 4 в пакете Windows Media Audioing Kit, который поддерживает всю реализацию декодера Windows Media Audio. Диапазон скорости потока является единственным различием между этим шаблоном и L2.</span><span class="sxs-lookup"><span data-stu-id="042bf-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="042bf-128">Н</span><span class="sxs-lookup"><span data-stu-id="042bf-128">"L"</span></span>             | <span data-ttu-id="042bf-129">Все скорости</span><span class="sxs-lookup"><span data-stu-id="042bf-129">All bit rates</span></span>      | <span data-ttu-id="042bf-130">Этот шаблон предназначен для использования только с личными компьютерами и обычно используется для демонстрации всех возможностей кодека.</span><span class="sxs-lookup"><span data-stu-id="042bf-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="042bf-131">В следующей таблице перечислены шаблоны соответствия устройств и связанные параметры для голосового кодека Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="042bf-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="042bf-132">Строка шаблона</span><span class="sxs-lookup"><span data-stu-id="042bf-132">Template string</span></span> | <span data-ttu-id="042bf-133">Диапазон скорости в битах</span><span class="sxs-lookup"><span data-stu-id="042bf-133">Bit rate range</span></span> | <span data-ttu-id="042bf-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="042bf-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042bf-135">S1</span><span class="sxs-lookup"><span data-stu-id="042bf-135">"S1"</span></span>            | <span data-ttu-id="042bf-136"><= 20 кбит/с</span><span class="sxs-lookup"><span data-stu-id="042bf-136"><= 20 Kbps</span></span>  | <span data-ttu-id="042bf-137">Этот шаблон предназначен только для устройств с очень низким уровнем сложности. Этот шаблон предназначен только для речи.</span><span class="sxs-lookup"><span data-stu-id="042bf-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="042bf-138">S2</span><span class="sxs-lookup"><span data-stu-id="042bf-138">"S2"</span></span>            | <span data-ttu-id="042bf-139"><= 20 кбит/с</span><span class="sxs-lookup"><span data-stu-id="042bf-139"><= 20 Kbps</span></span>  | <span data-ttu-id="042bf-140">Это рекомендуемый шаблон для большинства приложений. Этот шаблон поддерживает сочетания речи и музыки.</span><span class="sxs-lookup"><span data-stu-id="042bf-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="042bf-141">В следующей таблице перечислены шаблоны соответствия устройств и связанные параметры для кодека Windows Media Audio 9 Professional или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="042bf-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="042bf-142">Строка шаблона</span><span class="sxs-lookup"><span data-stu-id="042bf-142">Template string</span></span> | <span data-ttu-id="042bf-143">Свойства</span><span class="sxs-lookup"><span data-stu-id="042bf-143">Properties</span></span>                                                                                   | <span data-ttu-id="042bf-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="042bf-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042bf-145">M1</span><span class="sxs-lookup"><span data-stu-id="042bf-145">"M1"</span></span>            | <span data-ttu-id="042bf-146">Скорость разрядности <= 384 скорость Кбпссамплинг <= 48 кГц</span><span class="sxs-lookup"><span data-stu-id="042bf-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="042bf-147">Каналы <= 5,1</span><span class="sxs-lookup"><span data-stu-id="042bf-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="042bf-148">Этот шаблон рекомендуется для стандартных фильмов с окружающим звуком.</span><span class="sxs-lookup"><span data-stu-id="042bf-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="042bf-149">M2</span><span class="sxs-lookup"><span data-stu-id="042bf-149">"M2"</span></span>            | <span data-ttu-id="042bf-150">Скорость разрядности <= 768 скорость Кбпссамплинг <= 96 кГц</span><span class="sxs-lookup"><span data-stu-id="042bf-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="042bf-151">Каналы <= 5,1</span><span class="sxs-lookup"><span data-stu-id="042bf-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="042bf-152">Этот шаблон рекомендуется использовать для фильмов высокой четкости с окружающим звуком.</span><span class="sxs-lookup"><span data-stu-id="042bf-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="042bf-153">M3</span><span class="sxs-lookup"><span data-stu-id="042bf-153">"M3"</span></span>            | <span data-ttu-id="042bf-154">Скорость разрядности <= 1 500 скорость Кбпссамплинг <= 96 кГц</span><span class="sxs-lookup"><span data-stu-id="042bf-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="042bf-155">Каналы <= 7,1</span><span class="sxs-lookup"><span data-stu-id="042bf-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="042bf-156">Этот шаблон рекомендуется использовать для фильмов высокой четкости с 8-канальным звуковым звучанием, таким как содержимое, закодированное для презентации в кинотеатрах.</span><span class="sxs-lookup"><span data-stu-id="042bf-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="042bf-157">"M"</span><span class="sxs-lookup"><span data-stu-id="042bf-157">"M"</span></span>             | <span data-ttu-id="042bf-158">Скорость выборки всех битов Ратесалл</span><span class="sxs-lookup"><span data-stu-id="042bf-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="042bf-159">Все каналы</span><span class="sxs-lookup"><span data-stu-id="042bf-159">All channels</span></span><br/>                           | <span data-ttu-id="042bf-160">Этот шаблон предназначен для использования только с личными компьютерами и обычно используется для демонстрации всех возможностей кодека. Это также обозначение шаблона для всех аудиозаписей, закодированных с помощью кодека Windows Media Audio 9 без потерь.</span><span class="sxs-lookup"><span data-stu-id="042bf-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="042bf-161">См. также</span><span class="sxs-lookup"><span data-stu-id="042bf-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042bf-162">**Параметры шаблона соответствия устройств**</span><span class="sxs-lookup"><span data-stu-id="042bf-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="042bf-163">**Рекомендуемые сочетания шаблонов соответствия устройств**</span><span class="sxs-lookup"><span data-stu-id="042bf-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="042bf-164">**Шаблоны соответствия видеоустройств**</span><span class="sxs-lookup"><span data-stu-id="042bf-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





