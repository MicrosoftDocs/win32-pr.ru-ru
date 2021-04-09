---
title: Для дечередования видео
description: Для дечередования видео
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, видео с чередованием
- Windows Media Format SDK, обратная чересстрочности
- Windows Media Format SDK, чересстрочности
- Расширенный формат систем (ASF), видео с чередованием
- ASF (расширенный формат систем), видео с чередованием
- Расширенный формат систем (ASF), обратный чересстрочности
- ASF (Расширенный системный формат), обратный чересстрочности
- Расширенный системный формат (ASF), чересстрочности
- ASF (Расширенный системный формат), чересстрочности
- видео с чередованием
- Обратная чересстрочности, сведения
- чересстрочности, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069582"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="5ab87-115">Для дечередования видео</span><span class="sxs-lookup"><span data-stu-id="5ab87-115">To Deinterlace Video</span></span>

<span data-ttu-id="5ab87-116">Некоторые источники видео, такие как карты видеозаписи, предоставляют видеоданные для вывода с чередованием.</span><span class="sxs-lookup"><span data-stu-id="5ab87-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="5ab87-117">Каждый кадр с чередованием видео состоит из двух полей.</span><span class="sxs-lookup"><span data-stu-id="5ab87-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="5ab87-118">Верхнее поле содержит первую строку видео, а затем все остальные строки.</span><span class="sxs-lookup"><span data-stu-id="5ab87-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="5ab87-119">Затем в нижнем поле содержится вторая строка видео и все остальные строки.</span><span class="sxs-lookup"><span data-stu-id="5ab87-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="5ab87-120">Поэтому одно поле содержит все четные нумерованные строки, а другое — все нечетные строки.</span><span class="sxs-lookup"><span data-stu-id="5ab87-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="5ab87-121">Поля, составляющие кадр, представляют несколько различий представления, так что при чередовании они не формируют статическое изображение.</span><span class="sxs-lookup"><span data-stu-id="5ab87-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="5ab87-122">Если требуется отображать видео на мониторе компьютера, каждый кадр видео должен отображаться как один рисунок (этот способ отображения всего кадра видео в один раз называется *прогрессивным* видео). При поэтапном показе видео с чередованием кадры могут выглядеть неправильно, поскольку разница во времени между двумя полями.</span><span class="sxs-lookup"><span data-stu-id="5ab87-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="5ab87-123">Видеокодек Windows Media Video и кодек Windows Media Video расширенный профиль поддерживают функцию предварительной обработки, преобразующую чередующиеся содержимое в прогрессивные кадры.</span><span class="sxs-lookup"><span data-stu-id="5ab87-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="5ab87-124">Чтобы получить видео с расчередованием для кодека, вызовите метод [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) .</span><span class="sxs-lookup"><span data-stu-id="5ab87-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="5ab87-125">Параметр для использования — g \_ всздеинтерлацемоде.</span><span class="sxs-lookup"><span data-stu-id="5ab87-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="5ab87-126">Задайте для режима разчередования одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5ab87-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ab87-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5ab87-127">Value</span></span></th>
<th><span data-ttu-id="5ab87-128">Описание</span><span class="sxs-lookup"><span data-stu-id="5ab87-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ab87-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="5ab87-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="5ab87-130">Входные данные прогрессивны.</span><span class="sxs-lookup"><span data-stu-id="5ab87-130">Input is progressive.</span></span> <span data-ttu-id="5ab87-131">Используйте этот параметр, чтобы прерывать разчересстрочную развертку, если предварительно присвоить режиму разчередования другое значение.</span><span class="sxs-lookup"><span data-stu-id="5ab87-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab87-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="5ab87-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="5ab87-133">Выберите этот режим для смешения четных и нечетных полей с чередованием кадров (с использованием механизма компенсации движения). Среди</span><span class="sxs-lookup"><span data-stu-id="5ab87-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab87-134">Артефакты с чередованием последовательных экранов значительно сокращаются.</span><span class="sxs-lookup"><span data-stu-id="5ab87-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="5ab87-135">Видеокодек Windows Media видео обеспечивает более качественное сжатое видео.</span><span class="sxs-lookup"><span data-stu-id="5ab87-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab87-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="5ab87-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="5ab87-137">Выберите этот режим, если разрешение на выход имеет половину или меньшее разрешение входных данных.</span><span class="sxs-lookup"><span data-stu-id="5ab87-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="5ab87-138">Например, используйте этот режим, если разрешение входного видео равно 640 x 480 пикселей, а выходное видео имеет разрешение 320 x 240 пикселей. Среди</span><span class="sxs-lookup"><span data-stu-id="5ab87-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab87-139">Артефакты с чередованием последовательных экранов значительно сокращаются.</span><span class="sxs-lookup"><span data-stu-id="5ab87-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab87-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="5ab87-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="5ab87-141">Выберите этот режим, если разрешение на выход равно половине или меньше, чем разрешение ввода, а <a href="wmformat-glossary.md"><em>Частота кадров</em></a> вывода — в два раза больше.</span><span class="sxs-lookup"><span data-stu-id="5ab87-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="5ab87-142">Например, используйте этот режим, если разрешение входного видео равно 640 x 480 пикселей в 30 кадров/с и разрешение выходного видео равно 320 x 240 пикселей в кадрах 60/с. Среди</span><span class="sxs-lookup"><span data-stu-id="5ab87-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab87-143">Это создает прогрессивные кадры высокого качества, так как каждое поле преобразуется в рамку, поэтому нет необходимости смешивать какие-либо сведения.</span><span class="sxs-lookup"><span data-stu-id="5ab87-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="5ab87-144">Захватывается полное перемещение чередующихся полей.</span><span class="sxs-lookup"><span data-stu-id="5ab87-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab87-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="5ab87-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="5ab87-146">Выберите этот режим для преобразования видео телеЦинед 30 кадров/с в 24 кадра/с из исходной пленки. Среди</span><span class="sxs-lookup"><span data-stu-id="5ab87-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab87-147">Качество сжатия значительно улучшается, так как необходимо кодировать только 24 кадра/с, а не 30 кадров/с.</span><span class="sxs-lookup"><span data-stu-id="5ab87-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="5ab87-148">Поскольку результат является прогрессивным, реализуются те же возможности сжатия и просмотра, что и при дечередовании.</span><span class="sxs-lookup"><span data-stu-id="5ab87-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab87-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="5ab87-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="5ab87-150">Выберите этот режим, если вертикальное разрешение на выводе имеет половину или меньшее разрешение входного вертикального разрешения, а <a href="wmformat-glossary.md"><em>Частота кадров</em></a> вывода — в два раза больше.</span><span class="sxs-lookup"><span data-stu-id="5ab87-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="5ab87-151">Например, вертикальное разрешение видео составляет 640 x 480 пикселей в 30 чередующихся кадров/с, а вертикальное разрешение видео — 320 x 240 пикселей в кадрах 60/с. Среди</span><span class="sxs-lookup"><span data-stu-id="5ab87-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab87-152">Это создает прогрессивные кадры высокого качества, так как каждое поле преобразуется в рамку, поэтому нет необходимости смешивать какие-либо сведения.</span><span class="sxs-lookup"><span data-stu-id="5ab87-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="5ab87-153">Захватывается полное перемещение чередующихся полей.</span><span class="sxs-lookup"><span data-stu-id="5ab87-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5ab87-154">Для смешанного содержимого перед передачей образцов нового типа задайте режим разчередования.</span><span class="sxs-lookup"><span data-stu-id="5ab87-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="5ab87-155">Например, чтобы начать кодирование с помощью прогрессивного ввода, не нужно задавать режим разследовательного чередования.</span><span class="sxs-lookup"><span data-stu-id="5ab87-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="5ab87-156">Если для некоторых примеров требуется нормальное дечередование, необходимо установить режим разчередования для WM \_ DM \_ unразвертка \_ Обычная.</span><span class="sxs-lookup"><span data-stu-id="5ab87-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="5ab87-157">Чтобы обработать дополнительные прогрессивные примеры, необходимо установить режим разчередования для WM \_ DM \_ нотинтерлацед.</span><span class="sxs-lookup"><span data-stu-id="5ab87-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="5ab87-158">Параметры обратного чересстрочности</span><span class="sxs-lookup"><span data-stu-id="5ab87-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="5ab87-159">Описание обратного чересстрочностиа см. в разделе [Использование инверсии чересстрочности](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="5ab87-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="5ab87-160">Если присвоить режиму разчересстрочную развертку WM \_ DM \_ unчередованиing \_ инверсетелеЦине, можно указать шаблон чересстрочности первого входного кадра, вызвав метод [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="5ab87-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="5ab87-161">Параметр для использования — g \_ всзинитиалпаттернфоринверсетелеЦине.</span><span class="sxs-lookup"><span data-stu-id="5ab87-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="5ab87-162">Задайте для исходного шаблона одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5ab87-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="5ab87-163">Значение</span><span class="sxs-lookup"><span data-stu-id="5ab87-163">Value</span></span>                                              | <span data-ttu-id="5ab87-164">Описание</span><span class="sxs-lookup"><span data-stu-id="5ab87-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab87-165">\_приложение WM \_ DM \_ отключает \_ режим согласованности \_</span><span class="sxs-lookup"><span data-stu-id="5ab87-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="5ab87-166">Указывает, что входной носитель пропало через процесс чересстрочности, но кадры больше не находятся в прогнозируемом шаблоне.</span><span class="sxs-lookup"><span data-stu-id="5ab87-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="5ab87-167">Обычно это означает, что носитель был изменен после обработки чересстрочности.</span><span class="sxs-lookup"><span data-stu-id="5ab87-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="5ab87-168">При использовании этого параметра кодек попытается восстановить исходные кадры самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="5ab87-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="5ab87-169">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ — \_ AA \_ Top</span><span class="sxs-lookup"><span data-stu-id="5ab87-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="5ab87-170">Указывает, что верхнее поле рамки AA является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ab87-171">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ , — \_ BB \_ Top</span><span class="sxs-lookup"><span data-stu-id="5ab87-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="5ab87-172">Указывает, что верхнее поле рамки BB является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ab87-173">\_приложение WM \_ DM \_ \_ , первым кадром \_ в \_ картинке \_ , является \_ BC \_ Top</span><span class="sxs-lookup"><span data-stu-id="5ab87-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="5ab87-174">Указывает, что верхнее поле рамки BC является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ab87-175">\_приложение WM \_ DM \_ \_ , первым кадром \_ в \_ клипе \_ , находится на \_ компакт-диске \_</span><span class="sxs-lookup"><span data-stu-id="5ab87-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="5ab87-176">Указывает, что верхнее поле кадра компакт-диска является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ab87-177">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ — \_ DD \_ Top</span><span class="sxs-lookup"><span data-stu-id="5ab87-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="5ab87-178">Указывает, что верхнее поле рамки DD является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="5ab87-179">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ — \_ номер AA \_ снизу</span><span class="sxs-lookup"><span data-stu-id="5ab87-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="5ab87-180">Указывает, что нижнее поле рамки AA является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5ab87-181">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ , — \_ BB \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="5ab87-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="5ab87-182">Указывает, что нижнее поле рамки BB является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5ab87-183">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ , — \_ BC \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="5ab87-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="5ab87-184">Указывает, что нижнее поле рамки BC является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5ab87-185">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ клипе \_ , находится на \_ компакт-диске \_</span><span class="sxs-lookup"><span data-stu-id="5ab87-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="5ab87-186">Указывает, что нижнее поле кадра CD является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5ab87-187">\_приложение WM \_ DM \_ \_ , первый кадр \_ в \_ картинке \_ — \_ дд, \_ внизу</span><span class="sxs-lookup"><span data-stu-id="5ab87-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="5ab87-188">Указывает, что нижнее поле рамки DD является первым образцом.</span><span class="sxs-lookup"><span data-stu-id="5ab87-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="5ab87-189">См. также</span><span class="sxs-lookup"><span data-stu-id="5ab87-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab87-190">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="5ab87-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





