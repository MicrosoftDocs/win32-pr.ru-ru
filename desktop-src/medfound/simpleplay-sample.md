---
description: Показывает, как воспроизвести файл мультимедиа с помощью API Мфплай.
ms.assetid: 1acd6f98-af59-47fd-9a3e-38a668fb6acf
title: Пример Симплеплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02fee507ffed7bd91664f67ffb725565f47c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711393"
---
# <a name="simpleplay-sample"></a><span data-ttu-id="4b01a-103">Пример Симплеплай</span><span class="sxs-lookup"><span data-stu-id="4b01a-103">SimplePlay Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b01a-104">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4b01a-104">Deprecated.</span></span> <span data-ttu-id="4b01a-105">Этот API может быть удален из будущих выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="4b01a-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="4b01a-106">Приложения должны использовать [сеанс мультимедиа](media-session.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4b01a-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="4b01a-107">Показывает, как воспроизвести файл мультимедиа с помощью API Мфплай.</span><span class="sxs-lookup"><span data-stu-id="4b01a-107">Shows how to play a media file using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="4b01a-108">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="4b01a-108">APIs Demonstrated</span></span>

<span data-ttu-id="4b01a-109">В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="4b01a-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="4b01a-110">**имфпмедиаитем**</span><span class="sxs-lookup"><span data-stu-id="4b01a-110">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="4b01a-111">**имфпмедиаплайер**</span><span class="sxs-lookup"><span data-stu-id="4b01a-111">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="4b01a-112">**имфпмедиаплайеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4b01a-112">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="4b01a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4b01a-113">Requirements</span></span>



| <span data-ttu-id="4b01a-114">Продукт</span><span class="sxs-lookup"><span data-stu-id="4b01a-114">Product</span></span>                                                        | <span data-ttu-id="4b01a-115">Version</span><span class="sxs-lookup"><span data-stu-id="4b01a-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="4b01a-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4b01a-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="4b01a-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b01a-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4b01a-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="4b01a-118">Downloading the Sample</span></span>

<span data-ttu-id="4b01a-119">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span><span class="sxs-lookup"><span data-stu-id="4b01a-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b01a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4b01a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b01a-121">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b01a-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="4b01a-122">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="4b01a-122">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



