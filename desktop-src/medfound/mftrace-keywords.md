---
description: С помощью Мфтраце можно отфильтровать результаты трассировки, указав список ключевых слов.
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: Ключевые слова Мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155346"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="48d70-103">Ключевые слова Мфтраце</span><span class="sxs-lookup"><span data-stu-id="48d70-103">MFTrace Keywords</span></span>

<span data-ttu-id="48d70-104">С помощью [мфтраце](mftrace.md)можно отфильтровать результаты трассировки, указав список ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="48d70-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="48d70-105">В командной строке используйте аргумент командной строки **-k** .</span><span class="sxs-lookup"><span data-stu-id="48d70-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="48d70-106">Кроме того, можно указать элемент [**keyword**](keyword.md) в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="48d70-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="48d70-107">Дополнительные сведения см. [в разделе Использование мфтраце](using-mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="48d70-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="48d70-108">Мфтраце поддерживает следующие ключевые слова:</span><span class="sxs-lookup"><span data-stu-id="48d70-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="48d70-109">Большинство из них относятся к определенным интерфейсам или экспортам библиотек.</span><span class="sxs-lookup"><span data-stu-id="48d70-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="48d70-110">"All"</span><span class="sxs-lookup"><span data-stu-id="48d70-110">"All"</span></span>
-   <span data-ttu-id="48d70-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="48d70-111">"Default"</span></span>
-   <span data-ttu-id="48d70-112">Модули Detour</span><span class="sxs-lookup"><span data-stu-id="48d70-112">"Detours"</span></span>
-   <span data-ttu-id="48d70-113">"Ифилтерграф"</span><span class="sxs-lookup"><span data-stu-id="48d70-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="48d70-114">"Играфбуилдер"</span><span class="sxs-lookup"><span data-stu-id="48d70-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="48d70-115">"Имедиаконтрол"</span><span class="sxs-lookup"><span data-stu-id="48d70-115">"IMediaControl"</span></span>
-   <span data-ttu-id="48d70-116">"Имедиаобжект"</span><span class="sxs-lookup"><span data-stu-id="48d70-116">"IMediaObject"</span></span>
-   <span data-ttu-id="48d70-117">"Имеминпутпин"</span><span class="sxs-lookup"><span data-stu-id="48d70-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="48d70-118">"Имфактивате"</span><span class="sxs-lookup"><span data-stu-id="48d70-118">"IMFActivate"</span></span>
-   <span data-ttu-id="48d70-119">"Имфаттрибутес"</span><span class="sxs-lookup"><span data-stu-id="48d70-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="48d70-120">"Имфбитестреам"</span><span class="sxs-lookup"><span data-stu-id="48d70-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="48d70-121">"Имфбитестреамхандлер"</span><span class="sxs-lookup"><span data-stu-id="48d70-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="48d70-122">"Имфклокк"</span><span class="sxs-lookup"><span data-stu-id="48d70-122">"IMFClock"</span></span>
-   <span data-ttu-id="48d70-123">"Имфмедиаевентженератор"</span><span class="sxs-lookup"><span data-stu-id="48d70-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="48d70-124">"Имфмедиасессион"</span><span class="sxs-lookup"><span data-stu-id="48d70-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="48d70-125">"Имфмедиасинк"</span><span class="sxs-lookup"><span data-stu-id="48d70-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="48d70-126">"Имфмедиасаурце"</span><span class="sxs-lookup"><span data-stu-id="48d70-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="48d70-127">"Имфмедиастреам"</span><span class="sxs-lookup"><span data-stu-id="48d70-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="48d70-128">"Имфпмедиаитем"</span><span class="sxs-lookup"><span data-stu-id="48d70-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="48d70-129">"Имфпмедиаплайер"</span><span class="sxs-lookup"><span data-stu-id="48d70-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="48d70-130">"Имфпмедиаплайеркаллбакк"</span><span class="sxs-lookup"><span data-stu-id="48d70-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="48d70-131">"Имфпресентатионклокк"</span><span class="sxs-lookup"><span data-stu-id="48d70-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="48d70-132">"Имфкуалитядвисе"</span><span class="sxs-lookup"><span data-stu-id="48d70-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="48d70-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="48d70-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="48d70-134">"Имфкуалитиманажер"</span><span class="sxs-lookup"><span data-stu-id="48d70-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="48d70-135">"Имфреадвритеклассфактори"</span><span class="sxs-lookup"><span data-stu-id="48d70-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="48d70-136">"Имфсампле"</span><span class="sxs-lookup"><span data-stu-id="48d70-136">"IMFSample"</span></span>
-   <span data-ttu-id="48d70-137">"Имфсчемехандлер"</span><span class="sxs-lookup"><span data-stu-id="48d70-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="48d70-138">"Имфсинквритер"</span><span class="sxs-lookup"><span data-stu-id="48d70-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="48d70-139">"Имфсаурцереадер"</span><span class="sxs-lookup"><span data-stu-id="48d70-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="48d70-140">"Имфсаурцереадеркаллбакк"</span><span class="sxs-lookup"><span data-stu-id="48d70-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="48d70-141">"Имфсаурцересолвер"</span><span class="sxs-lookup"><span data-stu-id="48d70-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="48d70-142">"Имфстреамсинк"</span><span class="sxs-lookup"><span data-stu-id="48d70-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="48d70-143">"Имфтополоадер"</span><span class="sxs-lookup"><span data-stu-id="48d70-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="48d70-144">"Имфтопологи"</span><span class="sxs-lookup"><span data-stu-id="48d70-144">"IMFTopology"</span></span>
-   <span data-ttu-id="48d70-145">"Имфтопологиноде"</span><span class="sxs-lookup"><span data-stu-id="48d70-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="48d70-146">"Имфтрансформ"</span><span class="sxs-lookup"><span data-stu-id="48d70-146">"IMFTransform"</span></span>
-   <span data-ttu-id="48d70-147">"Ивмреадер"</span><span class="sxs-lookup"><span data-stu-id="48d70-147">"IWMReader"</span></span>
-   <span data-ttu-id="48d70-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="48d70-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="48d70-149">"Мфекспорт"</span><span class="sxs-lookup"><span data-stu-id="48d70-149">"MFExport"</span></span>
-   <span data-ttu-id="48d70-150">"Мфплатекспорт"</span><span class="sxs-lookup"><span data-stu-id="48d70-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="48d70-151">"Мфплайекспорт"</span><span class="sxs-lookup"><span data-stu-id="48d70-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="48d70-152">"Мфпублик"</span><span class="sxs-lookup"><span data-stu-id="48d70-152">"MFPublic"</span></span>
-   <span data-ttu-id="48d70-153">"Мфреадвритикспорт"</span><span class="sxs-lookup"><span data-stu-id="48d70-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="48d70-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="48d70-154">"Ole32Export"</span></span>
-   <span data-ttu-id="48d70-155">"Вмвкорикспорт"</span><span class="sxs-lookup"><span data-stu-id="48d70-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="48d70-156">См. также</span><span class="sxs-lookup"><span data-stu-id="48d70-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d70-157">мфтраце</span><span class="sxs-lookup"><span data-stu-id="48d70-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="48d70-158">Использование Мфтраце</span><span class="sxs-lookup"><span data-stu-id="48d70-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



