---
description: Важное значение устарело.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Пример MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898198"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="420e5-103">Пример MFPlayer2</span><span class="sxs-lookup"><span data-stu-id="420e5-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="420e5-104">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="420e5-104">Deprecated.</span></span> <span data-ttu-id="420e5-105">Этот API может быть удален из будущих выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="420e5-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="420e5-106">Приложения должны использовать [сеанс мультимедиа](media-session.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="420e5-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="420e5-107">Демонстрирует некоторые функции воспроизведения, пропущенные в примере [симплеплай](simpleplay-sample.md) , например:</span><span class="sxs-lookup"><span data-stu-id="420e5-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="420e5-108">Нужна</span><span class="sxs-lookup"><span data-stu-id="420e5-108">Seeking</span></span>
-   <span data-ttu-id="420e5-109">Rate-управление (Быстрая перемотка вперед и назад)</span><span class="sxs-lookup"><span data-stu-id="420e5-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="420e5-110">Громкость звука и звуковые элементы управления</span><span class="sxs-lookup"><span data-stu-id="420e5-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="420e5-111">Масштаб видео</span><span class="sxs-lookup"><span data-stu-id="420e5-111">Video zoom</span></span>

<span data-ttu-id="420e5-112">На следующем рисунке показаны элементы управления, используемые для этих функций.</span><span class="sxs-lookup"><span data-stu-id="420e5-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="420e5-113">снимок экрана образца мфплайер</span><span class="sxs-lookup"><span data-stu-id="420e5-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="420e5-114">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="420e5-114">APIs Demonstrated</span></span>

<span data-ttu-id="420e5-115">В этом образце демонстрируются следующие API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="420e5-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="420e5-116">**иаудиосессионконтрол**</span><span class="sxs-lookup"><span data-stu-id="420e5-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="420e5-117">**иаудиосессионманажер**</span><span class="sxs-lookup"><span data-stu-id="420e5-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="420e5-118">**имфпмедиаитем**</span><span class="sxs-lookup"><span data-stu-id="420e5-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="420e5-119">**имфпмедиаплайер**</span><span class="sxs-lookup"><span data-stu-id="420e5-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="420e5-120">**имфпмедиаплайеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="420e5-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="420e5-121">**иммдевице**</span><span class="sxs-lookup"><span data-stu-id="420e5-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="420e5-122">**иммдевицеенумератор**</span><span class="sxs-lookup"><span data-stu-id="420e5-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="420e5-123">**исимплеаудиоволуме**</span><span class="sxs-lookup"><span data-stu-id="420e5-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="420e5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="420e5-124">Requirements</span></span>



| <span data-ttu-id="420e5-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="420e5-125">Product</span></span>                                                        | <span data-ttu-id="420e5-126">Version</span><span class="sxs-lookup"><span data-stu-id="420e5-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="420e5-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="420e5-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="420e5-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="420e5-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="420e5-129">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="420e5-129">Downloading the Sample</span></span>

<span data-ttu-id="420e5-130">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span><span class="sxs-lookup"><span data-stu-id="420e5-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="420e5-131">См. также</span><span class="sxs-lookup"><span data-stu-id="420e5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="420e5-132">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="420e5-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="420e5-133">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="420e5-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
