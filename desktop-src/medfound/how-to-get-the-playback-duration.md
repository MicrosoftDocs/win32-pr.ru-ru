---
description: В этом разделе описывается, как получить продолжительность воспроизведения файла мультимедиа с помощью Мфплай.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Как получить длительность воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650612"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="cac78-103">Как получить длительность воспроизведения</span><span class="sxs-lookup"><span data-stu-id="cac78-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="cac78-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cac78-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cac78-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="cac78-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cac78-106">\]</span><span class="sxs-lookup"><span data-stu-id="cac78-106">\]</span></span>

<span data-ttu-id="cac78-107">В этом разделе описывается, как получить продолжительность воспроизведения файла мультимедиа с помощью Мфплай.</span><span class="sxs-lookup"><span data-stu-id="cac78-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="cac78-108">**Получение времени воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="cac78-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="cac78-109">Вызовите [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) или [**Имфпмедиаплайер:: креатемедиаитемфромобжект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) , чтобы создать элемент мультимедиа для файла.</span><span class="sxs-lookup"><span data-stu-id="cac78-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="cac78-110">Вызовите [**имфпмедиаитем:: Duration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span><span class="sxs-lookup"><span data-stu-id="cac78-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="cac78-111">Укажите **МФП \_ поситионтипе \_ 100 НС** для первого параметра.</span><span class="sxs-lookup"><span data-stu-id="cac78-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="cac78-112">Длительность возвращается в виде **пропвариант** , содержащего **большое \_ целочисленное** значение.</span><span class="sxs-lookup"><span data-stu-id="cac78-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="cac78-113">Длительность задается в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="cac78-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="cac78-114">В следующем примере показан шаг 2.</span><span class="sxs-lookup"><span data-stu-id="cac78-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="cac78-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cac78-115">Requirements</span></span>

<span data-ttu-id="cac78-116">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cac78-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cac78-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cac78-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac78-118">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="cac78-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



