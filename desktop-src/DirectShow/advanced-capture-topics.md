---
description: Разделы, посвященные расширенному записи
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Разделы, посвященные расширенному записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140363"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="c9cc8-103">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="c9cc8-103">Advanced Capture Topics</span></span>

<span data-ttu-id="c9cc8-104">В этом разделе описаны некоторые дополнительные аспекты видеозаписи в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="c9cc8-105">Большинство проблем, описанных в этом разделе, автоматически обрабатываются интерфейсом [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="c9cc8-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="c9cc8-106">Однако эти сведения могут оказаться полезными, если необходимо устранить неполадки в приложении видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="c9cc8-107">Кроме того, этот раздел следует прочесть, если приложение создает собственную диаграмму записи какого-либо типа, и вы обнаружите, что ICaptureGraphBuilder2 не соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="c9cc8-108">Наконец, в этом разделе содержатся некоторые сведения об использовании фильтра формирователя видео (VMR) в приложении видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="c9cc8-109">Граф видеозаписи можно создать целиком с помощью методов [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="c9cc8-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="c9cc8-110">Можно также объединить два интерфейса, используя ICaptureGraphBuilder2 для некоторых задач и Играфбуилдер для других.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="c9cc8-111">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="c9cc8-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="c9cc8-112">Обработка событий перерисовки в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="c9cc8-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="c9cc8-113">Работа с категориями ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="c9cc8-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="c9cc8-114">Использование фильтра Smart Tee</span><span class="sxs-lookup"><span data-stu-id="c9cc8-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="c9cc8-115">Использование микшера наложения в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="c9cc8-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="c9cc8-116">ПИН-коды порта видео</span><span class="sxs-lookup"><span data-stu-id="c9cc8-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="c9cc8-117">Тип формата VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="c9cc8-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="c9cc8-118">Создание фильтров Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="c9cc8-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="c9cc8-119">Фильтры драйвера класса WDM</span><span class="sxs-lookup"><span data-stu-id="c9cc8-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="c9cc8-120">Использование захвата WDDM в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9cc8-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="c9cc8-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c9cc8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9cc8-122">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="c9cc8-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



