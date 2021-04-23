---
description: Мфплай — это API для создания приложений воспроизведения мультимедиа на C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: начало работы с Мфплай
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496800"
---
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="0179a-103">начало работы с Мфплай</span><span class="sxs-lookup"><span data-stu-id="0179a-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="0179a-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0179a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0179a-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0179a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0179a-106">\]</span><span class="sxs-lookup"><span data-stu-id="0179a-106">\]</span></span>

<span data-ttu-id="0179a-107">Мфплай — это API для создания приложений воспроизведения мультимедиа на C++.</span><span class="sxs-lookup"><span data-stu-id="0179a-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="0179a-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0179a-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0179a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0179a-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0179a-110">О Мфплай</span><span class="sxs-lookup"><span data-stu-id="0179a-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="0179a-111">Воспроизведение файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0179a-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="0179a-112">Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="0179a-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="0179a-113">Получение событий от проигрывателя</span><span class="sxs-lookup"><span data-stu-id="0179a-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="0179a-114">Получение сведений о файле мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0179a-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="0179a-115">Управление воспроизведением видео</span><span class="sxs-lookup"><span data-stu-id="0179a-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="0179a-116">Ограничения Мфплай</span><span class="sxs-lookup"><span data-stu-id="0179a-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="0179a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0179a-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0179a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0179a-118">Requirements</span></span>

<span data-ttu-id="0179a-119">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0179a-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="0179a-120">О Мфплай</span><span class="sxs-lookup"><span data-stu-id="0179a-120">About MFPlay</span></span>

<span data-ttu-id="0179a-121">Мфплай имеет простую модель программирования, предоставляя основной набор функций, которые требуются большинству приложений для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0179a-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="0179a-122">Приложение создает объект *Player* , управляющий воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="0179a-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="0179a-123">Для воспроизведения файла мультимедиа объект Player создает *элемент мультимедиа*, который можно использовать для получения сведений о содержимом файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="0179a-124">Приложение управляет воспроизведением с помощью методов в интерфейсе [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) объекта Player.</span><span class="sxs-lookup"><span data-stu-id="0179a-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="0179a-125">При необходимости приложение может получать уведомления о событиях через интерфейс обратного вызова на следующей схеме показана эта процедура.</span><span class="sxs-lookup"><span data-stu-id="0179a-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![Концептуальная схема: приложение и игрок указывают друг на друга, обе указывают на элемент мультимедиа, указывающий на файл мультимедиа](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="0179a-127">Воспроизведение файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0179a-127">Playing a Media File</span></span>

<span data-ttu-id="0179a-128">Чтобы воспроизвести файл мультимедиа, вызовите функцию [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="0179a-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="0179a-129">Функция [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) создает новый экземпляр объекта Player мфплай.</span><span class="sxs-lookup"><span data-stu-id="0179a-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="0179a-130">Функция принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0179a-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="0179a-131">Первый параметр — это URL-адрес открываемого файла.</span><span class="sxs-lookup"><span data-stu-id="0179a-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="0179a-132">Это может быть локальный файл или файл на сервере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="0179a-133">Второй параметр указывает, запускается ли воспроизведение автоматически.</span><span class="sxs-lookup"><span data-stu-id="0179a-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="0179a-134">Если задать для этого пареметер **значение true**, файл будет воспроизводиться, как только мфплай загрузит его.</span><span class="sxs-lookup"><span data-stu-id="0179a-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="0179a-135">Третий параметр задает различные параметры.</span><span class="sxs-lookup"><span data-stu-id="0179a-135">The third parameter sets various options.</span></span> <span data-ttu-id="0179a-136">Для параметров по умолчанию передайте ноль (0).</span><span class="sxs-lookup"><span data-stu-id="0179a-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="0179a-137">Четвертый параметр — это указатель на необязательный интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0179a-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="0179a-138">Этот параметр может иметь **значение NULL**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0179a-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="0179a-139">Обратный вызов описан в разделе [получение событий от проигрывателя](#receiving-events-from-the-player).</span><span class="sxs-lookup"><span data-stu-id="0179a-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="0179a-140">Пятый параметр — это обработчик окна приложения.</span><span class="sxs-lookup"><span data-stu-id="0179a-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="0179a-141">Если файл мультимедиа содержит видеопоток, то в клиентской области этого окна появится видео.</span><span class="sxs-lookup"><span data-stu-id="0179a-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="0179a-142">Для воспроизведения только звука этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0179a-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="0179a-143">Последний параметр получает указатель на интерфейс [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) объекта Player.</span><span class="sxs-lookup"><span data-stu-id="0179a-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="0179a-144">Перед завершением работы приложения не забудьте освободить указатель [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="0179a-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="0179a-145">Это можно сделать в обработчике сообщений **WM \_ Close** .</span><span class="sxs-lookup"><span data-stu-id="0179a-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="0179a-146">В этом примере функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0179a-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="0179a-147">Для простого воспроизведения видео это весь код, который вам нужен.</span><span class="sxs-lookup"><span data-stu-id="0179a-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="0179a-148">В оставшейся части этого руководства будет показано, как добавить дополнительные функции, начиная с управления воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="0179a-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="0179a-149">Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="0179a-149">Controlling Playback</span></span>

<span data-ttu-id="0179a-150">Код, приведенный в предыдущем разделе, воспроизводит файл мультимедиа, пока не достигнет конца файла.</span><span class="sxs-lookup"><span data-stu-id="0179a-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="0179a-151">Вы можете запустить воспроизведение, вызвав следующие методы в интерфейсе [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :</span><span class="sxs-lookup"><span data-stu-id="0179a-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="0179a-152">[**Имфпмедиаплайер::P Аусе**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) приостанавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="0179a-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="0179a-153">Пока воспроизведение приостановлено, отображается последняя видеорамка, а звук не отображается в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="0179a-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="0179a-154">[**Имфпмедиаплайер:: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="0179a-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="0179a-155">Видео не отображается, а значение расположения воспроизведения сбрасывается до начала файла.</span><span class="sxs-lookup"><span data-stu-id="0179a-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="0179a-156">[**Имфпмедиаплайер::Pный макет**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) возобновляет воспроизведение после остановки или приостановки.</span><span class="sxs-lookup"><span data-stu-id="0179a-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="0179a-157">Следующий код приостанавливает или возобновляет воспроизведение при нажатии клавиши **пробел**.</span><span class="sxs-lookup"><span data-stu-id="0179a-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



<span data-ttu-id="0179a-158">В этом примере вызывается метод [**имфпмедиаплайер::-State**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) для получения текущего состояния воспроизведения (пауза, остановка или воспроизведение), а также приостановка или возобновление соответственно.</span><span class="sxs-lookup"><span data-stu-id="0179a-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="0179a-159">Получение событий от проигрывателя</span><span class="sxs-lookup"><span data-stu-id="0179a-159">Receiving Events From the Player</span></span>

<span data-ttu-id="0179a-160">Мфплай использует интерфейс обратного вызова для отправки событий в приложение.</span><span class="sxs-lookup"><span data-stu-id="0179a-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="0179a-161">Для этого обратного вызова существует две причины.</span><span class="sxs-lookup"><span data-stu-id="0179a-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="0179a-162">Воспроизведение выполняется в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="0179a-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="0179a-163">Во время воспроизведения могут возникнуть определенные события, например достижение конца файла.</span><span class="sxs-lookup"><span data-stu-id="0179a-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="0179a-164">Мфплай использует обратный вызов для уведомления приложения о событии.</span><span class="sxs-lookup"><span data-stu-id="0179a-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="0179a-165">Многие методы [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) являются асинхронными, то есть они возвращаются до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="0179a-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="0179a-166">Асинхронные методы позволяют запустить операцию из потока пользовательского интерфейса, выполнение которого может занять много времени, не вызывая блокировки пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0179a-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="0179a-167">После завершения операции Мфплай сигнализирует обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="0179a-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="0179a-168">Чтобы получать уведомления обратного вызова, реализуйте интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="0179a-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="0179a-169">Этот интерфейс наследует **IUnknown** и определяет единственный метод [**онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="0179a-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="0179a-170">Чтобы настроить обратный вызов, передайте указатель на реализацию **имфпмедиаплайеркаллбакк** в параметре *пкаллбакк* функции [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="0179a-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="0179a-171">Ниже приведен первый пример из этого руководства, который был изменен для включения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0179a-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="0179a-172">Метод [**онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) имеет один параметр, который является указателем на структуру [**\_ \_ заголовков событий МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="0179a-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="0179a-173">Элемент **ивенттипе** этой структуры сообщает, какое событие произошло.</span><span class="sxs-lookup"><span data-stu-id="0179a-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="0179a-174">Например, при запуске воспроизведения Мфплай отправляет событие **\_ \_ \_ воспроизведения типа события МФП** .</span><span class="sxs-lookup"><span data-stu-id="0179a-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="0179a-175">Каждый тип события имеет соответствующую структуру данных, содержащую сведения для этого события.</span><span class="sxs-lookup"><span data-stu-id="0179a-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="0179a-176">Каждая из этих структур начинается с структуры [**\_ \_ заголовков событий МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="0179a-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="0179a-177">В ответном вызове приведите указатель **\_ \_ заголовка события МФП** к структуре данных, относящейся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="0179a-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="0179a-178">Например, если событие имеет тип **МФП \_ Play \_**, структура данных является [**\_ \_ событием МФП Play**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="0179a-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="0179a-179">В следующем коде показано, как справиться с этим событием в обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="0179a-179">The following code shows how to handle this event in the callback.</span></span>


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



<span data-ttu-id="0179a-180">В этом примере используется [**событие \_ МФП \_ Get \_ Play**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) для приведения указателя *певенсеадер* к структуре [**событий МФП \_ Play \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .</span><span class="sxs-lookup"><span data-stu-id="0179a-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="0179a-181">Значение **HRESULT** из операции, вызвавшей событие, хранится в поле **хревент** структуры.</span><span class="sxs-lookup"><span data-stu-id="0179a-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="0179a-182">Список всех типов событий и соответствующих структур данных см. в разделе [**МФП \_ event \_ Type**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="0179a-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="0179a-183">Примечание о многопоточности. по умолчанию Мфплай вызывает обратный вызов из того же потока, который вызвал [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span><span class="sxs-lookup"><span data-stu-id="0179a-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="0179a-184">Этот поток должен иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="0179a-184">This thread must have a message loop.</span></span> <span data-ttu-id="0179a-185">Кроме того, можно передать **параметр МФП с \_ возможностью \_ освобождения \_ потокового \_ вызова** в параметре *креатионоптионс* **мфпкреатемедиаплайер**.</span><span class="sxs-lookup"><span data-stu-id="0179a-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="0179a-186">Этот флаг заставляет Мфплай вызывать обратные вызовы из отдельного потока.</span><span class="sxs-lookup"><span data-stu-id="0179a-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="0179a-187">Любой из этих параметров влияет на работу приложения.</span><span class="sxs-lookup"><span data-stu-id="0179a-187">Either option has implications for your application.</span></span> <span data-ttu-id="0179a-188">Параметр по умолчанию означает, что ваш обратный вызов не сможет выполнить никаких действий, ожидающих выполнения цикла обработки сообщений, например ожидания действия пользовательского интерфейса, так как он блокирует процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="0179a-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="0179a-189">Режим "бесплатный поток" означает, что для защиты любых данных, к которым вы обращаетесь при обратном вызове, необходимо использовать критические разделы.</span><span class="sxs-lookup"><span data-stu-id="0179a-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="0179a-190">В большинстве случаев параметр по умолчанию является простейшим.</span><span class="sxs-lookup"><span data-stu-id="0179a-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="0179a-191">Получение сведений о файле мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0179a-191">Getting Information About a Media File</span></span>

<span data-ttu-id="0179a-192">При открытии файла мультимедиа в Мфплай проигрыватель создает объект, называемый *элементом мультимедиа* , представляющим файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="0179a-193">Этот объект предоставляет интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , который можно использовать для получения сведений о файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="0179a-194">Многие структуры событий Мфплай содержат указатель на текущий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="0179a-195">Вы также можете получить текущий элемент мультимедиа, вызвав [**имфпмедиаплайер:: жетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) на проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="0179a-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="0179a-196">Два особенно полезных метода — [**имфпмедиаитем:: хасвидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) и [**Имфпмедиаитем:: хасаудио**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span><span class="sxs-lookup"><span data-stu-id="0179a-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="0179a-197">Эти методы запрашивают, содержит ли источник мультимедиа видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="0179a-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="0179a-198">Например, следующий код проверяет, содержит ли текущий файл мультимедиа поток видео.</span><span class="sxs-lookup"><span data-stu-id="0179a-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



<span data-ttu-id="0179a-199">Если исходный файл содержит поток видео, выбранный для воспроизведения, то для *бхасвидео* и *Бисселектед* устанавливается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0179a-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="0179a-200">Управление воспроизведением видео</span><span class="sxs-lookup"><span data-stu-id="0179a-200">Managing Video Playback</span></span>

<span data-ttu-id="0179a-201">Когда Мфплай воспроизводит видеофайл, он рисует видео в окне, которое вы указали в функции [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="0179a-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="0179a-202">Это происходит в отдельном потоке, принадлежащем конвейеру воспроизведения Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0179a-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="0179a-203">В большинстве случаев для приложения не требуется управлять этим процессом.</span><span class="sxs-lookup"><span data-stu-id="0179a-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="0179a-204">Однако существует две ситуации, когда приложение должно уведомлять Мфплай об обновлении видео.</span><span class="sxs-lookup"><span data-stu-id="0179a-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="0179a-205">Если воспроизведение приостановлено или остановлено, Мфплай должно быть уведомлено всякий раз, когда видеоокно приложения получает \_ сообщение WM Paint.</span><span class="sxs-lookup"><span data-stu-id="0179a-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="0179a-206">Это позволяет Мфплай перерисовывать окно.</span><span class="sxs-lookup"><span data-stu-id="0179a-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="0179a-207">При изменении размера окна Мфплай должно быть уведомлено, чтобы можно было масштабировать видео в соответствии с новым размером окна.</span><span class="sxs-lookup"><span data-stu-id="0179a-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="0179a-208">Метод [**имфпмедиаплайер:: упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) обрабатывает оба варианта.</span><span class="sxs-lookup"><span data-stu-id="0179a-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="0179a-209">Вызывайте этот метод в \_ обработчиках сообщений WM Paint и WM \_ size для окна видео.</span><span class="sxs-lookup"><span data-stu-id="0179a-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0179a-210">Вызовите функцию GDI **бегинпаинт** перед вызовом [**упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="0179a-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="0179a-211">Если не указано иное, Мфплай отображает видео с правильными пропорциями, используя пустых при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0179a-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="0179a-212">Если вы не хотите сохранять пропорции, вызовите [**имфпмедиаплайер:: сетаспектратиомоде**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) с флагом **мфвидеоармоде \_ None** .</span><span class="sxs-lookup"><span data-stu-id="0179a-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="0179a-213">Это приведет к тому, что Мфплай растягивает видео для заполнения всего прямоугольника без пустых.</span><span class="sxs-lookup"><span data-stu-id="0179a-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="0179a-214">Обычно следует использовать параметр по умолчанию и позволить Мфплай леттербокс видео.</span><span class="sxs-lookup"><span data-stu-id="0179a-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="0179a-215">Цвет леттербокс по умолчанию — черный, но его можно изменить, вызвав [**имфпмедиаплайер:: сетбордерколор**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span><span class="sxs-lookup"><span data-stu-id="0179a-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="0179a-216">Ограничения Мфплай</span><span class="sxs-lookup"><span data-stu-id="0179a-216">Limitations of MFPlay</span></span>

<span data-ttu-id="0179a-217">Текущая версия Мфплай имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="0179a-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="0179a-218">Мфплай не поддерживает содержимое, защищенное DRM.</span><span class="sxs-lookup"><span data-stu-id="0179a-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="0179a-219">По умолчанию Мфплай не поддерживает протоколы сетевой потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0179a-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="0179a-220">Дополнительные сведения см. в разделе [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="0179a-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="0179a-221">Мфплай не поддерживает списки воспроизведения на стороне сервера (Ссплс) или другие типы источников, которые воспроизводят более одного сегмента.</span><span class="sxs-lookup"><span data-stu-id="0179a-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="0179a-222">В технических терминах Мфплай останавливает воспроизведение после первой презентации и игнорирует все события [меневпресентатион](menewpresentation.md) из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="0179a-223">Мфплай не поддерживает плавные переходы между источниками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0179a-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="0179a-224">Мфплай не поддерживает смешивание нескольких видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="0179a-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="0179a-225">Мфплай поддерживаются только форматы мультимедиа, которые поддерживаются встроенными в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0179a-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="0179a-226">(Сюда относятся сторонние Media Foundation компоненты, которые могут быть установлены в системе.)</span><span class="sxs-lookup"><span data-stu-id="0179a-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0179a-227">См. также</span><span class="sxs-lookup"><span data-stu-id="0179a-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0179a-228">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="0179a-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



