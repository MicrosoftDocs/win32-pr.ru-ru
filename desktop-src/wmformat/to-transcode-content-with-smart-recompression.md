---
title: Перекодировать содержимое с помощью интеллектуального повторного сжатия
description: Перекодировать содержимое с помощью интеллектуального повторного сжатия
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK, перекодирование содержимого
- Windows Media Format SDK, интеллектуальное повторное сжатие
- Windows Media Format SDK, повторное сжатие
- Windows Media Format SDK, аудиокодеки Windows Media
- Расширенный системный формат (ASF), перекодирование содержимого
- ASF (Расширенный системный формат), перекодирование содержимого
- Расширенный системный формат (ASF), интеллектуальное повторное сжатие
- ASF (Расширенный системный формат), интеллектуальное повторное сжатие
- Расширенный формат систем (ASF), повторное сжатие
- ASF (Расширенный системный формат), повторное сжатие
- Расширенный системный формат (ASF), аудиокодеки Windows Media
- ASF (Расширенный системный формат), аудиокодеки Windows Media
- Перекодирование содержимого
- интеллектуальное повторное сжатие
- повторное сжатие
- Аудиокодеки Windows Media, перекодирование содержимого
- кодеки, аудиокодеки Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336351"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="966bb-120">Перекодировать содержимое с помощью интеллектуального повторного сжатия</span><span class="sxs-lookup"><span data-stu-id="966bb-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="966bb-121">Вы можете перекодировать содержимое из одной битовой скорости в другую с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="966bb-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="966bb-122">Как правило, это подразумевает простое декодирование содержимого и его повторное кодирование до нужной скорости.</span><span class="sxs-lookup"><span data-stu-id="966bb-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="966bb-123">Кодек Windows Media Audio 9 поддерживает интеллектуальное повторное сжатие, которое позволяет перекодировать, что достигает лучшего качества по сравнению с нормальным.</span><span class="sxs-lookup"><span data-stu-id="966bb-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="966bb-124">Для интеллектуального повторного сжатия исходный аудиопоток должен быть закодирован с помощью аудиокодека Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="966bb-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="966bb-125">Поддерживаются все версии кодеков, но специализированные аудиокодеки (Windows Media Audio 9 Professional и Windows Media Audio 9 Voice) не являются.</span><span class="sxs-lookup"><span data-stu-id="966bb-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="966bb-126">Если исходное аудио было закодировано с помощью кодека Windows Media Audio 9 без потерь, нет необходимости использовать интеллектуальное повторное сжатие, так как в исходной кодировке нет потерянных данных.</span><span class="sxs-lookup"><span data-stu-id="966bb-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="966bb-127">Чтобы использовать интеллектуальное повторное сжатие, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="966bb-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="966bb-128">Настройте объект Reader с помощью исходного файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="966bb-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="966bb-129">Дополнительные сведения см. в разделе [чтение файлов ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="966bb-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="966bb-130">Настройте объект модуля записи, который будет использоваться для перекодирования файла.</span><span class="sxs-lookup"><span data-stu-id="966bb-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="966bb-131">Задайте имя файла для нового файла.</span><span class="sxs-lookup"><span data-stu-id="966bb-131">Set the file name for the new file.</span></span> <span data-ttu-id="966bb-132">Выберите профиль, который будет использоваться для нового файла.</span><span class="sxs-lookup"><span data-stu-id="966bb-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="966bb-133">Задайте выбранный профиль в объекте модуля записи.</span><span class="sxs-lookup"><span data-stu-id="966bb-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="966bb-134">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="966bb-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="966bb-135">Получите указатель на интерфейс [**ивмпрофиле**](iwmprofile.md) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="966bb-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="966bb-136">Извлеките интерфейс [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) для потока аудиопотока, который необходимо перекодировать, вызвав [**Ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="966bb-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="966bb-137">Получите интерфейс [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) для объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="966bb-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="966bb-138">Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для потока, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="966bb-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="966bb-139">Получение размера структуры при первом вызове и выделение памяти для буфера, передаваемого во второй вызов.</span><span class="sxs-lookup"><span data-stu-id="966bb-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="966bb-140">Получите указатель на интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входных данных в средстве записи, вызвав [**Ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="966bb-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="966bb-141">Получите интерфейс [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) для входного объекта свойств носителя, вызвав **Ивминпутмедиапропс:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="966bb-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="966bb-142">Чтобы задать свойство g всзоригиналвавеформат, используйте метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) \_ .</span><span class="sxs-lookup"><span data-stu-id="966bb-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="966bb-143">Используйте структуру **вавеформатекс** , полученную на шаге 6, в качестве значения свойства.</span><span class="sxs-lookup"><span data-stu-id="966bb-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="966bb-144">Включите изменения, внесенные в свойства входного носителя, вызвав [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) и передав ему указатель на интерфейс **ивминпутмедиапропс** .</span><span class="sxs-lookup"><span data-stu-id="966bb-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="966bb-145">Начните считывать образцы из исходного файла и передавайте их в модуль записи с помощью вызовов [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="966bb-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="966bb-146">См. также</span><span class="sxs-lookup"><span data-stu-id="966bb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="966bb-147">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="966bb-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="966bb-148">**Интерфейс Ивминпутмедиапропс**</span><span class="sxs-lookup"><span data-stu-id="966bb-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="966bb-149">**Интерфейс Ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="966bb-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="966bb-150">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="966bb-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="966bb-151">**Интерфейс Ивмпропертиваулт**</span><span class="sxs-lookup"><span data-stu-id="966bb-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="966bb-152">**Интерфейс Ивмстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="966bb-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




