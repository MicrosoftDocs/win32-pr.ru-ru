---
title: Настройка профилей и других свойств файлов (КАСФ)
description: Настройка профилей и других свойств файлов (КАСФ)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, Настройка профилей (КАСФ)
- Windows Media Format SDK, Настройка свойств файлов (КАСФ)
- Windows Media Format SDK, метаданные (КАСФ)
- Расширенный системный формат (ASF), Настройка профилей (КАСФ)
- ASF (Расширенный системный формат), Настройка профилей (КАСФ)
- Расширенный системный формат (ASF), Настройка свойств файлов (КАСФ)
- ASF (Расширенный системный формат), Настройка свойств файлов (КАСФ)
- Расширенный системный формат (ASF), метаданные (КАСФ)
- ASF (Расширенный системный формат), метаданные (КАСФ)
- Windows Media Format SDK, КАСФ
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- метаданные, КАСФ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488032"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="dff99-116">Настройка профилей и других свойств файлов (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="dff99-117">Следующие элементы описывают выполнение различных задач, связанных с созданием файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="dff99-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="dff99-118">Создание профиля (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="dff99-119">Чтобы создать настраиваемый профиль, используйте пакет SDK для формата Windows Media, чтобы создать объект диспетчера профилей с помощью функции [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="dff99-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="dff99-120">Затем создайте профиль и передайте его в [модуль записи WM ASF](wm-asf-writer-filter.md) с помощью метода [**Иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="dff99-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="dff99-121">Это единственный способ настроить фильтр с помощью профиля, который использует кодеки Windows Media Audio и Video 9.</span><span class="sxs-lookup"><span data-stu-id="dff99-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="dff99-122">Системные профили для более ранних версий этих кодеков можно добавить с помощью метода [**иконфигасфвритер:: конфигурефилтерусингпрофилегуид**](iconfigasfwriter-configurefilterusingprofileguid.md) .</span><span class="sxs-lookup"><span data-stu-id="dff99-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="dff99-123">Добавление метаданных (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="dff99-124">Чтобы добавить метаданные в файл, вызовите **QueryInterface** из интерфейса **Ибасефилтер** в [модуле записи WM ASF](wm-asf-writer-filter.md) , чтобы получить интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="dff99-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="dff99-125">После того как для фильтра был получен профиль, используйте методы интерфейса **ивмхеадеринфо** для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="dff99-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="dff99-126">Индексирование файла (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="dff99-127">Модуль записи WM ASF по умолчанию создает временные индексированные файлы.</span><span class="sxs-lookup"><span data-stu-id="dff99-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="dff99-128">Чтобы создать файл, индексируемый по фрейму, используйте метод [**иконфигасфвритер:: сетиндексмоде**](iconfigasfwriter-setindexmode.md) , чтобы отключить все индексирование, а затем создайте файл.</span><span class="sxs-lookup"><span data-stu-id="dff99-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="dff99-129">По завершении используйте пакет SDK для формата Windows Media, чтобы создать для файла индекс на основе фрейма.</span><span class="sxs-lookup"><span data-stu-id="dff99-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="dff99-130">Выполнение Two-Pass кодирования (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="dff99-131">Двусторонняя кодировка поддерживается только в кодеках Windows Media версии 8 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="dff99-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="dff99-132">Переведите модуль записи WM ASF в режим предварительной обработки, вызвав [**IConfigAsfWriter2:: сетпарам**](iconfigasfwriter2-setparam.md) и указав \_ конфигасфвритер \_ param \_ в параметре *двпарам* , и **значение true** в параметре *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="dff99-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="dff99-133">Затем запустите граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="dff99-133">Then run the filter graph.</span></span> <span data-ttu-id="dff99-134">Когда выполняются все этапы предварительной обработки (обычно выполняется только один этап предварительной обработки), приложение получит событие **\_ \_ завершения предварительной обработки** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="dff99-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="dff99-135">При получении этого события используйте **имедиасикинг:: сетпоситионс** , чтобы сбросить указатель потока обратно на начало и снова запустить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="dff99-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="dff99-136">После последнего этапа (обычно второй проход) приложение получит событие **EC \_ Complete** , чтобы обозначить завершение процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="dff99-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="dff99-137">Если этап предварительной обработки был отменен до получения события **\_ предварительной обработки \_** , вызовите [**IConfigAsfWriter2:: ресетмултипассстате**](iconfigasfwriter2-resetmultipassstate.md) , чтобы сбросить фильтр, прежде чем пытаться выполнить другой предварительный запуск.</span><span class="sxs-lookup"><span data-stu-id="dff99-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="dff99-138">Вызов **иконфигасфвритер:: сетпарам**(AM \_ Конфигасфвритер \_ param, false) требуется только в том \_ случае , если нужно полностью перевести фильтр из режима предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="dff99-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dff99-139">Ответственность за включение режима предварительной обработки в зависимости от профиля, который будет использоваться для кодирования, несет приложение.</span><span class="sxs-lookup"><span data-stu-id="dff99-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="dff99-140">Для некоторых профилей требуется двусторонняя кодировка. Если вы попытаетесь закодировать файл с таким профилем и не установили \_ \_ параметр конфигасфвритер param of \_ Pass в **значение true**, \_ будет получено сообщение об ошибке EC усераборт.</span><span class="sxs-lookup"><span data-stu-id="dff99-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="dff99-141">Дополнительные сведения о том, как определить, требуется ли в данном профиле кодирование с двумя проходами, см. в разделе [использование Two-Pass кодирования](using-two-pass-encoding.md) или [запись потоков переменной скорости](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="dff99-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="dff99-142">Получение и установка свойств буфера во время выполнения (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="dff99-143">В некоторых случаях, например, если требуется принудительно вставить ключевые кадры при записи файла, приложению может потребоваться получить или задать сведения о буфере Windows Media во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="dff99-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="dff99-144">Фильтры модуля записи [WM ASF](wm-asf-reader-filter.md) и [WM ASF](wm-asf-writer-filter.md) поддерживают механизм обратного вызова, который позволяет приложению получать доступ к интерфейсу [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) в каждом отдельном буфере мультимедиа во время чтения или записи файлов.</span><span class="sxs-lookup"><span data-stu-id="dff99-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="dff99-145">Приложения могут использовать этот интерфейс для обозначения конкретных выборок в качестве ключевых кадров, или [*клеанпоинтс*](wmformat-glossary.md), для задания кодов времени SMPTE, для указания параметров чересстрочную развертки или добавления любых типов частных данных в поток.</span><span class="sxs-lookup"><span data-stu-id="dff99-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="dff99-146">Используйте интерфейс [**иамвмбуфферпасс**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) для регистрации обратных вызовов из ПИН-кода, обрабатывающего поток видео.</span><span class="sxs-lookup"><span data-stu-id="dff99-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="dff99-147">Когда ПИН-код вызывает метод [**иамвмбуфферпасскаллбакк:: notify**](iamwmbufferpasscallback-notify.md) , проверьте отметки времени в буфере и при необходимости вызовите [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) , чтобы задать для свойства **WM \_ Сампликстенсионгуид \_ аутпутклеанпоинт** в буфере **значение true**.</span><span class="sxs-lookup"><span data-stu-id="dff99-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="dff99-148">Поддержка неквадратных пикселей (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="dff99-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="dff99-149">Модуль записи WM ASF подключается к вышестоящему фильтру, например к декодеру DV, который выводит сведения о соотношении пропорций в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dff99-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="dff99-150">Модуль записи WM ASF записывает эти сведения в виде расширений модулей данных для каждого образца в файле.</span><span class="sxs-lookup"><span data-stu-id="dff99-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="dff99-151">Когда модуль чтения WM ASF встречает сведения о соотношении пропорций в заголовке файла или в расширениях модулей данных для образцов, он будет предлагать тип носителя **VIDEOINFOHEADER2** в качестве первого варианта для своего выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="dff99-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="dff99-152">Элементы **двпиктаспектратиокс** и **двпиктаспектратиой** структуры, описывающие пропорции видео, будут правильно скорректированы с учетом пропорций в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dff99-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="dff99-153">Поддержание формата с чередованием</span><span class="sxs-lookup"><span data-stu-id="dff99-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="dff99-154">При записи чередования видео с телевизора или с цифровой камеры может потребоваться сохранить исходное видео как независимые поля, если предполагается, что закодированный файл воспроизводится на телевизоре или другом с чередованием дисплее.</span><span class="sxs-lookup"><span data-stu-id="dff99-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="dff99-155">(Мониторы компьютеров — это прогрессивные проверки устройств.) Если вы развернете видео, а затем переустановите его для воспроизведения на телевизоре, будет вызвана часть потери данных.</span><span class="sxs-lookup"><span data-stu-id="dff99-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="dff99-156">В файле ASF сведения о чересстрочную развертке хранятся в виде модулей обработки данных, которые приложение применяет к каждому примеру с помощью метода **иамвмбуфферпасскаллбакк** , описанного выше.</span><span class="sxs-lookup"><span data-stu-id="dff99-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="dff99-157">Чтобы закодировать файл, сохраняющий исходные параметры развертки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dff99-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="dff99-158">Реализуйте класс, который поддерживает **иамвмбуфферпасскаллбакк** , и напишите функцию Notify, которая задает флаги чересстрочную развертки для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="dff99-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="dff99-159">Эта функция будет вызываться модулем записи WM ASF до обработки каждого примера.</span><span class="sxs-lookup"><span data-stu-id="dff99-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="dff99-160">Перед передачей профиля в фильтр задайте расширения единиц обработки данных в профиле.</span><span class="sxs-lookup"><span data-stu-id="dff99-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="dff99-161">После настройки фильтра с помощью профиля получите интерфейс **IWMWriterAdvanced2** из модуля записи WM ASF и вызовите метод **сетинпутсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="dff99-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
CComPtr<IServiceProvider> pProvider;
  CComPtr<IWMWriterAdvanced2> pWMWA2;
  hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                         (void**)&pProvider);
  if (SUCCEEDED(hr))
  {
      hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
                    IID_IWMWriterAdvanced2,
                    (void**)&pWMWA2);
  }
  BOOL pValue = TRUE;
 // Set the first parameter to your actual input number.
 hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
              WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
            
```



 

 