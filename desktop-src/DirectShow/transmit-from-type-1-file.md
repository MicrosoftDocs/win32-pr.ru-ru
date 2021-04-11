---
description: Передача из файла типа-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Передача из файла типа-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080938"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="68bd7-103">Передача из файла типа-1</span><span class="sxs-lookup"><span data-stu-id="68bd7-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="68bd7-104">Чтобы передать файл типа 1 при предварительном просмотре файла, используйте граф фильтра, показанный на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="68bd7-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![Тип-1. Передача с предварительной версией](images/dv1-transmit.png)

<span data-ttu-id="68bd7-106">Фильтры в этой диаграмме включают:</span><span class="sxs-lookup"><span data-stu-id="68bd7-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="68bd7-107">[Разделитель AVI](avi-splitter-filter.md) АНАЛИЗИРУЕТ файл AVI.</span><span class="sxs-lookup"><span data-stu-id="68bd7-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="68bd7-108">Для DV-файла типа 1 закрепление вывода обеспечивает чередование DV.</span><span class="sxs-lookup"><span data-stu-id="68bd7-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="68bd7-109">Фильтр [бесконечного ПИН-кода tee](infinite-pin-tee-filter.md) разделяет DV с чередованием на поток передачи и поток предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="68bd7-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="68bd7-110">Оба потока содержат одни и те же данные с чередованием.</span><span class="sxs-lookup"><span data-stu-id="68bd7-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="68bd7-111">(В этом графе вместо [смарт-tee](smart-tee-filter.md)используется неограниченный ПИН-код tee, так как при чтении из файла не существует опасности удаления кадров, как и в случае с динамической записью.)</span><span class="sxs-lookup"><span data-stu-id="68bd7-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="68bd7-112">[Разделитель DV](dv-splitter-filter.md) разделяет поток с чередованием на видеопоток видео, декодированный [видеодекодером DV](dv-video-decoder-filter.md)и звуковым потоком.</span><span class="sxs-lookup"><span data-stu-id="68bd7-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="68bd7-113">Оба потока являются рендерерд для предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="68bd7-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="68bd7-114">Выполните сборку этого графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="68bd7-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="68bd7-115">Вызовите [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="68bd7-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="68bd7-116">Создайте разделитель AVI и бесконечный ПИН-код tee и добавьте их в граф.</span><span class="sxs-lookup"><span data-stu-id="68bd7-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="68bd7-117">Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр источника к разделителю AVI.</span><span class="sxs-lookup"><span data-stu-id="68bd7-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="68bd7-118">Указание носителя \_ с чередованием для обеспечения сбоя метода, если исходный файл не является ФАЙЛОМ DV типа 1.</span><span class="sxs-lookup"><span data-stu-id="68bd7-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="68bd7-119">В этом случае можно выполнить откат и попытаться создать граф передачи типа 2.</span><span class="sxs-lookup"><span data-stu-id="68bd7-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="68bd7-120">Вызовите **RenderStream** еще раз, чтобы направить поток с чередованием из разделителя AVI на бесконечный ПИН-код Tee</span><span class="sxs-lookup"><span data-stu-id="68bd7-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="68bd7-121">Вызовите RenderStream третий раз, чтобы направить один поток из бесконечного ПИН-кода tee в фильтр МСДВ для передачи на устройство.</span><span class="sxs-lookup"><span data-stu-id="68bd7-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="68bd7-122">Вызовите **RenderStream** один раз, чтобы создать раздел для предварительного просмотра диаграммы.</span><span class="sxs-lookup"><span data-stu-id="68bd7-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="68bd7-123">Если вы не хотите использовать предварительную версию, просто подключите источник файла к фильтру МСДВ:</span><span class="sxs-lookup"><span data-stu-id="68bd7-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="68bd7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="68bd7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bd7-125">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="68bd7-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



