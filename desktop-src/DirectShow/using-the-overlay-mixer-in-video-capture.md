---
description: Использование микшера наложения в видеозаписи
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Использование микшера наложения в видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081087"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="2b47e-103">Использование микшера наложения в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2b47e-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="2b47e-104">Существуют определенные виды видео, которые фильтр модуля [подготовки видео](video-renderer-filter.md) не может отобразить сам по себе.</span><span class="sxs-lookup"><span data-stu-id="2b47e-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="2b47e-105">В таких ситуациях модуль подготовки отчетов должен работать с фильтром [микшера наложения](overlay-mixer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="2b47e-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="2b47e-106">Микшер наложения управляет отрисовкой, а модуль подготовки видео управляет окном видео.</span><span class="sxs-lookup"><span data-stu-id="2b47e-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="2b47e-107">Микшер наложения необходим в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="2b47e-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="2b47e-108">Контакты порта видео (вице-президент).</span><span class="sxs-lookup"><span data-stu-id="2b47e-108">Video port (VP) pins.</span></span> <span data-ttu-id="2b47e-109">Если устройство записи использует порт видео, микшер наложения управляет наложением оборудования.</span><span class="sxs-lookup"><span data-stu-id="2b47e-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="2b47e-110">Видео с чередованием.</span><span class="sxs-lookup"><span data-stu-id="2b47e-110">Interlaced video.</span></span> <span data-ttu-id="2b47e-111">Для видео с чередованием декодеру требуется формат [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , который не поддерживается модулем подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="2b47e-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="2b47e-112">Субтитры.</span><span class="sxs-lookup"><span data-stu-id="2b47e-112">Closed captions.</span></span> <span data-ttu-id="2b47e-113">Текст заголовка отображается в виде точечных рисунков размером 8 бит на пиксель, накладываемых микшером наложения на видео.</span><span class="sxs-lookup"><span data-stu-id="2b47e-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="2b47e-114">Метод **RenderStream** построителя графа записи вставляет микшер наложения при необходимости.</span><span class="sxs-lookup"><span data-stu-id="2b47e-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="2b47e-115">Однако при построении графа без использования построителя графа записи необходимо проверить каждую из этих ситуаций и вставить микшер наложения.</span><span class="sxs-lookup"><span data-stu-id="2b47e-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="2b47e-116">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="2b47e-116">\[!Important\]</span></span>  
    > <span data-ttu-id="2b47e-117">Если у устройства есть свой вице-президент, необходимо подключить микшер наложения, даже если в приложении не требуются функции предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="2b47e-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="2b47e-118">При использовании видеопорта устройство записи всегда отправляет данные видео в наложение оборудования, поэтому микшер наложения всегда нужен.</span><span class="sxs-lookup"><span data-stu-id="2b47e-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="2b47e-119">Фильтры рендеринга для микширования видео (VMR-7 и VMR-9) поддерживают чередование видео и могут смешивать точечные рисунки субтитров на основном видео.</span><span class="sxs-lookup"><span data-stu-id="2b47e-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="2b47e-120">Если для этих сценариев используется фильтр VMR, использовать микшер наложения не нужно.</span><span class="sxs-lookup"><span data-stu-id="2b47e-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="2b47e-121">VMR-9 не поддерживает подключения "вице-президент".</span><span class="sxs-lookup"><span data-stu-id="2b47e-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="2b47e-122">VMR-7 поддерживает подключения "вице-президент" через фильтр диспетчера видеопортов.</span><span class="sxs-lookup"><span data-stu-id="2b47e-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="2b47e-123">Однако может оказаться, что некоторые драйверы не работают правильно с диспетчером видеопортов.</span><span class="sxs-lookup"><span data-stu-id="2b47e-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="2b47e-124">По этой причине микшер наложения по-прежнему рекомендуется для закрепления президента.</span><span class="sxs-lookup"><span data-stu-id="2b47e-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b47e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2b47e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b47e-126">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="2b47e-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="2b47e-127">ПИН-коды порта видео</span><span class="sxs-lookup"><span data-stu-id="2b47e-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="2b47e-128">Тип формата VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="2b47e-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



