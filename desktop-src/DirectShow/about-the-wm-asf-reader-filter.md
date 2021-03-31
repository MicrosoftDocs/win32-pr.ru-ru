---
description: Сведения о фильтре средства чтения ASF-файлов WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Сведения о фильтре средства чтения ASF-файлов WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894982"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="263ed-103">Сведения о фильтре средства чтения ASF-файлов WM</span><span class="sxs-lookup"><span data-stu-id="263ed-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="263ed-104">Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="263ed-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="263ed-105">Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока.</span><span class="sxs-lookup"><span data-stu-id="263ed-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="263ed-106">В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков.</span><span class="sxs-lookup"><span data-stu-id="263ed-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="263ed-107">Чтобы воспроизвести файл ASF с фильтром чтения WM ASF, вызовите метод [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или [**Играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="263ed-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="263ed-108">Модуль чтения WM ASF поддерживает интерфейс DirectShow [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , позволяющий приложениям выполнять временное Поиск в файле.</span><span class="sxs-lookup"><span data-stu-id="263ed-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="263ed-109">Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)), не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="263ed-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="263ed-110">Фильтр чтения WM ASF также предоставляет несколько интерфейсов Windows Media Format SDK, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="263ed-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="263ed-111">Эти интерфейсы описаны в документации пакета Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="263ed-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="263ed-112">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="263ed-112">Interface</span></span>                                             | <span data-ttu-id="263ed-113">Как предоставлено</span><span class="sxs-lookup"><span data-stu-id="263ed-113">How exposed</span></span>                                 | <span data-ttu-id="263ed-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="263ed-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="263ed-115">**ивмдрмреадер**</span><span class="sxs-lookup"><span data-stu-id="263ed-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="263ed-116">Через **IServiceProvider** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="263ed-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="263ed-117">Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="263ed-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="263ed-118">**ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="263ed-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="263ed-119">**QueryInterface** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="263ed-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="263ed-120">Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.</span><span class="sxs-lookup"><span data-stu-id="263ed-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="263ed-121">**ивмреадерадванцед**</span><span class="sxs-lookup"><span data-stu-id="263ed-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="263ed-122">**QueryInterface** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="263ed-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="263ed-123">Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.</span><span class="sxs-lookup"><span data-stu-id="263ed-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="263ed-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="263ed-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="263ed-125">**QueryInterface** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="263ed-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="263ed-126">Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам в формате объекта чтения SDK.</span><span class="sxs-lookup"><span data-stu-id="263ed-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="263ed-127">См. также</span><span class="sxs-lookup"><span data-stu-id="263ed-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="263ed-128">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="263ed-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



