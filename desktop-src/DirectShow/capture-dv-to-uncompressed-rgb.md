---
description: Записать DV в Распакованный RGB
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Записать DV в Распакованный RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139415"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="0a78d-103">Записать DV в Распакованный RGB</span><span class="sxs-lookup"><span data-stu-id="0a78d-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="0a78d-104">В этом примере показано, как записать DV с камеры и сохранить его в файле как несжатый RGB при предварительном просмотре.</span><span class="sxs-lookup"><span data-stu-id="0a78d-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="0a78d-105">Используйте граф фильтра, показанный на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="0a78d-105">Use the filter graph shown in the following diagram.</span></span>

![запись несжатого RGB в файл](images/dv-rgb-cap.png)

<span data-ttu-id="0a78d-107">Фильтр разделителя DV разделяет аудио-или видеофайлы с чередованием на отдельные видео и звуковые потоки. видео с цифровой кодировкой преобразуется в фильтр [видеодекодеров DV](dv-video-decoder-filter.md) , который выводит несжатое видео в формате RGB.</span><span class="sxs-lookup"><span data-stu-id="0a78d-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="0a78d-108">Видео RGB направляется через фильтр Smart tee в фильтр мультиплексора (для записи) и модуль подготовки видео (для предварительного просмотра).</span><span class="sxs-lookup"><span data-stu-id="0a78d-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="0a78d-109">В то же время поток аудио из разделителя DV проходит через фильтр неограниченного ПИН-кода tee для камеры AVI и модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="0a78d-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="0a78d-110">Диспетчер графов фильтров сохраняет все эти потоки в синхронизированном виде, используя метки времени для образцов и время ссылки на граф.</span><span class="sxs-lookup"><span data-stu-id="0a78d-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="0a78d-111">Эта диаграмма может показаться ненужной сложной, но она гарантирует, что поток видео с цифровой кодировкой будет декодирован только один раз, что снизит требования к ЦП.</span><span class="sxs-lookup"><span data-stu-id="0a78d-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="0a78d-112">Кроме того, обратите внимание, что видео проходит через фильтр Smart tee, когда звук проходит через фильтр неограниченного ПИН-кода Tee.</span><span class="sxs-lookup"><span data-stu-id="0a78d-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="0a78d-113">Smart tee может удалить кадры предварительного просмотра, чтобы улучшить производительность отслеживания, что желательно для видео, но не для звука, когда удаленные образцы очень заметны.</span><span class="sxs-lookup"><span data-stu-id="0a78d-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="0a78d-114">Кроме того, так как для звука требуется намного более низкая пропускная способность, чем в видеоролике, существует сравнительно немало шансов на удаление звука в файле.</span><span class="sxs-lookup"><span data-stu-id="0a78d-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="0a78d-115">Эту диаграмму необходимо создавать по одному разделу за раз, но метод RenderStream по-прежнему может помочь.</span><span class="sxs-lookup"><span data-stu-id="0a78d-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="0a78d-116">Используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0a78d-116">Use the following code:</span></span>


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



<span data-ttu-id="0a78d-117">Необходимо создать разделитель DV, видеодекодер DV, Smart tee и неограниченный ПИН-код tee и добавить каждый из них в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="0a78d-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="0a78d-118">(Для краткости эти шаги пропускаются из предыдущего кода.) В этом примере используется метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) для поиска ПИН-кодов записи и предварительного просмотра в фильтре Smart Tee. захват всегда выводит ПИН-код 0, а Предварительная версия — выходной ПИН-код 1.</span><span class="sxs-lookup"><span data-stu-id="0a78d-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a78d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0a78d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a78d-120">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a78d-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



