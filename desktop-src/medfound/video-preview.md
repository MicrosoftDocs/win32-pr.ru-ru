---
description: В этом разделе описывается использование Мфплай для предварительного просмотра видео из видеокамеры.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Предварительный просмотр видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711385"
---
# <a name="video-preview"></a><span data-ttu-id="0a65e-103">Предварительный просмотр видео</span><span class="sxs-lookup"><span data-stu-id="0a65e-103">Video Preview</span></span>

<span data-ttu-id="0a65e-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0a65e-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a65e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0a65e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0a65e-106">\]</span><span class="sxs-lookup"><span data-stu-id="0a65e-106">\]</span></span>

<span data-ttu-id="0a65e-107">В этом разделе описывается использование Мфплай для предварительного просмотра видео из видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="0a65e-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="0a65e-108">Мфплай предоставляет самый простой способ Microsoft Media Foundation для предварительного просмотра видео с устройства записи.</span><span class="sxs-lookup"><span data-stu-id="0a65e-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="0a65e-109">Мфплай следует использовать, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0a65e-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="0a65e-110">Записывать видео в файл не нужно.</span><span class="sxs-lookup"><span data-stu-id="0a65e-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="0a65e-111">Точный контроль над отображением видео не требуется.</span><span class="sxs-lookup"><span data-stu-id="0a65e-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="0a65e-112">(Например, не нужно управлять созданием устройства Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="0a65e-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="0a65e-113">Перед отрисовкой не нужно обрабатывать видеоданные с камеры.</span><span class="sxs-lookup"><span data-stu-id="0a65e-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="0a65e-114">В противном случае [средство чтения исходного кода](source-reader.md) может быть лучшим вариантом.</span><span class="sxs-lookup"><span data-stu-id="0a65e-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="0a65e-115">Чтобы использовать Мфплай с устройством видеозаписи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0a65e-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="0a65e-116">Создайте источник мультимедиа для устройства записи.</span><span class="sxs-lookup"><span data-stu-id="0a65e-116">Create a media source for the capture device.</span></span> <span data-ttu-id="0a65e-117">См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="0a65e-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="0a65e-118">Вызовите [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) , чтобы создать экземпляр объекта Player.</span><span class="sxs-lookup"><span data-stu-id="0a65e-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="0a65e-119">Вызовите метод [**имфпмедиаплайер:: креатемедиаитемфромобжект**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) .</span><span class="sxs-lookup"><span data-stu-id="0a65e-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="0a65e-120">Передайте указатель на интерфейс Имфмедиасаурце источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0a65e-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="0a65e-121">Метод получает указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="0a65e-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="0a65e-122">Вызовите [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="0a65e-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="0a65e-123">Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="0a65e-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="0a65e-124">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="0a65e-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="0a65e-125">В типичном приложении необходимо предоставить указатель на интерфейс обратного вызова в функции [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) и использовать интерфейс обратного вызова для получения событий от проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="0a65e-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="0a65e-126">Для простоты показанный здесь код пропускает эти шаги.</span><span class="sxs-lookup"><span data-stu-id="0a65e-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="0a65e-127">Дополнительные сведения см. [в разделе Начало работы with мфплай](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="0a65e-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="0a65e-128">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="0a65e-128">Shutting Down</span></span>

<span data-ttu-id="0a65e-129">Перед завершением работы приложения завершите работу источника мультимедиа и объекта Player следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a65e-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="0a65e-130">Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0a65e-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="0a65e-131">Вызовите метод [**имфпмедиаплайер:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) в объекте Player.</span><span class="sxs-lookup"><span data-stu-id="0a65e-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="0a65e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0a65e-132">Requirements</span></span>

<span data-ttu-id="0a65e-133">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a65e-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a65e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0a65e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a65e-135">мфплай</span><span class="sxs-lookup"><span data-stu-id="0a65e-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="0a65e-136">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="0a65e-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



