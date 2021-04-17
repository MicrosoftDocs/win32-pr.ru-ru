---
description: В этом разделе описывается использование аудио-и видеоэффектов с Мфплай.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Как добавить аудио или видео эффекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711799"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="61e72-103">Как добавить аудио или видео эффекты</span><span class="sxs-lookup"><span data-stu-id="61e72-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="61e72-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="61e72-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61e72-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="61e72-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="61e72-106">\]</span><span class="sxs-lookup"><span data-stu-id="61e72-106">\]</span></span>

<span data-ttu-id="61e72-107">В этом разделе описывается использование аудио-и видеоэффектов с Мфплай.</span><span class="sxs-lookup"><span data-stu-id="61e72-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="61e72-108">Чтобы использовать действие с Мфплай, этот результат должен быть реализован в виде Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="61e72-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="61e72-109">Дополнительные сведения см. в разделе [преобразования Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="61e72-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="61e72-110">**Добавление звуковых эффектов или видео**</span><span class="sxs-lookup"><span data-stu-id="61e72-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="61e72-111">Создайте экземпляр файла MFT, который реализует этот результат.</span><span class="sxs-lookup"><span data-stu-id="61e72-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="61e72-112">Вызовите [**имфпмедиаплайер:: инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span><span class="sxs-lookup"><span data-stu-id="61e72-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="61e72-113">Вызовите [**инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) перед открытием файла мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="61e72-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="61e72-114">Мфплай автоматически определяет, является ли это действие видеороликом или звуковым действием.</span><span class="sxs-lookup"><span data-stu-id="61e72-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="61e72-115">Метод [**инсертеффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) также принимает логический параметр, указывающий, является ли результат необязательным или обязательным.</span><span class="sxs-lookup"><span data-stu-id="61e72-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="61e72-116">Если Мфплай не может добавить требуемый результат (например, из-за несовместимости формата потока), возникает ошибка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="61e72-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="61e72-117">В большинстве случаев лучше задать необязательный результат.</span><span class="sxs-lookup"><span data-stu-id="61e72-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="61e72-118">Мфплай продолжит использовать этот результат для всех последующих воспроизведений.</span><span class="sxs-lookup"><span data-stu-id="61e72-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="61e72-119">Чтобы удалить этот результат, вызовите [**имфпмедиаплайер:: ремовиффект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) или [**Имфпмедиаплайер:: ремовеаллеффектс**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span><span class="sxs-lookup"><span data-stu-id="61e72-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="61e72-120">Требования</span><span class="sxs-lookup"><span data-stu-id="61e72-120">Requirements</span></span>

<span data-ttu-id="61e72-121">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61e72-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61e72-122">См. также</span><span class="sxs-lookup"><span data-stu-id="61e72-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61e72-123">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="61e72-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



