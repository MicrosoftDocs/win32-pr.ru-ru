---
description: В этом разделе описывается, как реализовать воспроизведение звука и видео в приложении с помощью Microsoft Media Foundation.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Воспроизведение звука/видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692090"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="01e8f-103">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="01e8f-103">Audio/Video Playback</span></span>

<span data-ttu-id="01e8f-104">В этом разделе описывается, как реализовать воспроизведение звука и видео в приложении с помощью Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="01e8f-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01e8f-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="01e8f-105">In this section</span></span>



| <span data-ttu-id="01e8f-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="01e8f-106">Topic</span></span>                                                                                               | <span data-ttu-id="01e8f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="01e8f-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e8f-108">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01e8f-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="01e8f-109">В этом руководстве показано, как воспроизвести файлы мультимедиа с помощью объекта [сеанса мультимедиа](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="01e8f-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="01e8f-110">Воспроизведение защищенных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="01e8f-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="01e8f-111">Воспроизведение файлов, содержащих носитель, защищенный с использованием DRM.</span><span class="sxs-lookup"><span data-stu-id="01e8f-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="01e8f-112">Как определить длительность файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="01e8f-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="01e8f-113">Как определить длительность файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="01e8f-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="01e8f-114">Поиск, быстрая переадресация и обратная игра</span><span class="sxs-lookup"><span data-stu-id="01e8f-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="01e8f-115">В этом разделе показан пример кода для управления поиском и изменением скорости при использовании [сеанса мультимедиа](media-session.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="01e8f-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="01e8f-116">Как задать время окончания воспроизведения</span><span class="sxs-lookup"><span data-stu-id="01e8f-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="01e8f-117">В этом разделе описано, как задать время отмены воспроизведения при использовании [сеанса мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="01e8f-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="01e8f-118">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="01e8f-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="01e8f-119">Расширенный обработчик видео (Евр) — это компонент, отображающий видео на мониторе пользователя.</span><span class="sxs-lookup"><span data-stu-id="01e8f-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="01e8f-120">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="01e8f-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="01e8f-121">Потоковая прорисовка звука (САР) — это приемник мультимедиа, который визуализирует звук.</span><span class="sxs-lookup"><span data-stu-id="01e8f-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="01e8f-122">мфплай</span><span class="sxs-lookup"><span data-stu-id="01e8f-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="01e8f-123">API Мфплай является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="01e8f-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="01e8f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="01e8f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e8f-125">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01e8f-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="01e8f-126">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="01e8f-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="01e8f-127">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01e8f-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




