---
description: Выбор правильного модуля подготовки видео
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Выбор правильного модуля подготовки видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673099"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="b2835-103">Выбор правильного модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="b2835-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="b2835-104">DirectShow предоставляет несколько фильтров модуля подготовки отчетов, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b2835-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="b2835-105">Фильтр</span><span class="sxs-lookup"><span data-stu-id="b2835-105">Filter</span></span>                                                                  | <span data-ttu-id="b2835-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2835-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="b2835-107">[**Улучшенный обработчик видео**](enhanced-video-renderer-filter.md) (Евр)</span><span class="sxs-lookup"><span data-stu-id="b2835-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="b2835-108">Использует Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b2835-108">Uses Direct3D 9.</span></span> <span data-ttu-id="b2835-109">Требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="b2835-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="b2835-110">[Устройство микширования видео 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="b2835-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="b2835-111">Использует Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b2835-111">Uses Direct3D 9.</span></span> <span data-ttu-id="b2835-112">Требуется Windows XP или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="b2835-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="b2835-113">[Фильтр микширования видео 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="b2835-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="b2835-114">Использует DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="b2835-114">Uses DirectDraw.</span></span> <span data-ttu-id="b2835-115">Требуется Windows XP или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="b2835-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="b2835-116">Микшер наложения</span><span class="sxs-lookup"><span data-stu-id="b2835-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="b2835-117">Поддерживает наложение оборудования через DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="b2835-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="b2835-118">Устаревший фильтр модуля [подготовки отчетов видео](video-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b2835-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="b2835-119">Использует DirectDraw или (редко) GDI</span><span class="sxs-lookup"><span data-stu-id="b2835-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="b2835-120">Используемый модуль подготовки в основном зависит от того, какие версии Windows необходимо поддерживать.</span><span class="sxs-lookup"><span data-stu-id="b2835-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="b2835-121">В Windows Vista и более поздних версиях приложения должны использовать евр, если оборудование его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="b2835-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="b2835-122">В противном случае возвращается к VMR-9 или VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b2835-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="b2835-123">Евр обеспечивает лучшую производительность и улучшает качество видео по сравнению с предыдущими модулями подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="b2835-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="b2835-124">Кроме того, он предназначен для работы с диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="b2835-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="b2835-125">В версиях, предшествовавших Windows Vista, используйте VMR-9, если оборудование поддерживает функции порта и видео, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="b2835-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="b2835-126">В противном случае используйте VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b2835-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="b2835-127">В старых системах может потребоваться использование микшера наложения (для видеопортов или поддержки наложения оборудования) или устаревшего фильтра модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="b2835-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="b2835-128">Методы [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) и [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) используют фильтр VMR-7 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2835-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="b2835-129">Если оборудование не поддерживает VMR-7, эти методы переходят в устаревший фильтр модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="b2835-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="b2835-130">Евр и VMR-9 никогда не являются модулями подготовки отчетов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2835-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2835-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b2835-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2835-132">Рендеринг видео</span><span class="sxs-lookup"><span data-stu-id="b2835-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



