---
description: Использование модуля подготовки видео для микширования
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Использование модуля подготовки видео для микширования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663754"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="3946d-103">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="3946d-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="3946d-104">С точки зрения производительности и широты функций фильтр формирователя видео (VMR) представляет следующее поколение видео на платформе Windows.</span><span class="sxs-lookup"><span data-stu-id="3946d-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="3946d-105">VMR заменяет [микшер наложения](overlay-mixer-filter.md) и модуль [подготовки видео](video-renderer-filter.md), а также добавляет множество новых функций смешивания.</span><span class="sxs-lookup"><span data-stu-id="3946d-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="3946d-106">Существует две версии VMR:</span><span class="sxs-lookup"><span data-stu-id="3946d-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="3946d-107">Фильтр VMR-7, использующий DirectDraw 7 для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="3946d-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="3946d-108">Фильтр VMR-9, использующий Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3946d-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="3946d-109">VMR-7 доступен в Windows XP и более поздних версиях, но недоступен для распространения.</span><span class="sxs-lookup"><span data-stu-id="3946d-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="3946d-110">VMR-9 доступен для распространения на всех платформах, поддерживаемых DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="3946d-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="3946d-111">Два фильтра VMR очень похожи на их реализацию и интерфейсы, которые они предоставляют.</span><span class="sxs-lookup"><span data-stu-id="3946d-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="3946d-112">VMR-9 имеет собственный CLSID и собственный набор интерфейсов, структур и типов перечислений, которые не всегда идентичны соответствующим типам данных для VMR-7 из-за базовых различий между DirectDraw 7 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3946d-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="3946d-113">Все интерфейсы VMR-9 заканчиваются «9», например **IVMRStreamConfig9**, а для структур и типов перечисления — «VMR9», чтобы отличать их от типов данных, используемых с VMR-7.</span><span class="sxs-lookup"><span data-stu-id="3946d-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="3946d-114">Для обеспечения обратной совместимости VMR-9 не является модулем подготовки отчетов по умолчанию в любой системе.</span><span class="sxs-lookup"><span data-stu-id="3946d-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="3946d-115">Чтобы использовать VMR-9, необходимо явно добавить его в граф фильтра с помощью метода [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) и настроить его перед подключением к любым вышестоящим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="3946d-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="3946d-116">Эта статья состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="3946d-116">This article contains the following sections.</span></span> <span data-ttu-id="3946d-117">Если не указано иное, сведения в этих разделах относятся к фильтрам VMR-7 и VMR-9.</span><span class="sxs-lookup"><span data-stu-id="3946d-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="3946d-118">О рендеринге видео</span><span class="sxs-lookup"><span data-stu-id="3946d-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="3946d-119">Режимы VMR в операции</span><span class="sxs-lookup"><span data-stu-id="3946d-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="3946d-120">Создание графа фильтра VMR-9</span><span class="sxs-lookup"><span data-stu-id="3946d-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="3946d-121">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="3946d-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="3946d-122">Настройка параметров чередования</span><span class="sxs-lookup"><span data-stu-id="3946d-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="3946d-123">Использование VMR для разработчиков фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="3946d-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="3946d-124">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="3946d-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="3946d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3946d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3946d-126">Фильтр визуализации 7 для микширования видео</span><span class="sxs-lookup"><span data-stu-id="3946d-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="3946d-127">Фильтр визуализации 9 для микшера видео</span><span class="sxs-lookup"><span data-stu-id="3946d-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



