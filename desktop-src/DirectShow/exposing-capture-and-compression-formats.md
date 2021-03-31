---
description: Предоставление форматов записи и сжатия
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Предоставление форматов записи и сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806880"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="0aa46-103">Предоставление форматов записи и сжатия</span><span class="sxs-lookup"><span data-stu-id="0aa46-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="0aa46-104">В этой статье описывается, как вернуть форматы записи и сжатия с помощью метода [**иамстреамконфиг:: жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="0aa46-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="0aa46-105">Этот метод может получить дополнительные сведения о допустимых типах носителей, чем традиционный способ перечисления типов мультимедиа ПИН-кода, поэтому вместо него обычно следует использовать.</span><span class="sxs-lookup"><span data-stu-id="0aa46-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="0aa46-106">**Жетстреамкапс** может возвращать сведения о видах форматов, разрешенных для аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="0aa46-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="0aa46-107">Кроме того, в этой статье представлен пример кода, демонстрирующий способ повторного подключения входного ПИН-кода фильтра преобразования, чтобы фильтр мог выдать определенный результат.</span><span class="sxs-lookup"><span data-stu-id="0aa46-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="0aa46-108">Метод **жетстреамкапс** возвращает массив пар типов мультимедиа и структур возможностей.</span><span class="sxs-lookup"><span data-stu-id="0aa46-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="0aa46-109">Тип носителя — это структура [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , а возможности представлены либо структурой " [**\_ \_ \_ заглушка" конфигурации аудио потока**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) , либо структурой [**\_ \_ \_ capsing в конфигурации потока видео**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="0aa46-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="0aa46-110">В первом разделе этой статьи представлен пример видео, а во втором — пример звука.</span><span class="sxs-lookup"><span data-stu-id="0aa46-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="0aa46-111">Эта статья содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="0aa46-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="0aa46-112">Возможности видео</span><span class="sxs-lookup"><span data-stu-id="0aa46-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="0aa46-113">Возможности работы с аудио</span><span class="sxs-lookup"><span data-stu-id="0aa46-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="0aa46-114">Повторное подключение входных данных для обеспечения конкретных типов выходных данных</span><span class="sxs-lookup"><span data-stu-id="0aa46-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="0aa46-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0aa46-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa46-116">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="0aa46-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



