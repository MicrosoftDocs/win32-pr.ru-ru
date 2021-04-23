---
title: Входные параметры
description: Входные параметры
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, глобальные константы
- Расширенный системный формат (ASF), глобальные константы
- ASF (Расширенный системный формат), глобальные константы
- глобальные константы, список
- Windows Media Format SDK, константы
- Расширенный системный формат (ASF), константы
- ASF (Расширенный системный формат), константы
- константы, список
- Windows Media Format SDK, входные параметры
- Расширенный формат систем (ASF), параметры ввода
- ASF (Расширенный системный формат), параметры ввода
- входные параметры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069535"
---
# <a name="input-settings"></a><span data-ttu-id="33c5e-115">Входные параметры</span><span class="sxs-lookup"><span data-stu-id="33c5e-115">Input Settings</span></span>

<span data-ttu-id="33c5e-116">Следующие глобальные константы используются для задания входных параметров для модуля записи.</span><span class="sxs-lookup"><span data-stu-id="33c5e-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="33c5e-117">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="33c5e-117">Global constant</span></span>                        | <span data-ttu-id="33c5e-118">\_ \_ тип данных ВМТ attr</span><span class="sxs-lookup"><span data-stu-id="33c5e-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="33c5e-119">Описание параметра *pValue*</span><span class="sxs-lookup"><span data-stu-id="33c5e-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c5e-120">g \_ всздеинтерлацемоде</span><span class="sxs-lookup"><span data-stu-id="33c5e-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="33c5e-121">**ВМТ \_ Введите \_** в разделе DWORD значение одного из значений в таблице Mode раздела [, чтобы выполнить дечередование видео](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="33c5e-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="33c5e-122">Если задано значение, задает тип перечередования содержимого входных данных.</span><span class="sxs-lookup"><span data-stu-id="33c5e-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="33c5e-123">Дополнительные сведения см. в статье о [деразвертке видео](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="33c5e-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="33c5e-124">g \_ всзфикседфрамерате</span><span class="sxs-lookup"><span data-stu-id="33c5e-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="33c5e-125">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="33c5e-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="33c5e-126">Если задано значение true, то кодек не удаляет какие бы то ни было кадры во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="33c5e-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="33c5e-127">Это приведет к тому, что [*Частота кадров*](wmformat-glossary.md) выходного видеопотока будет постоянной.</span><span class="sxs-lookup"><span data-stu-id="33c5e-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="33c5e-128">Частота кадров входного потока не должна быть постоянной.</span><span class="sxs-lookup"><span data-stu-id="33c5e-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="33c5e-129">g \_ всзинитиалпаттернфоринверсетелеЦине</span><span class="sxs-lookup"><span data-stu-id="33c5e-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="33c5e-130">**ВМТ \_ Введите \_ DWORD** в качестве значения для одного из значений в исходной таблице шаблона в разделе, [чтобы выполнить дечередование видео](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="33c5e-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="33c5e-131">Если для режима чередования задано значение "инверсетелеЦине" в формате WM \_ DM \_ UNчересстрочную развертка \_ , это можно задать для указания шаблона входных данных [*чересстрочности*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="33c5e-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="33c5e-132">Дополнительные сведения см. в статье о [деразвертке видео](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="33c5e-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="33c5e-133">g \_ всзинтерлацедкодинг</span><span class="sxs-lookup"><span data-stu-id="33c5e-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="33c5e-134">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="33c5e-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="33c5e-135">При установке значения true указывает, что кодек должен кодировать поток как содержимое с чередованием.</span><span class="sxs-lookup"><span data-stu-id="33c5e-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="33c5e-136">Дополнительные сведения см. [в разделе Использование чередования видео](to-use-interlaced-video.md).</span><span class="sxs-lookup"><span data-stu-id="33c5e-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="33c5e-137">g \_ всзжпегкомпрессионкуалити</span><span class="sxs-lookup"><span data-stu-id="33c5e-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="33c5e-138">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="33c5e-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="33c5e-139">Задает уровень качества JPEG (от 1 до 100), используемый для входных данных.</span><span class="sxs-lookup"><span data-stu-id="33c5e-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="33c5e-140">g \_ всзватермаркклсид</span><span class="sxs-lookup"><span data-stu-id="33c5e-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="33c5e-141">**\_GUID типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="33c5e-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="33c5e-142">В качестве значения задается идентификатор GUID водяного знака.</span><span class="sxs-lookup"><span data-stu-id="33c5e-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="33c5e-143">g \_ всзватермаркконфиг</span><span class="sxs-lookup"><span data-stu-id="33c5e-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="33c5e-144">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="33c5e-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="33c5e-145">В качестве значения задается конфигурация водяного знака.</span><span class="sxs-lookup"><span data-stu-id="33c5e-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="33c5e-146">Это значение будет зависеть от подложки DMO.</span><span class="sxs-lookup"><span data-stu-id="33c5e-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="33c5e-147">Дополнительные сведения см. в документации по подложке.</span><span class="sxs-lookup"><span data-stu-id="33c5e-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="33c5e-148">Входные параметры, настроенные для потока, не сохраняются в записанном файле.</span><span class="sxs-lookup"><span data-stu-id="33c5e-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="33c5e-149">Если вы хотите, чтобы пользовательское средство чтения имело доступ к этим параметрам кодирования, необходимо создать настраиваемые атрибуты, чтобы сохранить их в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="33c5e-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="33c5e-150">См. также</span><span class="sxs-lookup"><span data-stu-id="33c5e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c5e-151">**IWMWriterAdvanced2:: Жетинпутсеттинг**</span><span class="sxs-lookup"><span data-stu-id="33c5e-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="33c5e-152">**IWMWriterAdvanced2:: Сетинпутсеттинг**</span><span class="sxs-lookup"><span data-stu-id="33c5e-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




