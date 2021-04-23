---
title: Запись потоков с неквадратными пикселями
description: Запись потоков с неквадратными пикселями
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, написание видеопотоков
- Windows Media Format SDK, потоки видео
- Пакет SDK для формата Windows Media, а не квадратные Пиксели
- Windows Media Format SDK, Пиксели (не квадратные)
- Расширенный системный формат (ASF), написание видеопотоков
- ASF (Расширенный системный формат), написание видеопотоков
- Расширенный системный формат (ASF), видеопотоки
- ASF (Расширенный системный формат), видеопотоки
- Расширенный формат систем (ASF), а не квадратные Пиксели
- ASF (Расширенный системный формат), неквадратные Пиксели
- Расширенный формат систем (ASF), пикселей (не квадратный)
- ASF (Расширенный системный формат), Пиксели (не квадратный)
- Написание видеопотоков
- видеопотоки, запись
- видеопотоки, не квадратные Пиксели
- неквадратные Пиксели
- Пиксели (не квадратные)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069561"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="7f461-120">Запись потоков с неквадратными пикселями</span><span class="sxs-lookup"><span data-stu-id="7f461-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="7f461-121">Существует два способа создания потоков видео с неквадратными пикселями, которые будут правильно отображаться в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f461-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="7f461-122">Первый способ заключается в установке атрибутов уровня потока в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="7f461-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="7f461-123">Второй способ включает добавление расширения единицы данных в поток в профиле, а затем задание значения для него в каждом написанном образце.</span><span class="sxs-lookup"><span data-stu-id="7f461-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="7f461-124">Использование атрибутов заголовка уровня потока для установки пропорций в пикселях</span><span class="sxs-lookup"><span data-stu-id="7f461-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="7f461-125">Настройте объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="7f461-125">Set up the writer object.</span></span> <span data-ttu-id="7f461-126">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="7f461-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="7f461-127">Создайте или загрузите профиль с одним или несколькими потоками видео.</span><span class="sxs-lookup"><span data-stu-id="7f461-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="7f461-128">Дополнительные сведения см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7f461-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="7f461-129">Вызовите [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="7f461-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="7f461-130">(Всегда вызывайте этот метод перед установкой атрибутов заголовка.)</span><span class="sxs-lookup"><span data-stu-id="7f461-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="7f461-131">Вызовите **QueryInterface** , чтобы получить интерфейс [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) и дважды вызвать [**аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) , чтобы добавить [**аспектратиокс**](aspectratiox.md) и [**аспектратиой**](aspectratioy.md) в качестве атрибутов уровня потока видеопотока.</span><span class="sxs-lookup"><span data-stu-id="7f461-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="7f461-132">Эти атрибуты являются значениями **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7f461-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="7f461-133">Запишите файл.</span><span class="sxs-lookup"><span data-stu-id="7f461-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="7f461-134">Использование модулей обработки данных для установки пропорций в пикселях</span><span class="sxs-lookup"><span data-stu-id="7f461-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="7f461-135">**Перед записью:**</span><span class="sxs-lookup"><span data-stu-id="7f461-135">**Before writing:**</span></span>

1.  <span data-ttu-id="7f461-136">Настройте объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="7f461-136">Set up the writer object.</span></span> <span data-ttu-id="7f461-137">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="7f461-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="7f461-138">Создайте или загрузите профиль с одним или несколькими потоками видео.</span><span class="sxs-lookup"><span data-stu-id="7f461-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="7f461-139">Дополнительные сведения см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7f461-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="7f461-140">Для каждого потока (любого типа мультимедиа) в профиле вызовите [**ивмстреамконфиг:: сетстреамнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) , чтобы указать уникальное имя по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="7f461-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="7f461-141">Не присваивайте двум потокам одно и то же имя.</span><span class="sxs-lookup"><span data-stu-id="7f461-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="7f461-142">Используйте [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) в потоке видео, чтобы добавить расширение единицы данных для пропорций в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7f461-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="7f461-143">Вызовите [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="7f461-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="7f461-144">Запишите файл.</span><span class="sxs-lookup"><span data-stu-id="7f461-144">Write the file.</span></span>

<span data-ttu-id="7f461-145">**При записи:**</span><span class="sxs-lookup"><span data-stu-id="7f461-145">**While writing:**</span></span>

-   <span data-ttu-id="7f461-146">Для каждого образца вызовите [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) и укажите свойство WM \_ сампликстенсионгуид \_ пикселаспектратио вместе с правильным значением.</span><span class="sxs-lookup"><span data-stu-id="7f461-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="7f461-147">Значения пропорций записываются как два сцепленных двузначного значения.</span><span class="sxs-lookup"><span data-stu-id="7f461-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="7f461-148">Например, 16:9 записывается как 1609 или 0x0649.</span><span class="sxs-lookup"><span data-stu-id="7f461-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="7f461-149">Это всегда является 2-байтовым значением.</span><span class="sxs-lookup"><span data-stu-id="7f461-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f461-150">См. также</span><span class="sxs-lookup"><span data-stu-id="7f461-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f461-151">**Чтение и запись видеопотоков с неквадратными пикселями**</span><span class="sxs-lookup"><span data-stu-id="7f461-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




