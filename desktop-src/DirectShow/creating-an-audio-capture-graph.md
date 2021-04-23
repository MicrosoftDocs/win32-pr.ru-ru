---
description: Создание графика записи звука
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Создание графика записи звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662056"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="ac41b-103">Создание графика записи звука</span><span class="sxs-lookup"><span data-stu-id="ac41b-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="ac41b-104">Первым шагом для приложения аудиозаписи является создание графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ac41b-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="ac41b-105">Конфигурация графа зависит от типа файла, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="ac41b-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="ac41b-106">AVI-файл только для звука: фильтр записи звука для фильтра [мультиплексора AVI](avi-mux-filter.md) и фильтр AVI-мультиплексора для фильтра [записи файлов](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ac41b-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="ac41b-107">WAV файл: фильтр записи звука в фильтр [Вавдест Filter](wavdest-filter-sample.md) для фильтра записи файлов</span><span class="sxs-lookup"><span data-stu-id="ac41b-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="ac41b-108">Файл Windows Media Audio (WMA): фильтр записи звука для фильтра [модуля записи WM ASF](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ac41b-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="ac41b-109">Фильтр Вавдест предоставляется в виде примера пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="ac41b-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="ac41b-110">Чтобы использовать его, необходимо создать и зарегистрировать фильтр.</span><span class="sxs-lookup"><span data-stu-id="ac41b-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="ac41b-111">Чтобы использовать фильтр модуля записи ASF, необходимо установить Windows Media SDK и получить программный ключ для разблокировки фильтра.</span><span class="sxs-lookup"><span data-stu-id="ac41b-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="ac41b-112">Дополнительные сведения см. [в разделе Использование Windows Media в DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ac41b-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="ac41b-113">Можно построить граф фильтра с помощью объекта [построителя графа записи](capture-graph-builder.md) или построить граф вручную. Это значит, что приложение программным образом добавляет и подключает каждый фильтр.</span><span class="sxs-lookup"><span data-stu-id="ac41b-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="ac41b-114">В этой статье описывается ручной подход.</span><span class="sxs-lookup"><span data-stu-id="ac41b-114">This article describes the manual approach.</span></span> <span data-ttu-id="ac41b-115">Дополнительные сведения об использовании построителя графа записи см. в разделе [Capture видео](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="ac41b-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="ac41b-116">Большая часть информации в этой статье относится к графикам только для звука.</span><span class="sxs-lookup"><span data-stu-id="ac41b-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="ac41b-117">Добавление устройства записи звука</span><span class="sxs-lookup"><span data-stu-id="ac41b-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="ac41b-118">Так как фильтр записи звука взаимодействует с конкретным устройством, вы не можете просто вызвать **CoCreateInstance** для создания фильтра.</span><span class="sxs-lookup"><span data-stu-id="ac41b-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="ac41b-119">Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md) для перечисления всех устройств в категории "источники звукового захвата", которая определяется идентификатором класса CLSID \_ аудиоинпутдевицекатегори.</span><span class="sxs-lookup"><span data-stu-id="ac41b-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="ac41b-120">Перечислитель системных устройств возвращает список моникеров для устройств. Понятное имя каждого моникера соответствует имени устройства.</span><span class="sxs-lookup"><span data-stu-id="ac41b-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="ac41b-121">Выберите одно из возвращенных моникеров и используйте его для создания экземпляра фильтра записи звука для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="ac41b-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="ac41b-122">Добавьте фильтр к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="ac41b-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="ac41b-123">Предпочитаемое устройство записи звука отображается первым в списке моникеров.</span><span class="sxs-lookup"><span data-stu-id="ac41b-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="ac41b-124">(Пользователь выбирает предпочитаемое устройство, щелкая звуки и мультимедиа в панели управления.)</span><span class="sxs-lookup"><span data-stu-id="ac41b-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="ac41b-125">Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="ac41b-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="ac41b-126">Чтобы указать, какие входные данные нужно записать, получите интерфейс [**иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) из фильтра записи звука и вызовите метод Where **\_ Enable** , чтобы указать входные данные.</span><span class="sxs-lookup"><span data-stu-id="ac41b-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="ac41b-127">Однако одним из ограничений этого метода является то, что разные аппаратные устройства могут использовать разные строки для обнаружения входных данных.</span><span class="sxs-lookup"><span data-stu-id="ac41b-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="ac41b-128">Например, одна карта может использовать "микрофон" для распознавания входных данных с микрофона, а другая плата может использовать "Mic".</span><span class="sxs-lookup"><span data-stu-id="ac41b-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="ac41b-129">Чтобы определить идентификатор строки для заданного входа, используйте функции мультимедиа Windows [**вавеаутопен**](/previous-versions//dd743866(v=vs.85)), [**миксеропен**](/previous-versions//dd757308(v=vs.85))и [**миксержетлинеинфо**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac41b-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="ac41b-130">Дополнительные сведения см. в разделе [запросы устройства микшера](/windows/desktop/Multimedia/mixer-device-queries) MSDN.</span><span class="sxs-lookup"><span data-stu-id="ac41b-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="ac41b-131">Добавление мультиплексора и модуля записи файлов</span><span class="sxs-lookup"><span data-stu-id="ac41b-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="ac41b-132">График записи звука должен содержать мультиплексор и модуль записи файлов.</span><span class="sxs-lookup"><span data-stu-id="ac41b-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="ac41b-133">*Мультиплексор* — это фильтр, объединяющий один или несколько потоков в один поток с определенным форматом.</span><span class="sxs-lookup"><span data-stu-id="ac41b-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="ac41b-134">Например, фильтр мультиплексора AVI сочетает аудио и видеопотоки с чередованием потока AVI.</span><span class="sxs-lookup"><span data-stu-id="ac41b-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="ac41b-135">Для записи звука обычно используется только один аудиопоток, но звуковые данные по-прежнему должны быть упакованы в формат, который можно сохранить на диске, что требует мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="ac41b-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="ac41b-136">Выбор мультиплексора зависит от целевого формата:</span><span class="sxs-lookup"><span data-stu-id="ac41b-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="ac41b-137">AVI: мультиплексор AVI</span><span class="sxs-lookup"><span data-stu-id="ac41b-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="ac41b-138">WAV: Вавдест</span><span class="sxs-lookup"><span data-stu-id="ac41b-138">WAV: WavDest</span></span>
-   <span data-ttu-id="ac41b-139">WMA: модуль записи ASF</span><span class="sxs-lookup"><span data-stu-id="ac41b-139">WMA: ASF Writer</span></span>

<span data-ttu-id="ac41b-140">*Модуль записи файлов* — это фильтр, записывающий входящие данные в файл.</span><span class="sxs-lookup"><span data-stu-id="ac41b-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="ac41b-141">Для файлов AVI или WAV используйте [фильтр записи файлов](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ac41b-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="ac41b-142">Для файлов WMA модуль записи ASF выступает в качестве мультиплексора и модуля записи файлов.</span><span class="sxs-lookup"><span data-stu-id="ac41b-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="ac41b-143">После создания фильтров и добавления их к графу Подключите выходную закрепление фильтра записи звука к входному ПИН-коду мультиплексора и подключите выходный ПИН-код мультиплексора к входному ПИН-коду модуля записи фильтра (предполагая, что они являются отдельными фильтрами).</span><span class="sxs-lookup"><span data-stu-id="ac41b-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="ac41b-144">Чтобы указать имя файла, запросите средство записи файлов для интерфейса [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) и вызовите метод [**Ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .</span><span class="sxs-lookup"><span data-stu-id="ac41b-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="ac41b-145">Пример кода</span><span class="sxs-lookup"><span data-stu-id="ac41b-145">Example Code</span></span>

<span data-ttu-id="ac41b-146">В следующем примере показано, как создать график записи звука с помощью фильтра Вавдест.</span><span class="sxs-lookup"><span data-stu-id="ac41b-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="ac41b-147">Те же принципы применяются для других типов файлов.</span><span class="sxs-lookup"><span data-stu-id="ac41b-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="ac41b-148">В этом примере используется `AddFilterByCLSID` функция, описанная в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md), и `ConnectFilters` функция, описанная в разделе [Подключение двух фильтров](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ac41b-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="ac41b-149">Ни один из них не является API DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ac41b-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac41b-150">См. также</span><span class="sxs-lookup"><span data-stu-id="ac41b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac41b-151">Запись звука</span><span class="sxs-lookup"><span data-stu-id="ac41b-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
