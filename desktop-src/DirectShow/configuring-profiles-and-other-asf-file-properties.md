---
description: Настройка профилей и других свойств ASF-файлов
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Настройка профилей и других свойств ASF-файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422997"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="22c23-103">Настройка профилей и других свойств ASF-файлов</span><span class="sxs-lookup"><span data-stu-id="22c23-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="22c23-104">Следующие элементы описывают выполнение различных задач, связанных с созданием файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="22c23-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="22c23-105">Некоторые из интерфейсов, упомянутых в этом разделе, описаны в документации пакета SDK для Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="22c23-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="22c23-106">Создание профиля</span><span class="sxs-lookup"><span data-stu-id="22c23-106">Creating a Profile</span></span>

<span data-ttu-id="22c23-107">Профили ASF подробно обсуждаются в пакете SDK формата Windows Media. по сути, они описывают атрибуты файла формата Windows Media, такие как скорость, число и тип потоков, а также качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="22c23-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="22c23-108">Фильтр использует профиль для определения типа записываемого файла формата Windows Media, количества входных контактов, которые он должен настроить, и типов носителей, которые они могут принимать.</span><span class="sxs-lookup"><span data-stu-id="22c23-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="22c23-109">Чтобы создать настраиваемый профиль, используйте пакет SDK для формата Windows Media, чтобы создать объект диспетчера профилей с помощью функции **вмкреатепрофилеманажер** .</span><span class="sxs-lookup"><span data-stu-id="22c23-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="22c23-110">Затем создайте профиль и передайте его в [модуль записи WM ASF](wm-asf-writer-filter.md) с помощью метода [**Иконфигасфвритер:: конфигурефилтерусингпрофиле**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) .</span><span class="sxs-lookup"><span data-stu-id="22c23-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="22c23-111">Это единственный способ настроить фильтр с помощью профиля, который использует кодеки Windows Media Audio и Video 9.</span><span class="sxs-lookup"><span data-stu-id="22c23-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="22c23-112">Системные профили для более ранних версий этих кодеков можно добавить с помощью метода [**иконфигасфвритер:: конфигурефилтерусингпрофилегуид**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .</span><span class="sxs-lookup"><span data-stu-id="22c23-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="22c23-113">Вы можете сбросить профиль, пока подключены входные сигналы фильтра, если новый профиль не требует дополнительных входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="22c23-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="22c23-114">Например, если изменить профиль из одновходного звукового профиля на два входных аудио-и видеопрофиль, будет повторно подключен только ПИН-код, а для видеопотока не будет создан новый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="22c23-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="22c23-115">Добавление метаданных</span><span class="sxs-lookup"><span data-stu-id="22c23-115">Adding Metadata</span></span>

<span data-ttu-id="22c23-116">Чтобы добавить метаданные в файл, запросите фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) для интерфейса **ивмхеадеринфо** .</span><span class="sxs-lookup"><span data-stu-id="22c23-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="22c23-117">После того как для фильтра был получен профиль, используйте методы интерфейса **ивмхеадеринфо** для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="22c23-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="22c23-118">Индексирование файла</span><span class="sxs-lookup"><span data-stu-id="22c23-118">Indexing a File</span></span>

<span data-ttu-id="22c23-119">Модуль записи WM ASF по умолчанию создает временные индексированные файлы.</span><span class="sxs-lookup"><span data-stu-id="22c23-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="22c23-120">Чтобы создать файл, индексируемый по фрейму, используйте метод [**иконфигасфвритер:: сетиндексмоде**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) , чтобы отключить все индексирование, а затем создайте файл.</span><span class="sxs-lookup"><span data-stu-id="22c23-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="22c23-121">По завершении используйте пакет SDK для формата Windows Media, чтобы создать для файла индекс на основе фрейма.</span><span class="sxs-lookup"><span data-stu-id="22c23-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="22c23-122">Кодировка Two-Pass</span><span class="sxs-lookup"><span data-stu-id="22c23-122">Two-Pass Encoding</span></span>

<span data-ttu-id="22c23-123">Двусторонняя кодировка поддерживается только в кодеках Windows Media версии 8 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="22c23-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="22c23-124">Переведите модуль записи WM ASF в режим предварительной обработки, вызвав [**IConfigAsfWriter2:: сетпарам**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) и указав \_ конфигасфвритер \_ param \_ в параметре *двпарам* , и **значение true** в параметре *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="22c23-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="22c23-125">Затем запустите граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="22c23-125">Then run the filter graph.</span></span> <span data-ttu-id="22c23-126">Когда выполняются все этапы предварительной обработки (обычно выполняется только один этап предварительной обработки), приложение получит событие [**\_ \_ завершения предварительной обработки**](ec-preprocess-complete.md) в фильтре.</span><span class="sxs-lookup"><span data-stu-id="22c23-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="22c23-127">При получении этого события используйте [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , чтобы сбросить указатель потока обратно на начало и снова запустить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="22c23-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="22c23-128">После последнего этапа (обычно второй проход) приложение получит событие [**EC \_ Complete**](ec-complete.md) , чтобы обозначить завершение процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="22c23-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="22c23-129">Если этап предварительной обработки был отменен до получения события **\_ предварительной обработки \_** , вызовите [**IConfigAsfWriter2:: ресетмултипассстате**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) , чтобы сбросить фильтр, прежде чем пытаться выполнить другой предварительный запуск.</span><span class="sxs-lookup"><span data-stu-id="22c23-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="22c23-130">\_ \_ \_ Если требуется полностью перевести фильтр из режима предварительной обработки в **значение false** , необходимо установить параметр многопрохода конфигасфвритер параметра.</span><span class="sxs-lookup"><span data-stu-id="22c23-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22c23-131">Ответственность за включение режима предварительной обработки на основе профиля, который будет использоваться для кодирования, несет приложение.</span><span class="sxs-lookup"><span data-stu-id="22c23-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="22c23-132">Для некоторых профилей требуется двусторонняя кодировка. Если вы попытаетесь закодировать файл с таким профилем и не установили \_ \_ параметр конфигасфвритер param of \_ Pass в **значение true**, будет получено сообщение об ошибке [**EC \_ усераборт**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="22c23-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="22c23-133">Дополнительные сведения см. в документации пакета Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="22c23-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="22c23-134">Получение и установка свойств буфера во время выполнения</span><span class="sxs-lookup"><span data-stu-id="22c23-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="22c23-135">В некоторых случаях, например, если требуется принудительно вставить ключевые кадры при записи файла, приложению может потребоваться получить или задать сведения о буфере Windows Media во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="22c23-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="22c23-136">Фильтры модуля записи [WM ASF](wm-asf-reader-filter.md) и [WM ASF](wm-asf-writer-filter.md) поддерживают механизм обратного вызова, который позволяет приложению получать доступ к интерфейсу **INSSBuffer3** в каждом отдельном буфере мультимедиа во время чтения или записи файлов.</span><span class="sxs-lookup"><span data-stu-id="22c23-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="22c23-137">Приложения могут использовать этот интерфейс для обозначения конкретных выборок в качестве ключевых кадров, установки кодов времени SMPTE, указания параметров чересстрочную развертки или добавления любых типов частных данных в поток.</span><span class="sxs-lookup"><span data-stu-id="22c23-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="22c23-138">Используйте интерфейс [**иамвмбуфферпасс**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) для регистрации обратных вызовов из ПИН-кода, обрабатывающего поток видео.</span><span class="sxs-lookup"><span data-stu-id="22c23-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="22c23-139">ПИН-код будет вызывать метод [**иамвмбуфферпасскаллбакк:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) для каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="22c23-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="22c23-140">Неквадратные Пиксели</span><span class="sxs-lookup"><span data-stu-id="22c23-140">Non-Square Pixels</span></span>

<span data-ttu-id="22c23-141">Модуль записи WM ASF подключается к вышестоящему фильтру, например к декодеру DV, который выводит сведения о соотношении пропорций в пикселях.</span><span class="sxs-lookup"><span data-stu-id="22c23-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="22c23-142">Модуль записи WM ASF записывает эти сведения в виде расширений модулей данных для каждого образца в файле.</span><span class="sxs-lookup"><span data-stu-id="22c23-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="22c23-143">Когда читатель WM ASF встречает сведения о соотношении пропорций в заголовке файла или в расширениях модулей данных для образцов, он будет предлагать формат [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) в качестве первого варианта для своего выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="22c23-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="22c23-144">Элементы **двпиктаспектратиокс** и **двпиктаспектратиой** структуры, описывающие пропорции видео, будут правильно скорректированы с учетом пропорций в пикселях.</span><span class="sxs-lookup"><span data-stu-id="22c23-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="22c23-145">Поддержание формата с чередованием</span><span class="sxs-lookup"><span data-stu-id="22c23-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="22c23-146">При записи чередования видео с телевизора или с цифровой камеры может потребоваться сохранить исходное видео как независимые поля, если предполагается, что закодированный файл воспроизводится на телевизоре или другом с чередованием дисплее.</span><span class="sxs-lookup"><span data-stu-id="22c23-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="22c23-147">(Мониторы компьютеров — это прогрессивные проверки устройств.) Если вы развернете видео, а затем переустановите его для воспроизведения на телевизоре, будет вызвана часть потери данных.</span><span class="sxs-lookup"><span data-stu-id="22c23-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="22c23-148">В файле ASF сведения о чересстрочную развертке хранятся в виде модулей обработки данных, которые приложение применяет к каждому примеру с помощью метода [**иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) , описанного выше.</span><span class="sxs-lookup"><span data-stu-id="22c23-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="22c23-149">Чтобы закодировать файл, сохраняющий исходные параметры развертки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="22c23-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="22c23-150">Реализуйте класс, который поддерживает **иамвмбуфферпасскаллбакк** , и напишите функцию Notify, которая задает флаги чересстрочную развертки для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="22c23-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="22c23-151">Эта функция будет вызываться модулем записи WM ASF до обработки каждого примера.</span><span class="sxs-lookup"><span data-stu-id="22c23-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="22c23-152">Перед передачей профиля в фильтр задайте расширения единиц обработки данных в профиле.</span><span class="sxs-lookup"><span data-stu-id="22c23-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="22c23-153">После настройки фильтра с помощью профиля получите интерфейс **IWMWriterAdvanced2** из модуля записи WM ASF и вызовите метод **сетинпутсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="22c23-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
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

    

## <a name="related-topics"></a><span data-ttu-id="22c23-154">См. также</span><span class="sxs-lookup"><span data-stu-id="22c23-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c23-155">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="22c23-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



