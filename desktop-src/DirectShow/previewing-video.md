---
description: Предварительный просмотр видео
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Предварительный просмотр видео (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567242"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="a3afd-103">Предварительный просмотр видео (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="a3afd-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="a3afd-104">Чтобы создать диаграмму предварительного просмотра видео, вызовите метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a3afd-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="a3afd-105">В этом примере предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="a3afd-105">This example assumes the following:</span></span>

-   <span data-ttu-id="a3afd-106">*пбуилд* был инициализирован, как описано в разделе [о построителе графов записи](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="a3afd-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="a3afd-107">*ПКАП* был инициализирован путем создания экземпляра фильтра записи и его добавления в граф фильтра, как описано в разделе [Выбор устройства записи](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="a3afd-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="a3afd-108">Первый параметр метода [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) задает категорию закрепления. для предварительного просмотра диаграммы используйте **\_ \_ Предварительный просмотр категории закрепления**.</span><span class="sxs-lookup"><span data-stu-id="a3afd-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="a3afd-109">Второй параметр указывает тип носителя, в качестве основного GUID типа.</span><span class="sxs-lookup"><span data-stu-id="a3afd-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="a3afd-110">Для видео используйте **\_ Формат MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="a3afd-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="a3afd-111">DV-устройства доставляют аудио и видео с чередованием, для которых используется тип носителя с **\_ чередованием**.</span><span class="sxs-lookup"><span data-stu-id="a3afd-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="a3afd-112">(Дополнительные сведения о записи DV см. [в статье Digital Video In DirectShow](digital-video-in-directshow.md).)</span><span class="sxs-lookup"><span data-stu-id="a3afd-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="a3afd-113">Третий параметр является указателем на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра захвата.</span><span class="sxs-lookup"><span data-stu-id="a3afd-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="a3afd-114">В этом примере следующие два параметра не требуются.</span><span class="sxs-lookup"><span data-stu-id="a3afd-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="a3afd-115">Они используются для указания дополнительных фильтров, которые могут потребоваться для визуализации потока.</span><span class="sxs-lookup"><span data-stu-id="a3afd-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="a3afd-116">Установка последнего параметра в **значение NULL** приводит к тому, что построитель диаграмм будет выбирать модуль подготовки отчетов по умолчанию для потока на основе типа носителя.</span><span class="sxs-lookup"><span data-stu-id="a3afd-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="a3afd-117">Для видео Построитель графов записи всегда использует фильтр модуля [подготовки](video-renderer-filter.md) отчетов в качестве модуля подготовки отчетов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3afd-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="a3afd-118">В Windows XP и более поздних версиях, хотя модуль подготовки видео (VMR) является модулем подготовки видео по умолчанию для методов [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , он не является модулем подготовки отчетов по умолчанию для метода [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="a3afd-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="a3afd-119">На любой платформе в построителе графов записи всегда используется старый фильтр модуля подготовки отчетов, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="a3afd-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="a3afd-120">Хотя Категория PIN-кодов указана **как \_ \_ Предварительная версия категории ПИН**-кода, она не имеет значения, имеет ли фильтр предварительный ПИН-код, он может иметь ПИН-код видеопорта или просто ПИН-код захвата.</span><span class="sxs-lookup"><span data-stu-id="a3afd-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="a3afd-121">В любом случае построитель графов записи автоматически создает правильный граф.</span><span class="sxs-lookup"><span data-stu-id="a3afd-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="a3afd-122">На следующей диаграмме показана самая простая диаграмма для предварительного просмотра видео.</span><span class="sxs-lookup"><span data-stu-id="a3afd-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![Диаграмма предварительного просмотра видео](images/vidcap01.png)

<span data-ttu-id="a3afd-124">На этой схеме фильтр записи имеет предварительный ПИН-код для предварительного просмотра, который подключается непосредственно к модулю подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="a3afd-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="a3afd-125">Если фильтр записи имеет только ПИН-код записи, построитель графа записи добавляет фильтр [Smart tee](smart-tee-filter.md) , который разделяет поток на поток записи и предварительный просмотр потока.</span><span class="sxs-lookup"><span data-stu-id="a3afd-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="a3afd-126">Это описано более подробно в статье [объединение видеороликов и предварительной версии](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="a3afd-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="a3afd-127">В некоторых случаях поток видео должен проходить через фильтр микшера наложения.</span><span class="sxs-lookup"><span data-stu-id="a3afd-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="a3afd-128">Если это так, метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) автоматически добавит его в граф.</span><span class="sxs-lookup"><span data-stu-id="a3afd-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3afd-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a3afd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3afd-130">Объединение видеозаписей и предварительной версии</span><span class="sxs-lookup"><span data-stu-id="a3afd-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="a3afd-131">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="a3afd-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



