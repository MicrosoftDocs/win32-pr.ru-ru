---
description: В этом учебнике представлено законченное приложение, которое воспроизводит видео с помощью Мфплай.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Учебник по Мфплай: воспроизведение видео'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812622"
---
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="97f4b-103">Учебник по Мфплай: воспроизведение видео</span><span class="sxs-lookup"><span data-stu-id="97f4b-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="97f4b-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="97f4b-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97f4b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="97f4b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="97f4b-106">\]</span><span class="sxs-lookup"><span data-stu-id="97f4b-106">\]</span></span>

<span data-ttu-id="97f4b-107">В этом учебнике представлено законченное приложение, которое воспроизводит видео с помощью Мфплай.</span><span class="sxs-lookup"><span data-stu-id="97f4b-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="97f4b-108">Он основан на образце пакета SDK для [симплеплай](simpleplay-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="97f4b-109">Этот учебник содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="97f4b-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="97f4b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="97f4b-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="97f4b-111">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="97f4b-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="97f4b-112">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="97f4b-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="97f4b-113">Объявление класса обратного вызова</span><span class="sxs-lookup"><span data-stu-id="97f4b-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="97f4b-114">Объявление функции Саферелеасе</span><span class="sxs-lookup"><span data-stu-id="97f4b-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="97f4b-115">Открытие файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="97f4b-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="97f4b-116">Обработчики сообщений окна</span><span class="sxs-lookup"><span data-stu-id="97f4b-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="97f4b-117">Реализация метода обратного вызова</span><span class="sxs-lookup"><span data-stu-id="97f4b-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="97f4b-118">Реализация WinMain</span><span class="sxs-lookup"><span data-stu-id="97f4b-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="97f4b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="97f4b-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="97f4b-120">Более подробное описание API Мфплай см. в разделе [Начало работы with мфплай](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="97f4b-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97f4b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="97f4b-121">Requirements</span></span>

<span data-ttu-id="97f4b-122">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97f4b-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="97f4b-123">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="97f4b-123">Header and Library Files</span></span>

<span data-ttu-id="97f4b-124">Включите в проект следующие файлы заголовков:</span><span class="sxs-lookup"><span data-stu-id="97f4b-124">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



<span data-ttu-id="97f4b-125">Ссылка на следующие библиотеки кода:</span><span class="sxs-lookup"><span data-stu-id="97f4b-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="97f4b-126">мфплай. lib</span><span class="sxs-lookup"><span data-stu-id="97f4b-126">mfplay.lib</span></span>
-   <span data-ttu-id="97f4b-127">Shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="97f4b-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="97f4b-128">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="97f4b-128">Global Variables</span></span>

<span data-ttu-id="97f4b-129">Объявите следующие глобальные переменные:</span><span class="sxs-lookup"><span data-stu-id="97f4b-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="97f4b-130">Эти переменные будут использоваться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="97f4b-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="97f4b-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*</span><span class="sxs-lookup"><span data-stu-id="97f4b-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="97f4b-132">Маркер окна приложения.</span><span class="sxs-lookup"><span data-stu-id="97f4b-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="97f4b-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ бвидео*</span><span class="sxs-lookup"><span data-stu-id="97f4b-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="97f4b-134">Логическое значение, которое отслеживает, воспроизводится ли видео.</span><span class="sxs-lookup"><span data-stu-id="97f4b-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="97f4b-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ пплайер*</span><span class="sxs-lookup"><span data-stu-id="97f4b-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="97f4b-136">Указатель на интерфейс [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="97f4b-137">Этот интерфейс используется для управления воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="97f4b-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="97f4b-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ пкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="97f4b-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="97f4b-139">Указатель на интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="97f4b-140">Приложение реализует этот интерфейс обратного вызова для получения уведомлений от объекта Player.</span><span class="sxs-lookup"><span data-stu-id="97f4b-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="97f4b-141">Объявление класса обратного вызова</span><span class="sxs-lookup"><span data-stu-id="97f4b-141">Declare the Callback Class</span></span>

<span data-ttu-id="97f4b-142">Чтобы получать уведомления о событиях из объекта Player, приложение должно реализовать интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="97f4b-143">В следующем коде объявляется класс, реализующий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="97f4b-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="97f4b-144">Единственной переменной-членом является *m \_ cref*, в которой хранится счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="97f4b-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="97f4b-145">Методы **IUnknown** реализуются встроенными методами.</span><span class="sxs-lookup"><span data-stu-id="97f4b-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="97f4b-146">Реализация метода [**имфпмедиаплайеркаллбакк:: онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) показана далее. см. раздел [Реализация метода обратного вызова](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="97f4b-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="97f4b-147">Объявление функции Саферелеасе</span><span class="sxs-lookup"><span data-stu-id="97f4b-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="97f4b-148">В рамках этого руководства функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса:</span><span class="sxs-lookup"><span data-stu-id="97f4b-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a><span data-ttu-id="97f4b-149">Открытие файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="97f4b-149">Open a Media File</span></span>

<span data-ttu-id="97f4b-150">`PlayMediaFile`Функция открывает файл мультимедиа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="97f4b-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="97f4b-151">Если параметр *g \_ Пплайер* имеет **значение NULL**, функция вызывает [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) для создания нового экземпляра объекта проигрывателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="97f4b-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="97f4b-152">Входные параметры для **мфпкреатемедиаплайер** включают указатель на интерфейс обратного вызова и маркер для окна видео.</span><span class="sxs-lookup"><span data-stu-id="97f4b-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="97f4b-153">Чтобы открыть файл мультимедиа, функция вызывает [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), передавая URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="97f4b-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="97f4b-154">Этот метод завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="97f4b-154">This method completes asynchronously.</span></span> <span data-ttu-id="97f4b-155">По завершении вызывается метод [**имфпмедиаплайеркаллбакк:: онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) приложения.</span><span class="sxs-lookup"><span data-stu-id="97f4b-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



<span data-ttu-id="97f4b-156">`OnFileOpen`Функция отображает диалоговое окно общего файла, позволяющее пользователю выбрать файл для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97f4b-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="97f4b-157">Интерфейс **ифилеопендиалог** используется для вывода диалогового окна общего файла.</span><span class="sxs-lookup"><span data-stu-id="97f4b-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="97f4b-158">Этот интерфейс является частью API оболочки Windows. Он появился в Windows Vista как замена старой функции **GetOpenFilename** .</span><span class="sxs-lookup"><span data-stu-id="97f4b-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="97f4b-159">После того как пользователь выберет файл, `OnFileOpen` вызывается `PlayMediaFile` для запуска воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97f4b-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a><span data-ttu-id="97f4b-160">Обработчики сообщений окна</span><span class="sxs-lookup"><span data-stu-id="97f4b-160">Window Message Handlers</span></span>

<span data-ttu-id="97f4b-161">Затем объявите обработчики сообщений для следующих оконных сообщений:</span><span class="sxs-lookup"><span data-stu-id="97f4b-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="97f4b-162">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="97f4b-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="97f4b-163">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="97f4b-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="97f4b-164">**\_Закрыть WM**</span><span class="sxs-lookup"><span data-stu-id="97f4b-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="97f4b-165">Для сообщения **WM \_ Paint** необходимо определить, воспроизводится ли видео в данный момент.</span><span class="sxs-lookup"><span data-stu-id="97f4b-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="97f4b-166">Если это так, вызовите метод [**имфпмедиаплайер:: упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="97f4b-167">Этот метод приводит к тому, что объект Player перерисовывает самый последний кадр видео.</span><span class="sxs-lookup"><span data-stu-id="97f4b-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="97f4b-168">Если видео нет, приложение несет ответственность за рисование окна.</span><span class="sxs-lookup"><span data-stu-id="97f4b-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="97f4b-169">В этом руководстве приложение просто вызывает функцию GDI **филлрект** для заполнения всей клиентской области.</span><span class="sxs-lookup"><span data-stu-id="97f4b-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="97f4b-170">Для сообщения **\_ размером WM** вызовите [**имфпмедиаплайер:: упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="97f4b-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="97f4b-171">Этот метод приводит к тому, что объект Player перестраивает видео в соответствии с текущим размером окна.</span><span class="sxs-lookup"><span data-stu-id="97f4b-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="97f4b-172">Обратите внимание, что **упдатевидео** используется как для **WM \_ Paint** , так и для **\_ размера WM**.</span><span class="sxs-lookup"><span data-stu-id="97f4b-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



<span data-ttu-id="97f4b-173">Для сообщения **о \_ закрытии WM** Освободите указатели [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) и [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="97f4b-174">Реализация метода обратного вызова</span><span class="sxs-lookup"><span data-stu-id="97f4b-174">Implement the Callback Method</span></span>

<span data-ttu-id="97f4b-175">Интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) определяет один метод, [**онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="97f4b-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="97f4b-176">Этот метод уведомляет приложение каждый раз при возникновении события во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97f4b-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="97f4b-177">Метод принимает один параметр — указатель на структуру [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="97f4b-178">Элемент **ивенттипе** структуры определяет произошедшее событие.</span><span class="sxs-lookup"><span data-stu-id="97f4b-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="97f4b-179">За структурой [**\_ \_ заголовков событий МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) могут следовать дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="97f4b-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="97f4b-180">Для каждого типа событий определяется макрос, который приводит указатель **\_ \_ заголовка события МФП** к структуре, относящейся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="97f4b-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="97f4b-181">(См. раздел [**\_ \_ Тип события МФП**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span><span class="sxs-lookup"><span data-stu-id="97f4b-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="97f4b-182">Для этого руководства важны два события:</span><span class="sxs-lookup"><span data-stu-id="97f4b-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="97f4b-183">Событие</span><span class="sxs-lookup"><span data-stu-id="97f4b-183">Event</span></span>                                    | <span data-ttu-id="97f4b-184">Описание</span><span class="sxs-lookup"><span data-stu-id="97f4b-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f4b-185">**\_ \_ создан тип события МФП \_ MEDIAITEM \_**</span><span class="sxs-lookup"><span data-stu-id="97f4b-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="97f4b-186">Посылается после завершения [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="97f4b-187">**\_ \_ \_ набор MEDIAITEM типа события \_ МФП**</span><span class="sxs-lookup"><span data-stu-id="97f4b-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="97f4b-188">Посылается, когда [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) завершается.</span><span class="sxs-lookup"><span data-stu-id="97f4b-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="97f4b-189">В следующем коде показано, как привести указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к структуре, относящейся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="97f4b-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



<span data-ttu-id="97f4b-190">Событие **МФП \_ \_ типа события \_ MEDIAITEM \_ Created** уведомляет приложение о завершении метода [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="97f4b-191">Структура событий содержит указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , представляющий элемент мультимедиа, созданный из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="97f4b-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="97f4b-192">Чтобы поместить элемент в очередь на воспроизведение, передайте этот указатель методу [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :</span><span class="sxs-lookup"><span data-stu-id="97f4b-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



<span data-ttu-id="97f4b-193">Событие **МФП \_ \_ типа события \_ MEDIAITEM \_ Set** уведомляет приложение о завершении [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="97f4b-194">Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать воспроизведение:</span><span class="sxs-lookup"><span data-stu-id="97f4b-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a><span data-ttu-id="97f4b-195">Реализация WinMain</span><span class="sxs-lookup"><span data-stu-id="97f4b-195">Implement WinMain</span></span>

<span data-ttu-id="97f4b-196">В оставшейся части этого руководства нет вызовов Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="97f4b-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="97f4b-197">В следующем коде показана процедура окна:</span><span class="sxs-lookup"><span data-stu-id="97f4b-197">The following code shows the window procedure:</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



<span data-ttu-id="97f4b-198">`InitializeWindow`Функция регистрирует класс окна приложения и создает окно.</span><span class="sxs-lookup"><span data-stu-id="97f4b-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



<span data-ttu-id="97f4b-199">Наконец, реализуйте точку входа приложения:</span><span class="sxs-lookup"><span data-stu-id="97f4b-199">Finally, implement the application entry point:</span></span>


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="97f4b-200">См. также</span><span class="sxs-lookup"><span data-stu-id="97f4b-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97f4b-201">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="97f4b-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



