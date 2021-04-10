---
title: Настройка модуля записи WM ASF (КАСФ)
description: Настройка модуля записи WM ASF (КАСФ)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Пакет SDK для Windows Media Format, Настройка модуля записи WM ASF (КАСФ)
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, модуль записи WM ASF
- Windows Media Format SDK, КАСФ
- Расширенный формат систем (ASF), Настройка модуля записи WM ASF (КАСФ)
- ASF (Расширенный системный формат), Настройка модуля записи WM ASF (КАСФ)
- Расширенный формат систем (ASF), модуль записи WM ASF
- ASF (Расширенный системный формат), модуль записи WM ASF
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- DirectShow, Настройка модуля записи WM ASF (КАСФ)
- DirectShow, модуль записи WM ASF
- DirectShow, КАСФ
- Модуль записи WM ASF, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134382"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="5aff2-119">Настройка модуля записи WM ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="5aff2-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="5aff2-120">Когда фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) создан, он автоматически настраивается с помощью вмпрофиле \_ V80 \_ 256Video Profile в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5aff2-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="5aff2-121">Поскольку в этом профиле используются кодеки Windows Media Audio и Windows Media Video версии 8, рекомендуется создать пользовательский профиль, использующий кодеки Windows Media 9, а затем передать его указатель [**ивмпрофиле**](iwmprofile.md) в фильтр с помощью метода [**Иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5aff2-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="5aff2-122">Фильтр необходимо добавить в граф, прежде чем можно будет настроить фильтр, и его необходимо настроить перед подключением к вышестоящим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="5aff2-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="5aff2-123">Фильтр использует профиль для определения типа записываемого файла формата Windows Media, количества устанавливаемых ПИН-кодов входа и типов носителей, которые могут принимать эти сигналы.</span><span class="sxs-lookup"><span data-stu-id="5aff2-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="5aff2-124">Фильтр позволяет сбрасывать профили во время подключения входных контактов, если новый профиль не требует дополнительных входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="5aff2-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="5aff2-125">Например, если изменить профиль из одновходного звукового профиля на два входных аудио-и видеопрофиль, то только ПИН-код будет Реконнектедалл входные данные должны быть отметкой времени, а все входные контакты должны быть подключены, прежде чем фильтр можно будет запустить или приостановить.</span><span class="sxs-lookup"><span data-stu-id="5aff2-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="5aff2-126">Это означает, что если вы настроите фильтр с профилем, имеющим звуковой поток и поток видео, фильтр создаст звук и ПИН-код входного видео, и оба этих контакта должны быть подключены, прежде чем можно будет запустить фильтр.</span><span class="sxs-lookup"><span data-stu-id="5aff2-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="5aff2-127">Добавление модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="5aff2-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="5aff2-128">Вы можете настроить поток профиля для модулей обработки данных, например коды времени SMPTE до или после подключения фильтра, при условии, что выполняется следующий порядок операций:</span><span class="sxs-lookup"><span data-stu-id="5aff2-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="5aff2-129">Добавьте в поток одно или несколько расширений модулей данных с помощью [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="5aff2-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="5aff2-130">Вызовите [**вмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) , чтобы обновить профиль.</span><span class="sxs-lookup"><span data-stu-id="5aff2-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="5aff2-131">Вызовите [**иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) с обновленным объектом Profile.</span><span class="sxs-lookup"><span data-stu-id="5aff2-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="5aff2-132">Найдите ПИН-код входного видео и вызовите его метод [**иамвмбуфферпасс:: сетнотифи**](iamwmbufferpass-setnotify.md) , чтобы зарегистрировать определяемый приложением интерфейс [**иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) .</span><span class="sxs-lookup"><span data-stu-id="5aff2-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="5aff2-133">При запуске графа метод [**иамвмбуфферпасскаллбакк:: notify**](iamwmbufferpasscallback-notify.md) будет вызываться для каждого кадра, и вы сможете получить и задать свойства в образце с помощью его методов интерфейса [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="5aff2-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="5aff2-134">В некоторых сценариях с интенсивным использованием процессора, таких как инверсный чересстрочности, модуль записи WM ASF может потребовать больше буферов вывода, чем может поддерживать некоторые нисходящие фильтры.</span><span class="sxs-lookup"><span data-stu-id="5aff2-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="5aff2-135">Например, декодер DV не принимает более одного буфера для выходного ПИН-кода, и это справедливо для распаковки AVI в определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="5aff2-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="5aff2-136">При возникновении проблем при попытке подключения к этим фильтрам или, возможно, при запуске графа, может потребоваться написать промежуточный фильтр, который принимает любое количество буферов на выходном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="5aff2-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 