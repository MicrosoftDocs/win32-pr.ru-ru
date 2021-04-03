---
description: В этом разделе приведен шаг 4 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: Шаг 4. Создание сеанса мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999984"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="0c327-103">Шаг 4. Создание сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0c327-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="0c327-104">В этом разделе приведен шаг 4 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="0c327-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="0c327-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="0c327-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="0c327-106">`CPlayer::CreateSession`Создает новый экземпляр сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c327-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



<span data-ttu-id="0c327-107">Этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0c327-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="0c327-108">Вызывает метод `CPlayer::CloseSession` , чтобы закрыть все предыдущие экземпляры сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c327-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="0c327-109">Вызывает [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) для создания нового экземпляра сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c327-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="0c327-110">Вызывает метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) для запроса следующего события из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c327-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="0c327-111">Первый параметр для **бегинжетевент** — это указатель на сам объект **кплайер** , который имплентс интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="0c327-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="0c327-112">Обработка событий описана на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="0c327-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="0c327-113">Далее: [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="0c327-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c327-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0c327-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c327-115">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="0c327-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="0c327-116">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c327-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



