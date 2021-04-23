---
description: Сведения об API перекодирования
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Сведения об API перекодирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558387"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="b7073-103">Сведения об API перекодирования</span><span class="sxs-lookup"><span data-stu-id="b7073-103">About the Transcode API</span></span>

<span data-ttu-id="b7073-104">На следующей схеме показано, как API-интерфейс перекодировки связан с остальной частью конвейера кодирования Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b7073-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![Схема, на которой показан API перекодирования.](images/encoding08.png)

<span data-ttu-id="b7073-106">Конвейер кодирования содержит следующие объекты обработки данных:</span><span class="sxs-lookup"><span data-stu-id="b7073-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="b7073-107">Источник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b7073-107">Media source</span></span>
-   <span data-ttu-id="b7073-108">Показан</span><span class="sxs-lookup"><span data-stu-id="b7073-108">Decoder</span></span>
-   <span data-ttu-id="b7073-109">Видеоконтроллер или повторный выбор звука</span><span class="sxs-lookup"><span data-stu-id="b7073-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="b7073-110">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="b7073-110">Encoder</span></span>
-   <span data-ttu-id="b7073-111">Приемник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b7073-111">Media sink</span></span>

<span data-ttu-id="b7073-112">Изменение размера видео требуется только в том случае, если размер выходного видео отличается от исходного.</span><span class="sxs-lookup"><span data-stu-id="b7073-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="b7073-113">Перевыборка аудио требуется только в том случае, если перед кодированием необходимо выполнить повторную выборку звука.</span><span class="sxs-lookup"><span data-stu-id="b7073-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="b7073-114">Пара декодера/кодировщика необходима для перекодирования, но не для ремуксинг.</span><span class="sxs-lookup"><span data-stu-id="b7073-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="b7073-115">*Топология* кодирования — это набор объектов конвейера (источника, декодера, изменения размера, средства перевыборки, кодировщика и приемника мультимедиа), а также точки соединения между ними.</span><span class="sxs-lookup"><span data-stu-id="b7073-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="b7073-116">Дополнительные сведения о топологиях см. в разделе [топологии](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b7073-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="b7073-117">Различные компоненты отвечают за создание различных объектов конвейера:</span><span class="sxs-lookup"><span data-stu-id="b7073-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="b7073-118">Приложение обычно использует [сопоставитель источников](source-resolver.md) для создания источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b7073-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="b7073-119">[Сеанс мультимедиа](media-session.md) загружает и настраивает декодер, видеоконтроллер и интерполяцию звука.</span><span class="sxs-lookup"><span data-stu-id="b7073-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="b7073-120">На внутреннем уровне для этого используется загрузчик топологии (см. [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="b7073-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="b7073-121">API-интерфейс перекодировки загружает и настраивает кодировщик и приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b7073-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="b7073-122">Расширенные приложения могут настроить кодировщик и приемник мультимедиа напрямую, а не использовать API перекодирования.</span><span class="sxs-lookup"><span data-stu-id="b7073-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7073-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b7073-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7073-124">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="b7073-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="b7073-125">Использование API перекодирования</span><span class="sxs-lookup"><span data-stu-id="b7073-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



