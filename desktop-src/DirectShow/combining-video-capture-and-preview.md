---
description: Объединение видеозаписей и предварительной версии
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Объединение видеозаписей и предварительной версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494634"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="dc232-103">Объединение видеозаписей и предварительной версии</span><span class="sxs-lookup"><span data-stu-id="dc232-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="dc232-104">В предыдущих разделах описывается запись видео в различные форматы файлов.</span><span class="sxs-lookup"><span data-stu-id="dc232-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="dc232-105">В разделе [Предварительный просмотр видео](previewing-video.md) описано, как создать график динамической предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="dc232-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="dc232-106">Однако многие приложения должны одновременно выполнять обе операции.</span><span class="sxs-lookup"><span data-stu-id="dc232-106">However, many applications must do both at once.</span></span> <span data-ttu-id="dc232-107">Чтобы создать объединенную предварительную версию и граф для создания файлов, просто сделайте два вызова [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span><span class="sxs-lookup"><span data-stu-id="dc232-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="dc232-108">В этом коде построитель графа записи скрывает некоторые сведения:</span><span class="sxs-lookup"><span data-stu-id="dc232-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="dc232-109">Если фильтр записи имеет ПИН-код предварительной версии или PIN-код, а также ПИН-код записи, метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) просто визуализирует оба контакта, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc232-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![Диаграмма записи и предварительного просмотра](images/vidcap04.png)

-   <span data-ttu-id="dc232-111">Если фильтр имеет только ПИН-код захвата, Построитель графов записи использует фильтр [Smart tee](smart-tee-filter.md) для разделения потока записи.</span><span class="sxs-lookup"><span data-stu-id="dc232-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="dc232-112">На следующем рисунке показан граф с Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="dc232-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![запись и предварительный просмотр графа с помощью интеллектуального фильтра Tee](images/vidcap05.png)

<span data-ttu-id="dc232-114">Фильтр Smart tee имеет ПИН-код захвата и предварительный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="dc232-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="dc232-115">Он принимает один поток видео из фильтра записи и разделяет его на два потока: один для захвата и один для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="dc232-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="dc232-116">Чтобы обеспечить пропускную способность для ПИН-кода записи, при необходимости предварительный ПИН-код удаляет кадры.</span><span class="sxs-lookup"><span data-stu-id="dc232-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="dc232-117">Кроме того, он позволяет отформатировать отметки времени от каждого примера перед его доставкой, по причинам, описанным в разделе [фильтры записи видео DirectShow](directshow-video-capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="dc232-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="dc232-118">Хотя Smart tee разделяет поток, он физически не дублирует данные видео.</span><span class="sxs-lookup"><span data-stu-id="dc232-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="dc232-119">Вместо этого он использует пользовательские образцы объектов мультимедиа, которые совместно используют буферы.</span><span class="sxs-lookup"><span data-stu-id="dc232-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="dc232-120">Образцы помечаются как "только для чтения", чтобы не записывать данные в подчиненных фильтрах.</span><span class="sxs-lookup"><span data-stu-id="dc232-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="dc232-121">Если на диаграмме записи есть окно предварительного просмотра, то в диспетчере графов фильтров может быть остановлен весь граф, включая поток записи:</span><span class="sxs-lookup"><span data-stu-id="dc232-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="dc232-122">Блокировка компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc232-122">Locking the computer.</span></span>
-   <span data-ttu-id="dc232-123">Нажав клавиши CTRL + ALT + DELETE на компьютере, который является членом домена.</span><span class="sxs-lookup"><span data-stu-id="dc232-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="dc232-124">Запуск полноэкранного приложения Direct3D, такого как игра или экранная заставка.</span><span class="sxs-lookup"><span data-stu-id="dc232-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="dc232-125">Переключение мониторов или изменение разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="dc232-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="dc232-126">Запуск программы, которая заставляет Windows отображать диалоговое окно контроля учетных записей (UAC).</span><span class="sxs-lookup"><span data-stu-id="dc232-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="dc232-127">(Windows Vista или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="dc232-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="dc232-128">Запуск полноэкранного окна DOS.</span><span class="sxs-lookup"><span data-stu-id="dc232-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="dc232-129">Любое из этих событий может привести к прерыванию сеанса записи, возможно, в результате потери данных.</span><span class="sxs-lookup"><span data-stu-id="dc232-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="dc232-130">(Вот что происходит внутри: модуль подготовки видео теряет необходимые ресурсы Direct3D или DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="dc232-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="dc232-131">В процессе восстановления этих ресурсов модуль подготовки отчетов должен повторно подключиться к вышестоящему фильтру, что приведет к тому, что диспетчер графов фильтров завершит работу графа.)</span><span class="sxs-lookup"><span data-stu-id="dc232-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="dc232-132">Ниже приведены два возможных решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="dc232-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="dc232-133">Не включайте поток предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="dc232-133">Do not include a preview stream.</span></span> <span data-ttu-id="dc232-134">Однако имейте в виду, что метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) автоматически добавляет окно предварительного просмотра, когда устройство записи имеет ПИН-код видеопорта.</span><span class="sxs-lookup"><span data-stu-id="dc232-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="dc232-135">См. раздел [Контакты видеопортов в записи файлов](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="dc232-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="dc232-136">Используйте механизм буфера потока для отправки потока просмотра в граф в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="dc232-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc232-137">См. также</span><span class="sxs-lookup"><span data-stu-id="dc232-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc232-138">Запись видео в файл</span><span class="sxs-lookup"><span data-stu-id="dc232-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



