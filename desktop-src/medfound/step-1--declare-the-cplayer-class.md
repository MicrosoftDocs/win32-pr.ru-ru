---
description: В этом разделе приведен шаг 1 из руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: Шаг 1. объявление класса Кплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61f03a9054e96769414320811d32a549027defb80ff929aba2c27ad4aa5b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112914"
---
# <a name="step-1-declare-the-cplayer-class"></a>Шаг 1. объявление класса Кплайер

В этом разделе приведен шаг 1 из руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

В этом руководстве функция воспроизведения инкапсулирована в `CPlayer` классе. Класс `CPlayer`объявляется следующим образом:


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



Обратите внимание на `CPlayer` следующее:

-   Событие "константа" **\_ \_ проигрывателя \_ приложений WM** определяет сообщение частного окна. Это сообщение используется для уведомления приложения о событиях сеанса мультимедиа. См. [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md).
-   `PlayerState`Перечисление определяет возможные состояния `CPlayer` объекта.
-   `CPlayer`Класс реализует интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , который используется для получения уведомлений о событиях из сеанса мультимедиа.
-   `CPlayer`Конструктор является закрытым. Приложение вызывает статический `CreateInstance` метод для создания экземпляра `CPlayer` класса.
-   `CPlayer`Деструктор также является закрытым. `CPlayer`Класс реализует **IUnknown**, поэтому время существования объекта регулируется с помощью счетчика ссылок (*m \_ нрефкаунт*). Чтобы уничтожить объект, приложение вызывает **IUnknown:: Release**, а не **Delete**.
-   `CPlayer`Объект управляет сеансом мультимедиа и источником мультимедиа.

## <a name="implement-iunknown"></a>Реализация IUnknown

`CPlayer`Класс реализует [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), который наследует **IUnknown**.

Приведенный здесь код является довольно стандартной реализацией **IUnknown**. При желании для реализации этих методов можно использовать библиотеку ATL. Однако не `CPlayer` поддерживает [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) или любые дополнительные функции COM, поэтому использовать ATL здесь не существует.


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



Далее. [Шаг 2. Создание объекта кплайер](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
