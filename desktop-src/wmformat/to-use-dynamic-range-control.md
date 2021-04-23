---
title: Использование динамического контроля диапазона
description: Использование динамического контроля диапазона
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Пакет SDK для формата Windows Media, динамический контроль диапазона
- Windows Media Format SDK, кодек Windows Media Audio 9 Professional
- Windows Media Format SDK, кодек Windows Media Audio 9 без потерь
- Стандартный формат систем (ASF), кодек Windows Media Audio 9 Professional
- ASF (Расширенный системный формат), кодек Windows Media Audio 9 Professional
- Расширенный формат систем (ASF), кодек Windows Media Audio 9 без потерь
- ASF (Расширенный системный формат), кодек Windows Media Audio 9 без потерь
- Расширенный системный формат (ASF), динамический контроль диапазона
- ASF (Расширенный системный формат), динамический контроль диапазонов
- динамический контроль диапазона
- кодеки, кодек Windows Media Audio 9 без потерь
- кодеки, кодек Windows Media Audio 9 Professional
- Кодек Windows Media Audio 9 без потерь, динамический контроль диапазонов
- Кодек Windows Media Audio 9 Professional, динамический контроль диапазона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691442"
---
# <a name="to-use-dynamic-range-control"></a><span data-ttu-id="57601-117">Использование динамического контроля диапазона</span><span class="sxs-lookup"><span data-stu-id="57601-117">To Use Dynamic Range Control</span></span>

<span data-ttu-id="57601-118">Динамический диапазон звукового содержимого — это, по сути, различие между самым низким и максимальным томами.</span><span class="sxs-lookup"><span data-stu-id="57601-118">The dynamic range of a piece of audio content is basically the difference between the lowest volume and the maximum volume.</span></span> <span data-ttu-id="57601-119">Если динамический диапазон содержимого слишком велик, пользователи могут постоянно настраивать том во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="57601-119">If the dynamic range of the content is too high, users may find themselves adjusting the volume repeatedly during playback.</span></span> <span data-ttu-id="57601-120">Например, фильмы часто имеют большой динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="57601-120">For example, movies frequently have a high dynamic range.</span></span> <span data-ttu-id="57601-121">Часто при изменении тома таким образом, чтобы диалоговое окно можно было понять во время скрытия сцен, другие части фильма с музыкой или звуковыми эффектами являются громче, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="57601-121">Often, when the volume is adjusted so that dialog can be understood during quiet scenes, other parts of the movie with music or sound effects are louder than desired.</span></span>

<span data-ttu-id="57601-122">Кодеки Windows Media Audio 9 Professional и Windows Media Audio 9 без потерь поддерживают функцию, называемую динамическим контролем диапазона.</span><span class="sxs-lookup"><span data-stu-id="57601-122">The Windows Media Audio 9 Professional and Windows Media Audio 9 Lossless codecs support a feature called dynamic range control.</span></span> <span data-ttu-id="57601-123">Во время кодирования кодек вычисляет пиковые и средние значения амплитуды в содержимом, а объект модуля записи сохраняет эти значения в метаданных для потока при завершении кодирования.</span><span class="sxs-lookup"><span data-stu-id="57601-123">At encode time, the codec calculates the peak and average amplitude values in the content, and the writer object stores these values in the metadata for the stream when encoding is finished.</span></span> <span data-ttu-id="57601-124">При необходимости приложение может также записывать значения "Target" в виде метаданных, которые приложения проигрывателя и декодер могут использовать в качестве подсказок при воспроизведении файла.</span><span class="sxs-lookup"><span data-stu-id="57601-124">Optionally, an application can also write "target" values as metadata that player applications and the decoder can use as hints when playing back the file.</span></span> <span data-ttu-id="57601-125">Во время воспроизведения приложение может указать уровень динамического управления диапазоном, применяемый к звуковому потоку.</span><span class="sxs-lookup"><span data-stu-id="57601-125">At playback time, an application can specify the level of dynamic range control to apply to the audio stream.</span></span>

<span data-ttu-id="57601-126">Проигрыватель Windows Media реализует динамический контроль диапазона в качестве функции автоматического режима.</span><span class="sxs-lookup"><span data-stu-id="57601-126">Windows Media Player implements dynamic range control as the Quiet Mode feature.</span></span>

## <a name="when-to-use-dynamic-range-control"></a><span data-ttu-id="57601-127">Когда следует использовать динамический контроль диапазона</span><span class="sxs-lookup"><span data-stu-id="57601-127">When to Use Dynamic Range Control</span></span>

<span data-ttu-id="57601-128">Динамический контроль диапазона может изменить звук содержимого.</span><span class="sxs-lookup"><span data-stu-id="57601-128">Dynamic range control can alter the sound of the content.</span></span> <span data-ttu-id="57601-129">По этой причине не следует настраивать приложение для автоматического использования динамического управления диапазоном.</span><span class="sxs-lookup"><span data-stu-id="57601-129">For that reason, you should not configure your application to use dynamic range control automatically.</span></span> <span data-ttu-id="57601-130">Вместо этого предоставьте пользователям возможность включать или отключать динамический контроль диапазона по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="57601-130">Instead, provide users with the ability to turn dynamic range control on or off as needed.</span></span>

## <a name="using-dynamic-range-control"></a><span data-ttu-id="57601-131">Использование динамического контроля диапазона</span><span class="sxs-lookup"><span data-stu-id="57601-131">Using Dynamic Range Control</span></span>

<span data-ttu-id="57601-132">Во время воспроизведения динамический контроль диапазона активируется с помощью параметра OUTPUT g \_ всздинамикранжеконтрол.</span><span class="sxs-lookup"><span data-stu-id="57601-132">At playback time, dynamic range control is activated using the output setting g\_wszDynamicRangeControl.</span></span> <span data-ttu-id="57601-133">Для настройки параметра используйте [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="57601-133">Use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) to configure the setting.</span></span> <span data-ttu-id="57601-134">Нулевое значение (по умолчанию) указывает, что динамический диапазон не следует изменять.</span><span class="sxs-lookup"><span data-stu-id="57601-134">A value of zero (the default) indicates that the dynamic range should not be altered.</span></span> <span data-ttu-id="57601-135">Значение 1 или 2 сигнализирует кодеку выполнить динамический контроль диапазона, где 1 — средний уровень динамического сжатия диапазона, а 2 — высокий уровень динамического сжатия диапазона.</span><span class="sxs-lookup"><span data-stu-id="57601-135">A value of 1 or 2 signals the codec to perform dynamic range control, where 1 is a moderate level of dynamic range compression, and 2 is a high level of dynamic range compression.</span></span>

<span data-ttu-id="57601-136">Во время кодирования или во время воспроизведения можно предоставить значения PCM для пикового и среднего уровня, установив атрибуты [**WM/вмадркпеактаржет**](wm-wmadrcpeaktarget.md) и [**WM/вмадркаверажетаржет**](wm-wmadrcaveragetarget.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="57601-136">At encoding time or playback time, you can give the codec target PCM values for the peak and average levels by setting the [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) and [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) attributes, respectively.</span></span> <span data-ttu-id="57601-137">Эти значения хранятся в виде атрибутов метаданных, и доступ к ним должен осуществляться с помощью методов интерфейса [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) .</span><span class="sxs-lookup"><span data-stu-id="57601-137">These values are stored as metadata attributes and should be accessed using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface.</span></span> <span data-ttu-id="57601-138">При кодировании аудиопотока с использованием профессионального или телекодека атрибуты [**WM/вмадркпеакреференце**](wm-wmadrcpeakreference.md) и [**WM/вмадркаверажереференце**](wm-wmadrcaveragereference.md) автоматически устанавливаются в пиковую и среднюю степени исходного содержимого.</span><span class="sxs-lookup"><span data-stu-id="57601-138">When you encode an audio stream using the professional or lossless codec, the [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) and [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) attributes are set automatically to the peak and average levels of the original content.</span></span> <span data-ttu-id="57601-139">Целевые значения устанавливаются в те же значения, что и ссылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57601-139">The target values are set to the same values as the references by default.</span></span>

<span data-ttu-id="57601-140">Во время воспроизведения декодер вычисляет динамический диапазон на основе выбранного уровня динамического управления диапазоном и целевых значений (если они указаны).</span><span class="sxs-lookup"><span data-stu-id="57601-140">The decoder at playback time calculates the dynamic range based on the selected level of dynamic range control and the target values (if any are specified).</span></span> <span data-ttu-id="57601-141">Возможные диапазоны показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="57601-141">The possible ranges are shown in the following table.</span></span>



| <span data-ttu-id="57601-142">Параметры</span><span class="sxs-lookup"><span data-stu-id="57601-142">Settings</span></span>                                                                | <span data-ttu-id="57601-143">Диапазон доставленных аудио</span><span class="sxs-lookup"><span data-stu-id="57601-143">Range of delivered audio</span></span>                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57601-144">g \_ всздинамикранжеконтрол = 0 (любые целевые значения)</span><span class="sxs-lookup"><span data-stu-id="57601-144">g\_wszDynamicRangeControl = 0 (Any target values)</span></span>                       | <span data-ttu-id="57601-145">Тот же диапазон, что и у исходного содержимого.</span><span class="sxs-lookup"><span data-stu-id="57601-145">Same range as the original content.</span></span>                                                                                          |
| <span data-ttu-id="57601-146">g \_ всздинамикранжеконтрол = 1 (целевые значения равны ссылочным значениям)</span><span class="sxs-lookup"><span data-stu-id="57601-146">g\_wszDynamicRangeControl = 1 (Target values equal to reference values)</span></span> | <span data-ttu-id="57601-147">Средний уровень поддерживается, а пиковые значения — в среднем + 12 dB.</span><span class="sxs-lookup"><span data-stu-id="57601-147">Average level is maintained and peaks are confined to the average +12 dB.</span></span>                                                    |
| <span data-ttu-id="57601-148">g \_ всздинамикранжеконтрол = 2 (целевые значения равны ссылочным значениям)</span><span class="sxs-lookup"><span data-stu-id="57601-148">g\_wszDynamicRangeControl = 2 (Target values equal to reference values)</span></span> | <span data-ttu-id="57601-149">Средний уровень поддерживается, а пиковые значения — в среднем + 6 dB.</span><span class="sxs-lookup"><span data-stu-id="57601-149">Average level is maintained and peaks are confined to the average +6 dB.</span></span>                                                     |
| <span data-ttu-id="57601-150">g \_ всздинамикранжеконтрол = 1 (указаны целевые значения)</span><span class="sxs-lookup"><span data-stu-id="57601-150">g\_wszDynamicRangeControl = 1 (Target values specified)</span></span>                 | <span data-ttu-id="57601-151">Средний уровень задает целевое среднее значение и пиковые значения, ограниченные целевым пиковым значением.</span><span class="sxs-lookup"><span data-stu-id="57601-151">Average level set to the target average value and peaks confined to the target peak value.</span></span>                                   |
| <span data-ttu-id="57601-152">g \_ всздинамикранжеконтрол = 2 (указанные целевые значения)</span><span class="sxs-lookup"><span data-stu-id="57601-152">g\_wszDynamicRangeControl = 2 (Target values specified)</span></span>                 | <span data-ttu-id="57601-153">Средний уровень задает целевое среднее значение и пиковые значения, ограниченные медианы целевого среднего и целевого пикового значения.</span><span class="sxs-lookup"><span data-stu-id="57601-153">Average level set to the target average value and peaks confined to the median of the target average and target peak values.</span></span> |



 

<span data-ttu-id="57601-154">Обратите внимание, что динамический элемент управления диапазоном является компонентом только для декодирования и существует только в виде метаданных в самом файле.</span><span class="sxs-lookup"><span data-stu-id="57601-154">Note that dynamic range control is a feature of decoding only and exists only as metadata in the file itself.</span></span> <span data-ttu-id="57601-155">Эти параметры не влияют на содержимое, хранящееся в файле, если только вы не указываете, что декодер использует их.</span><span class="sxs-lookup"><span data-stu-id="57601-155">These settings have no effect on the content stored in the file unless you specifically instruct the decoder to use them.</span></span> <span data-ttu-id="57601-156">Пакет SDK для формата Windows Media не предоставляет методов для изменения динамического диапазона звуковых данных во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="57601-156">The Windows Media Format SDK provides no methods for modifying the dynamic range of the audio data at encoding time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57601-157">См. также</span><span class="sxs-lookup"><span data-stu-id="57601-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57601-158">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="57601-158">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 




