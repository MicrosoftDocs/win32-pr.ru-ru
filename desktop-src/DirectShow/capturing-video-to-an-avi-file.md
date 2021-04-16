---
description: Запись видео в файл AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Запись видео в файл AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104571214"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="f1d89-103">Запись видео в файл AVI</span><span class="sxs-lookup"><span data-stu-id="f1d89-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="f1d89-104">На следующем рисунке показана самая простая диаграмма для записи видео в файл AVI.</span><span class="sxs-lookup"><span data-stu-id="f1d89-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![Граф записи видео AVI](images/vidcap02.png)

<span data-ttu-id="f1d89-106">Фильтр [мультиплексора AVI](avi-mux-filter.md) принимает видеопоток из ПИН-кода захвата и упаковывает его в поток AVI.</span><span class="sxs-lookup"><span data-stu-id="f1d89-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="f1d89-107">Кроме того, аудиопоток может быть подключен к фильтру мультиплексора AVI. в этом случае мультиплексор будет чередовать два потока.</span><span class="sxs-lookup"><span data-stu-id="f1d89-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="f1d89-108">Фильтр [записи файлов](file-writer-filter.md) записывает поток AVI на диск.</span><span class="sxs-lookup"><span data-stu-id="f1d89-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="f1d89-109">Чтобы построить граф, начните с вызова метода [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1d89-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="f1d89-110">Первый параметр указывает тип файла — в данном случае это AVI.</span><span class="sxs-lookup"><span data-stu-id="f1d89-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="f1d89-111">Второй параметр задает имя файла.</span><span class="sxs-lookup"><span data-stu-id="f1d89-111">The second parameter gives the file name.</span></span> <span data-ttu-id="f1d89-112">Для AVI метод Сетаутпутфиленаме создает фильтр мультиплексора и фильтр для записи файлов и добавляет их в граф.</span><span class="sxs-lookup"><span data-stu-id="f1d89-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="f1d89-113">Он также задает имя файла в фильтре записи файлов путем вызова метода [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) и соединяет два фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1d89-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="f1d89-114">Метод возвращает указатель на мультиплексор AVI в третьем параметре.</span><span class="sxs-lookup"><span data-stu-id="f1d89-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="f1d89-115">При необходимости он возвращает указатель на интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) в четвертом параметре.</span><span class="sxs-lookup"><span data-stu-id="f1d89-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="f1d89-116">Если этот интерфейс не нужен, можно присвоить этому параметру **значение NULL**, как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f1d89-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="f1d89-117">Затем вызовите метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) для подключения фильтра записи к мультиплексору AVI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1d89-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="f1d89-118">Первый параметр дает категорию ПИН-кода, которая является закреплением \_ \_ захвата категории для захвата.</span><span class="sxs-lookup"><span data-stu-id="f1d89-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="f1d89-119">Второй параметр задает тип носителя.</span><span class="sxs-lookup"><span data-stu-id="f1d89-119">The second parameter gives the media type.</span></span> <span data-ttu-id="f1d89-120">Третий параметр является указателем на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра захвата.</span><span class="sxs-lookup"><span data-stu-id="f1d89-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="f1d89-121">Четвертый параметр является необязательным; Он позволяет направить поток видео через промежуточный фильтр, например кодировщик, перед его передачей в фильтр мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="f1d89-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="f1d89-122">В противном случае присвойте этому параметру **значение NULL**, как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f1d89-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="f1d89-123">Пятый параметр — это указатель на фильтр мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="f1d89-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="f1d89-124">Этот указатель получается путем вызова метода Сетаутпутфиленаме.</span><span class="sxs-lookup"><span data-stu-id="f1d89-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="f1d89-125">Для записи звука вызовите RenderStream с типом носителя Media \_ Audio.</span><span class="sxs-lookup"><span data-stu-id="f1d89-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="f1d89-126">Если вы записываете аудио и видео с двух отдельных устройств, рекомендуется сделать этот поток главным потоком.</span><span class="sxs-lookup"><span data-stu-id="f1d89-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="f1d89-127">Это помогает предотвратить смещение между двумя потоками, поскольку фильтр мультиплексора AVI корректирует скорость воспроизведения видеопотока в соответствии с звуковым потоком.</span><span class="sxs-lookup"><span data-stu-id="f1d89-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="f1d89-128">Чтобы задать главный поток, вызовите метод [**иконфигавимукс:: сетмастерстреам**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) в фильтре мультиплексора AVI:</span><span class="sxs-lookup"><span data-stu-id="f1d89-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="f1d89-129">Параметр для Сетмастерстреам — это номер потока, который определяется порядком вызова RenderStream.</span><span class="sxs-lookup"><span data-stu-id="f1d89-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="f1d89-130">Например, если для видео сначала вызывается RenderStream, а затем для звукового сигнала, видео является потоком 0, а звук — потоком 1.</span><span class="sxs-lookup"><span data-stu-id="f1d89-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="f1d89-131">Кроме того, может потребоваться задать способ, которым фильтр мультиплексора AVI будет чередовать звуковые и видеопотоки, вызвав метод [**иконфигинтерлеавинг: \_ :p UT**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="f1d89-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="f1d89-132">При использовании \_ флага записи чередования Камера AVI выполняет чередование с частотой, подходящей для видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="f1d89-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="f1d89-133">Кроме того, можно использовать ЧЕРЕДОВАНИе \_ None, что означает отсутствие чередования — МУЛЬТИПЛЕКСОР AVI будет просто записывать данные в порядке поступления.</span><span class="sxs-lookup"><span data-stu-id="f1d89-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="f1d89-134">Флаг ЧЕРЕДОВАНИя \_ означает, что он выполняет полное чередование, но этот режим менее подходит для видеозаписи, так как он требует наиболее полного перепрослушивания.</span><span class="sxs-lookup"><span data-stu-id="f1d89-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="f1d89-135">Кодирование видеопотока</span><span class="sxs-lookup"><span data-stu-id="f1d89-135">Encoding the Video Stream</span></span>

<span data-ttu-id="f1d89-136">Поток видео можно кодировать, вставив фильтр кодировщика между фильтром записи и фильтром мультиплексора AVI.</span><span class="sxs-lookup"><span data-stu-id="f1d89-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="f1d89-137">Используйте [перечислитель системных устройств](system-device-enumerator.md) или средство [сопоставления фильтров](filter-mapper.md) для выбора фильтра кодировщика.</span><span class="sxs-lookup"><span data-stu-id="f1d89-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="f1d89-138">(Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="f1d89-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="f1d89-139">Укажите фильтр кодировщика в качестве четвертого параметра для RenderStream, как показано жирным шрифтом в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="f1d89-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="f1d89-140">Фильтр кодировщика может поддерживать [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) или другие интерфейсы для настройки параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="f1d89-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="f1d89-141">Список возможных интерфейсов см. в разделе [интерфейсы кодирования и декодирования файлов](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f1d89-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d89-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f1d89-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d89-143">Запись видео в файл</span><span class="sxs-lookup"><span data-stu-id="f1d89-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



