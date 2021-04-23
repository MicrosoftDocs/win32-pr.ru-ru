---
description: В этом разделе описывается, как воспроизвести сегмент файла мультимедиа в Мфплай, установив время начала и окончания воспроизведения.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Воспроизведение клипа файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898058"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="3a82c-103">Воспроизведение клипа файла</span><span class="sxs-lookup"><span data-stu-id="3a82c-103">How to Play a File Clip</span></span>

<span data-ttu-id="3a82c-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3a82c-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3a82c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="3a82c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3a82c-106">\]</span><span class="sxs-lookup"><span data-stu-id="3a82c-106">\]</span></span>

<span data-ttu-id="3a82c-107">В этом разделе описывается, как воспроизвести сегмент файла мультимедиа в Мфплай, установив время начала и окончания воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3a82c-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="3a82c-108">**Воспроизведение клипа файла**</span><span class="sxs-lookup"><span data-stu-id="3a82c-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="3a82c-109">Вызовите [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) или [**Имфпмедиаплайер:: креатемедиаитемфромобжект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) , чтобы создать элемент мультимедиа для файла.</span><span class="sxs-lookup"><span data-stu-id="3a82c-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="3a82c-110">При необходимости получите общую длительность файла, как описано в разделе [как получить длительность воспроизведения](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="3a82c-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="3a82c-111">Вызовите [**имфпмедиаитем:: сетстартстоппоситион**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) , чтобы задать время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="3a82c-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="3a82c-112">Время окончания не должно превышать длительность файла.</span><span class="sxs-lookup"><span data-stu-id="3a82c-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="3a82c-113">Вызовите [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) , чтобы запустить воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="3a82c-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="3a82c-114">В следующем примере используется блокирующая версия [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="3a82c-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="3a82c-115">Если используется Неблокирующая версия, код, который появляется после **креатемедиаитемфромурл** , должен быть помещен в обработчик для события **МФП \_ \_ типа \_ MEDIAITEM \_ Created** .</span><span class="sxs-lookup"><span data-stu-id="3a82c-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="3a82c-116">Дополнительные сведения о событиях в Мфплай см. в разделе [получение событий от проигрывателя](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="3a82c-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="3a82c-117">Чтобы получить длительность файла, в этом примере вызывается `GetPlaybackDuration` функция, показанная в разделе [как получить длительность воспроизведения](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="3a82c-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3a82c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3a82c-118">Requirements</span></span>

<span data-ttu-id="3a82c-119">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a82c-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a82c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3a82c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a82c-121">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="3a82c-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



