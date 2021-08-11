---
description: В этом учебнике представлено законченное приложение, которое воспроизводит видео с помощью Мфплай.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Учебник по Мфплай: воспроизведение видео'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5b98de6cc845d121928fb18a33db055154f717e8fe583bcd1ad6ef8da32deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242011"
---
# <a name="mfplay-tutorial-video-playback"></a>Учебник по Мфплай: воспроизведение видео

\[Мфплай доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. \]

В этом учебнике представлено законченное приложение, которое воспроизводит видео с помощью Мфплай. Он основан на образце пакета SDK для [симплеплай](simpleplay-sample.md) .

Этот учебник содержит следующие подразделы:

-   [Требования](#requirements)
-   [Файлы заголовков и библиотек](#header-and-library-files)
-   [Глобальные переменные](#global-variables)
-   [Объявление класса обратного вызова](#declare-the-callback-class)
-   [Объявление функции Саферелеасе](#declare-the-saferelease-function)
-   [Открытие файла мультимедиа](#open-a-media-file)
-   [Обработчики сообщений окна](#window-message-handlers)
-   [Реализация метода обратного вызова](#implement-the-callback-method)
-   [Реализация WinMain](#implement-winmain)
-   [Связанные темы](#related-topics)

Более подробное описание API Мфплай см. в разделе [Начало работы with мфплай](getting-started-with-mfplay.md).

## <a name="requirements"></a>Требования

для мфплай требуется Windows 7.

## <a name="header-and-library-files"></a>Файлы заголовков и библиотек

Включите в проект следующие файлы заголовков:


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



Ссылка на следующие библиотеки кода:

-   мфплай. lib
-   Shlwapi. lib

## <a name="global-variables"></a>Глобальные переменные

Объявите следующие глобальные переменные:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Эти переменные будут использоваться следующим образом:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*
</dt> <dd>

Маркер окна приложения.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ бвидео*
</dt> <dd>

Логическое значение, которое отслеживает, воспроизводится ли видео.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ пплайер*
</dt> <dd>

Указатель на интерфейс [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Этот интерфейс используется для управления воспроизведением.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ пкаллбакк*
</dt> <dd>

Указатель на интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . Приложение реализует этот интерфейс обратного вызова для получения уведомлений от объекта Player.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Объявление класса обратного вызова

Чтобы получать уведомления о событиях из объекта Player, приложение должно реализовать интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . В следующем коде объявляется класс, реализующий интерфейс. Единственной переменной-членом является *m \_ cref*, в которой хранится счетчик ссылок.

Методы **IUnknown** реализуются встроенными методами. Реализация метода [**имфпмедиаплайеркаллбакк:: онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) показана далее. см. раздел [Реализация метода обратного вызова](#implement-the-callback-method).


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



## <a name="declare-the-saferelease-function"></a>Объявление функции Саферелеасе

В рамках этого руководства функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса:


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



## <a name="open-a-media-file"></a>Открытие файла мультимедиа

`PlayMediaFile`Функция открывает файл мультимедиа следующим образом:

1.  Если параметр *g \_ Пплайер* имеет **значение NULL**, функция вызывает [**мфпкреатемедиаплайер**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) для создания нового экземпляра объекта проигрывателя мультимедиа. Входные параметры для **мфпкреатемедиаплайер** включают указатель на интерфейс обратного вызова и маркер для окна видео.
2.  Чтобы открыть файл мультимедиа, функция вызывает [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), передавая URL-адрес файла. Этот метод завершается асинхронно. По завершении вызывается метод [**имфпмедиаплайеркаллбакк:: онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) приложения.


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



`OnFileOpen`Функция отображает диалоговое окно общего файла, позволяющее пользователю выбрать файл для воспроизведения. Интерфейс **ифилеопендиалог** используется для вывода диалогового окна общего файла. этот интерфейс является частью интерфейсов api оболочки Windows; он появился в Windows Vista в качестве замены для старой функции **GetOpenFileName** . После того как пользователь выберет файл, `OnFileOpen` вызывается `PlayMediaFile` для запуска воспроизведения.


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



## <a name="window-message-handlers"></a>Обработчики сообщений окна

Затем объявите обработчики сообщений для следующих оконных сообщений:

-   **WM \_ Paint**
-   **\_Размер WM**
-   **\_Закрыть WM**

Для сообщения **WM \_ Paint** необходимо определить, воспроизводится ли видео в данный момент. Если это так, вызовите метод [**имфпмедиаплайер:: упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) . Этот метод приводит к тому, что объект Player перерисовывает самый последний кадр видео.

Если видео нет, приложение несет ответственность за рисование окна. В этом руководстве приложение просто вызывает функцию GDI **филлрект** для заполнения всей клиентской области.


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



Для сообщения **\_ размером WM** вызовите [**имфпмедиаплайер:: упдатевидео**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo). Этот метод приводит к тому, что объект Player перестраивает видео в соответствии с текущим размером окна. Обратите внимание, что **упдатевидео** используется как для **WM \_ Paint** , так и для **\_ размера WM**.


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



Для сообщения **о \_ закрытии WM** Освободите указатели [**имфпмедиаплайер**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) и [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Реализация метода обратного вызова

Интерфейс [**имфпмедиаплайеркаллбакк**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) определяет один метод, [**онмедиаплайеревент**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Этот метод уведомляет приложение каждый раз при возникновении события во время воспроизведения. Метод принимает один параметр — указатель на структуру [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . Элемент **ивенттипе** структуры определяет произошедшее событие.

За структурой [**\_ \_ заголовков событий МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) могут следовать дополнительные данные. Для каждого типа событий определяется макрос, который приводит указатель **\_ \_ заголовка события МФП** к структуре, относящейся к конкретному событию. (См. раздел [**\_ \_ Тип события МФП**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)

Для этого руководства важны два события:



| Событие                                    | Описание                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_ \_ создан тип события МФП \_ MEDIAITEM \_** | Посылается после завершения [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . |
| **\_ \_ \_ набор MEDIAITEM типа события \_ МФП**     | Посылается, когда [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) завершается.                         |



 

В следующем коде показано, как привести указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к структуре, относящейся к конкретному событию.


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



Событие **МФП \_ \_ типа события \_ MEDIAITEM \_ Created** уведомляет приложение о завершении метода [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . Структура событий содержит указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , представляющий элемент мультимедиа, созданный из URL-адреса. Чтобы поместить элемент в очередь на воспроизведение, передайте этот указатель методу [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :


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



Событие **МФП \_ \_ типа события \_ MEDIAITEM \_ Set** уведомляет приложение о завершении [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) . Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать воспроизведение:


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



## <a name="implement-winmain"></a>Реализация WinMain

В оставшейся части этого руководства нет вызовов Media Foundation API. В следующем коде показана процедура окна:


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



`InitializeWindow`Функция регистрирует класс окна приложения и создает окно.


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



Наконец, реализуйте точку входа приложения:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



