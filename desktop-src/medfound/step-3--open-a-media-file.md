---
description: В этом разделе описывается этап 3 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: Шаг 3. Открытие файла мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081710"
---
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="e461b-103">Шаг 3. Открытие файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e461b-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="e461b-104">В этом разделе описывается этап 3 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="e461b-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="e461b-106">`CPlayer::OpenURL`Метод открывает файл мультимедиа из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e461b-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="e461b-107">Этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e461b-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="e461b-108">Вызывает **кплайер:: CreateSession** для создания нового экземпляра сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e461b-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="e461b-109">См. [Шаг 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="e461b-110">Создает источник мультимедиа по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="e461b-110">Creates a media source from the URL.</span></span> <span data-ttu-id="e461b-111">Полный код для этого шага приведен в разделе [Использование сопоставителя источников](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="e461b-112">Вызывает [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы получить дескриптор представления источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e461b-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="e461b-113">Дескриптор представления описывает каждый поток в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="e461b-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="e461b-114">Создает топологию воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e461b-114">Creates the playback topology.</span></span> <span data-ttu-id="e461b-115">Код для этого шага показан в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="e461b-116">Вызывает [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e461b-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="e461b-117">Метод [**сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e461b-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="e461b-118">По завершении вызывается метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта кплайер; см. [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="e461b-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="e461b-119">Далее: [Шаг 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="e461b-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e461b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e461b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e461b-121">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="e461b-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="e461b-122">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e461b-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



