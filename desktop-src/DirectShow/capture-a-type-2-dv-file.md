---
description: Запись файла DV типа 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Запись файла DV типа 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894202"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="ab9b2-103">Запись файла DV типа 2</span><span class="sxs-lookup"><span data-stu-id="ab9b2-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="ab9b2-104">AVI-файл типа 2 DV содержит два потока, один из которых содержит видео DV и другое, содержащее звук.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="ab9b2-105">Чтобы записать файл типа 2 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![Тип 2. запись с предварительным просмотром](images/dv2-cap.png)

<span data-ttu-id="ab9b2-107">Этот граф почти тот же, что и граф для записи типа 1 (см. раздел [запись файла DV типа 1](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="ab9b2-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="ab9b2-108">Однако перед достижением фильтра [мультиплексора AVI](avi-mux-filter.md) поток отслеживания проходит через фильтр [разделителя DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ab9b2-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="ab9b2-109">Поэтому мультиплексор AVI получает два потока: аудиопоток и видео в кодировке DV.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="ab9b2-110">Выполните сборку этого графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ab9b2-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="ab9b2-111">Создайте разделитель DV и добавьте его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="ab9b2-112">Вызовите [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , чтобы подключить фильтр мультиплексора AVI к фильтру записи файлов.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="ab9b2-113">Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр записи Мсдв к разделителю DV.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="ab9b2-114">Этот вызов также подключает один из выходных контактов разделителя DV к мультиплексору AVI.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="ab9b2-115">Вызовите RenderStream еще раз, чтобы подключить другой ПИН-код разделителя DV к мультиплексору камеры AVI.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="ab9b2-116">Вызовите RenderStream третий раз, чтобы отобразить предварительный просмотр потока.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="ab9b2-117">Пропустите этот шаг, если не хотите выполнять предварительный просмотр видео.</span><span class="sxs-lookup"><span data-stu-id="ab9b2-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab9b2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ab9b2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab9b2-119">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab9b2-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



