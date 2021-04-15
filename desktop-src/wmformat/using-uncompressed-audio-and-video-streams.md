---
title: Использование несжатых потоков аудио и видео
description: Использование несжатых потоков аудио и видео
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- потоки, Настройка несжатых аудио и видеопотоков
- кодеки, Настройка несжатых аудио и видеопотоков
- видеопотоки, без сжатия
- звуковые потоки, без сжатия
- несжатые аудио и видео потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710239"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="a6efc-108">Использование несжатых потоков аудио и видео</span><span class="sxs-lookup"><span data-stu-id="a6efc-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="a6efc-109">В большинстве случаев несжатые носители имеют неограниченные требования к хранению и доставке, но для некоторых сценариев локального воспроизведения уровень качества достаточно важен, чтобы не использовать сжатие.</span><span class="sxs-lookup"><span data-stu-id="a6efc-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="a6efc-110">Параметры для несжатого потока мультимедиа должны отражать параметры исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="a6efc-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="a6efc-111">При настройке несжатого потока необходимо вычислить скорость потока мультимедиа и соответствующим образом задать поток, вызвав [**ивмстреамконфиг:: сетбитрате**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span><span class="sxs-lookup"><span data-stu-id="a6efc-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="a6efc-112">Так как несжатые потоки недоступны для потоковой передачи, всегда следует задать для окна буфера несжатых потоков мультимедиа нулевое значение, вызвав [**ивмстреамконфиг:: сетбуффервиндов**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span><span class="sxs-lookup"><span data-stu-id="a6efc-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="a6efc-113">Для несжатых видеопотоков поддерживаются следующие форматы пикселей:</span><span class="sxs-lookup"><span data-stu-id="a6efc-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="a6efc-114">ВММЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a6efc-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="a6efc-115">ВММЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="a6efc-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="a6efc-116">ВММЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a6efc-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="a6efc-117">ВММЕДИАСУБТИПЕ \_ I420</span><span class="sxs-lookup"><span data-stu-id="a6efc-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="a6efc-118">ВММЕДИАСУБТИПЕ \_ ийув</span><span class="sxs-lookup"><span data-stu-id="a6efc-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="a6efc-119">ВММЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="a6efc-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="a6efc-120">ВММЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="a6efc-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="a6efc-121">ВММЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="a6efc-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="a6efc-122">ВММЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="a6efc-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6efc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a6efc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6efc-124">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="a6efc-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="a6efc-125">**Настройка звуковых потоков**</span><span class="sxs-lookup"><span data-stu-id="a6efc-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="a6efc-126">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="a6efc-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="a6efc-127">**Настройка потоков видео**</span><span class="sxs-lookup"><span data-stu-id="a6efc-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




