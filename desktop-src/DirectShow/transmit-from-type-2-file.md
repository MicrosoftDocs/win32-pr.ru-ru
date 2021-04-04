---
description: Передача из файла типа 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Передача из файла типа 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998700"
---
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="bb929-103">Передача из файла типа 2</span><span class="sxs-lookup"><span data-stu-id="bb929-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="bb929-104">Чтобы передать файл типа 2 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="bb929-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![Тип-2. Передача с предварительной версией](images/dv2-transmit.png)

<span data-ttu-id="bb929-106">Файл типа 2 имеет два потока: один аудиопоток и один поток видео в кодировке DV.</span><span class="sxs-lookup"><span data-stu-id="bb929-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="bb929-107">В этой диаграмме для объединения аудио и видеопотоков используется фильтр [DV мультиплексор](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="bb929-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="bb929-108">Он отправляет поток с чередованием в фильтр МСДВ, но снова разделяет поток для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="bb929-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="bb929-109">Выполните сборку этого графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bb929-109">Build this graph as follows:</span></span>


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



<span data-ttu-id="bb929-110">Этот код выполняет несколько вызовов **RenderStream**:</span><span class="sxs-lookup"><span data-stu-id="bb929-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="bb929-111">Первые два способа соединяют фильтр источника с разделителем AVI и разделителем AVI с видеомультиплексором.</span><span class="sxs-lookup"><span data-stu-id="bb929-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="bb929-112">При первом вызове построитель диаграмм автоматически добавляет разделитель AVI к графу и подключает один из выходных контактов разделителя AVI к мультиплексору DV.</span><span class="sxs-lookup"><span data-stu-id="bb929-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="bb929-113">Во втором вызове построитель графа записи находит второй выходной ПИН-код разделителя AVI и подключается к мультиплексору DV.</span><span class="sxs-lookup"><span data-stu-id="bb929-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="bb929-114">Третий вызов **RenderStream** подключает DV мультиплексор к фильтру Tee с бесконечным ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="bb929-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="bb929-115">Следующий вызов соединяет один поток от бесконечного ПИН-кода Tee с фильтром записи МСДВ.</span><span class="sxs-lookup"><span data-stu-id="bb929-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="bb929-116">Этот поток передается на устройство.</span><span class="sxs-lookup"><span data-stu-id="bb929-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="bb929-117">Последний вызов **RenderStream** создает раздел предварительного просмотра диаграммы.</span><span class="sxs-lookup"><span data-stu-id="bb929-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="bb929-118">Если вы не хотите выполнять предварительный просмотр во время передачи, можно опустить неограниченный ПИН-код tee и просто подключить цифровой мультиплексор к фильтру МСДВ:</span><span class="sxs-lookup"><span data-stu-id="bb929-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="bb929-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bb929-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb929-120">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bb929-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



