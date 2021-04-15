---
description: Запись файла DV типа 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Запись файла DV типа 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555053"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="e04aa-103">Запись файла DV типа 1</span><span class="sxs-lookup"><span data-stu-id="e04aa-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="e04aa-104">Файл AVI типа 1 DV содержит один поток с чередованием.</span><span class="sxs-lookup"><span data-stu-id="e04aa-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="e04aa-105">Чтобы записать файл типа 1 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e04aa-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![запись типа 1 с предварительным просмотром](images/dv1-cap.png)

<span data-ttu-id="e04aa-107">Фильтры в этой диаграмме включают:</span><span class="sxs-lookup"><span data-stu-id="e04aa-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="e04aa-108">Фильтр [Smart tee](smart-tee-filter.md) разделяет DV с чередованием на поток записи и предварительный просмотр потока.</span><span class="sxs-lookup"><span data-stu-id="e04aa-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="e04aa-109">Оба потока содержат одни и те же данные с чередованием.</span><span class="sxs-lookup"><span data-stu-id="e04aa-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="e04aa-110">Средство [мультиплексирования](avi-mux-filter.md) и [записи файлов](file-writer-filter.md) AVI записывает поток с чередованием на диск.</span><span class="sxs-lookup"><span data-stu-id="e04aa-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="e04aa-111">[Разделитель DV](dv-splitter-filter.md) разделяет поток с чередованием на поток видео в DV и аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="e04aa-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="e04aa-112">Оба потока являются рендерерд для предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="e04aa-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="e04aa-113">[Видеодекодер DV](dv-video-decoder-filter.md) дедекодирует видеопоток видео для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="e04aa-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="e04aa-114">Выполните сборку этого графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e04aa-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="e04aa-115">Вызовите [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , чтобы подключить фильтр мультиплексора AVI к фильтру записи файлов.</span><span class="sxs-lookup"><span data-stu-id="e04aa-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="e04aa-116">Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) с захватом категории ПИН-кода \_ \_ для отображения потока отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e04aa-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="e04aa-117">Построитель графов записи автоматически вставляет интеллектуальный фильтр Tee.</span><span class="sxs-lookup"><span data-stu-id="e04aa-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="e04aa-118">Вызовите RenderStream еще раз, но с помощью предварительной версии категории ПИН-кода \_ \_ для отображения предварительного просмотра потока.</span><span class="sxs-lookup"><span data-stu-id="e04aa-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="e04aa-119">Пропустите этот вызов, если вы не хотите просматривать видео.</span><span class="sxs-lookup"><span data-stu-id="e04aa-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="e04aa-120">Для обоих вызовов RenderStream типом носителя является носитель с \_ чередованием, что означает чередование DV-видео.</span><span class="sxs-lookup"><span data-stu-id="e04aa-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="e04aa-121">В этом коде построитель диаграмм записи автоматически добавляет каждый необходимый фильтр, за исключением фильтра записи МСДВ.</span><span class="sxs-lookup"><span data-stu-id="e04aa-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e04aa-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e04aa-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e04aa-123">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="e04aa-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



