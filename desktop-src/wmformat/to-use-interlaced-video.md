---
title: Использование чередования видео
description: Использование чередования видео
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK, видео с чередованием
- Windows Media Format SDK, кодирование видео с чередованием
- Windows Media Format SDK, кодирование видео с чередованием
- Windows Media Format SDK, декодирование видео с чередованием
- Пакет SDK Windows Media Format, порядок полей
- Расширенный формат систем (ASF), видео с чередованием
- ASF (Расширенный системный формат), видео с чередованием
- Расширенный формат систем (ASF), кодирование видео с чередованием
- ASF (Расширенный системный формат), кодирование видео с чередованием
- Расширенный формат систем (ASF), кодирование видео с чередованием
- ASF (Расширенный системный формат), кодирование видео с чередованием
- Расширенный формат систем (ASF), декодирование видео с чередованием
- ASF (Расширенный системный формат), декодирование видео с чередованием
- Расширенный системный формат (ASF), порядок полей
- ASF (Расширенный системный формат), порядок полей
- чередование видео, сведения
- чередование видео, кодирование
- чередование видео, декодирование
- чередование видео, порядок полей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890248"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="13dfd-122">Использование чередования видео</span><span class="sxs-lookup"><span data-stu-id="13dfd-122">To Use Interlaced Video</span></span>

<span data-ttu-id="13dfd-123">Существует два основных типа кодирования видео: прогрессивные и чередующиеся.</span><span class="sxs-lookup"><span data-stu-id="13dfd-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="13dfd-124">В прогрессивной кодировке каждый кадр представляет собой закодированное представление одного кадра видео.</span><span class="sxs-lookup"><span data-stu-id="13dfd-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="13dfd-125">При шифровании с чередованием каждый кадр представляет собой закодированное представление всех четных строк пикселов в видео или всех нечетных строк.</span><span class="sxs-lookup"><span data-stu-id="13dfd-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="13dfd-126">Каждый чередующийся кадр называется *полем*, поэтому существуют четные поля и даже поля.</span><span class="sxs-lookup"><span data-stu-id="13dfd-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="13dfd-127">Чередующиеся экраны (например, телевизор) отображают поля по одному, чередование полей.</span><span class="sxs-lookup"><span data-stu-id="13dfd-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="13dfd-128">Последовательный экран отображает все кадры одновременно.</span><span class="sxs-lookup"><span data-stu-id="13dfd-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="13dfd-129">Кодек расширенного профиля Windows Media Video 9 обеспечивает поддержку сохранения чересстрочную развертки в сжатых потоках.</span><span class="sxs-lookup"><span data-stu-id="13dfd-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="13dfd-130">Когда следует использовать чередование видео</span><span class="sxs-lookup"><span data-stu-id="13dfd-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="13dfd-131">Кодирование видео с чередованием полезно только в том случае, если содержимое отображается на устройстве с чередованием.</span><span class="sxs-lookup"><span data-stu-id="13dfd-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="13dfd-132">Содержимое, предназначенное для просмотра на телевизоре (через набор или другое устройство), может потребоваться для чередования.</span><span class="sxs-lookup"><span data-stu-id="13dfd-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="13dfd-133">Содержимое, которое предназначено для просмотра исключительно на дисплее компьютера, не должно быть закодировано с чередованием.</span><span class="sxs-lookup"><span data-stu-id="13dfd-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="13dfd-134">Чтобы закодировать видео с чередованием в виде последовательного видео, необходимо настроить входные параметры.</span><span class="sxs-lookup"><span data-stu-id="13dfd-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="13dfd-135">Дополнительные сведения см. в статье о [деразвертке видео](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="13dfd-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="13dfd-136">Порядок полей</span><span class="sxs-lookup"><span data-stu-id="13dfd-136">Field Order</span></span>

<span data-ttu-id="13dfd-137">Большинство источников чередующихся видеороликов, таких как карты видеозаписи, доставляют образцы видео, включающие оба поля, которые чередуются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="13dfd-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="13dfd-138">Результат похож на полный кадр видео, за исключением того, что четные и четные линии немного сдвигаются по времени.</span><span class="sxs-lookup"><span data-stu-id="13dfd-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="13dfd-139">Не существует универсального стандарта, по которому поле в примере с чередованием видео происходит в первый раз.</span><span class="sxs-lookup"><span data-stu-id="13dfd-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="13dfd-140">Необходимо разрешить пользователям указывать порядок полей при передаче образцов с чередованием в приложение.</span><span class="sxs-lookup"><span data-stu-id="13dfd-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="13dfd-141">Кодирование видео с чередованием</span><span class="sxs-lookup"><span data-stu-id="13dfd-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="13dfd-142">Чтобы использовать чередование кодирования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="13dfd-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="13dfd-143">Настройте поток видео в профиле для использования расширения единиц обработки данных типа содержимого, вызвав метод [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="13dfd-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="13dfd-144">Пример GUID расширения для расширения типа содержимого — WM \_ сампликстенсионсгуид \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="13dfd-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="13dfd-145">Установите поток в профиле и настройте для модуля записи профиль в нормальном режиме.</span><span class="sxs-lookup"><span data-stu-id="13dfd-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="13dfd-146">Прежде чем передавать образцы с чередованием в модуль записи, вызовите метод [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , чтобы задать \_ для параметра g Всзинтерлацедкодинг input значение **true**.</span><span class="sxs-lookup"><span data-stu-id="13dfd-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="13dfd-147">Для каждого образца с чередованием, передаваемого в модуль записи, вызовите метод [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) , чтобы задать тип содержимого.</span><span class="sxs-lookup"><span data-stu-id="13dfd-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="13dfd-148">Значения типа содержимого являются комбинациями флагов, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="13dfd-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="13dfd-149">Flag</span><span class="sxs-lookup"><span data-stu-id="13dfd-149">Flag</span></span>                         | <span data-ttu-id="13dfd-150">Описание</span><span class="sxs-lookup"><span data-stu-id="13dfd-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13dfd-151">с \_ \_ чередованием WM CT</span><span class="sxs-lookup"><span data-stu-id="13dfd-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="13dfd-152">Всегда устанавливайте этот флаг при кодировании содержимого с чередованием.</span><span class="sxs-lookup"><span data-stu-id="13dfd-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="13dfd-153">Если этот флаг используется без установки флага порядка полей (первое поле WM \_ CT \_ \_ \_ First или WM \_ CT \_ Top \_ \_ ), кодек предполагает, что верхнее поле является первым.</span><span class="sxs-lookup"><span data-stu-id="13dfd-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="13dfd-154">Если кодек использует неправильный порядок полей, это не должно повлиять на качество изображения, однако эффективность кодирования будет нарушена.</span><span class="sxs-lookup"><span data-stu-id="13dfd-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="13dfd-155">\_ \_ \_ сначала следует поле WM CT снизу \_</span><span class="sxs-lookup"><span data-stu-id="13dfd-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="13dfd-156">В сочетании с \_ \_ флагом с чередованием WM CT этот флаг указывает на то, что нижнее поле (поле, начинающееся со второй строки в образце) сначала выполняется в первый раз.</span><span class="sxs-lookup"><span data-stu-id="13dfd-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="13dfd-157">\_ \_ первое поле, расположенное в верхней части WM CT \_ \_</span><span class="sxs-lookup"><span data-stu-id="13dfd-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="13dfd-158">В сочетании с \_ \_ флагом с чередованием WM CT этот флаг указывает, что верхнее поле (поле, начинающееся с первой строки в образце) будет выполняться первым по времени.</span><span class="sxs-lookup"><span data-stu-id="13dfd-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="13dfd-159">\_ \_ \_ первое поле повтора в WM CT \_</span><span class="sxs-lookup"><span data-stu-id="13dfd-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="13dfd-160">Указывает, что первое поле в образце должно повторяться при воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="13dfd-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="13dfd-161">Этот флаг используется для видео, созданного на основе пленки процессом чересстрочности. Если флаг порядка полей не установлен вместе с этим флагом, то верхнее поле считается первым в момент времени.</span><span class="sxs-lookup"><span data-stu-id="13dfd-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="13dfd-162">Если флаг с \_ \_ чередованием WM CT не установлен, предполагается, что образец содержит последовательный видеокадр.</span><span class="sxs-lookup"><span data-stu-id="13dfd-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="13dfd-163">Декодирование видео с чередованием</span><span class="sxs-lookup"><span data-stu-id="13dfd-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="13dfd-164">При декодировании с чередованием видео необходимо задать \_ для параметра g всзалловинтерлацедаутпут значение **true** с помощью метода [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="13dfd-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="13dfd-165">В противном случае кодек будет доставлять прогрессивные кадры.</span><span class="sxs-lookup"><span data-stu-id="13dfd-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="13dfd-166">Расширение единицы данных типа содержимого поддерживается в выходных образцах.</span><span class="sxs-lookup"><span data-stu-id="13dfd-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="13dfd-167">Необходимо передать ориентацию поля на устройство отрисовки, чтобы обеспечить правильное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="13dfd-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13dfd-168">См. также</span><span class="sxs-lookup"><span data-stu-id="13dfd-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13dfd-169">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="13dfd-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





