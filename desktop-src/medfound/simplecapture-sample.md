---
description: Демонстрация предварительного просмотра видео с устройства видеозаписи с помощью API Мфплай.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Пример Симплекаптуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263485"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="1e408-103">Пример Симплекаптуре</span><span class="sxs-lookup"><span data-stu-id="1e408-103">SimpleCapture Sample</span></span>

<span data-ttu-id="1e408-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1e408-104">\[Deprecated.</span></span> <span data-ttu-id="1e408-105">API Мфплай может быть удален из будущих выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="1e408-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="1e408-106">Приложения должны использовать [модуль чтения исходного кода](source-reader.md) для записи видео.\]</span><span class="sxs-lookup"><span data-stu-id="1e408-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="1e408-107">Демонстрация предварительного просмотра видео с устройства видеозаписи с помощью API Мфплай.</span><span class="sxs-lookup"><span data-stu-id="1e408-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="1e408-108">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="1e408-108">APIs Demonstrated</span></span>

<span data-ttu-id="1e408-109">В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="1e408-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="1e408-110">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="1e408-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="1e408-111">**имфпмедиаитем**</span><span class="sxs-lookup"><span data-stu-id="1e408-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="1e408-112">**имфпмедиаплайер**</span><span class="sxs-lookup"><span data-stu-id="1e408-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="1e408-113">**имфпмедиаплайеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1e408-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="1e408-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1e408-114">Requirements</span></span>



| <span data-ttu-id="1e408-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="1e408-115">Product</span></span>                                                        | <span data-ttu-id="1e408-116">Version</span><span class="sxs-lookup"><span data-stu-id="1e408-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="1e408-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1e408-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="1e408-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e408-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1e408-119">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="1e408-119">Downloading the Sample</span></span>

<span data-ttu-id="1e408-120">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span><span class="sxs-lookup"><span data-stu-id="1e408-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e408-121">См. также</span><span class="sxs-lookup"><span data-stu-id="1e408-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e408-122">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="1e408-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="1e408-123">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e408-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



