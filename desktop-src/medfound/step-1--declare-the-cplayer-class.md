---
description: В этом разделе приведен шаг 1 из руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: Шаг 1. объявление класса Кплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711390"
---
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="b4121-103">Шаг 1. объявление класса Кплайер</span><span class="sxs-lookup"><span data-stu-id="b4121-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="b4121-104">В этом разделе приведен шаг 1 из руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="b4121-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="b4121-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="b4121-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="b4121-106">В этом руководстве функция воспроизведения инкапсулирована в `CPlayer` классе.</span><span class="sxs-lookup"><span data-stu-id="b4121-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="b4121-107">Класс `CPlayer`объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4121-107">The `CPlayer` class is declared as follows:</span></span>


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



<span data-ttu-id="b4121-108">Обратите внимание на `CPlayer` следующее:</span><span class="sxs-lookup"><span data-stu-id="b4121-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="b4121-109">Событие "константа" **\_ \_ проигрывателя \_ приложений WM** определяет сообщение частного окна.</span><span class="sxs-lookup"><span data-stu-id="b4121-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="b4121-110">Это сообщение используется для уведомления приложения о событиях сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b4121-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="b4121-111">См. [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="b4121-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="b4121-112">`PlayerState`Перечисление определяет возможные состояния `CPlayer` объекта.</span><span class="sxs-lookup"><span data-stu-id="b4121-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="b4121-113">`CPlayer`Класс реализует интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , который используется для получения уведомлений о событиях из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b4121-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="b4121-114">`CPlayer`Конструктор является закрытым.</span><span class="sxs-lookup"><span data-stu-id="b4121-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="b4121-115">Приложение вызывает статический `CreateInstance` метод для создания экземпляра `CPlayer` класса.</span><span class="sxs-lookup"><span data-stu-id="b4121-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="b4121-116">`CPlayer`Деструктор также является закрытым.</span><span class="sxs-lookup"><span data-stu-id="b4121-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="b4121-117">`CPlayer`Класс реализует **IUnknown**, поэтому время существования объекта регулируется с помощью счетчика ссылок (*m \_ нрефкаунт*).</span><span class="sxs-lookup"><span data-stu-id="b4121-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="b4121-118">Чтобы уничтожить объект, приложение вызывает **IUnknown:: Release**, а не **Delete**.</span><span class="sxs-lookup"><span data-stu-id="b4121-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="b4121-119">`CPlayer`Объект управляет сеансом мультимедиа и источником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b4121-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="b4121-120">Реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4121-120">Implement IUnknown</span></span>

<span data-ttu-id="b4121-121">`CPlayer`Класс реализует [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), который наследует **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b4121-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="b4121-122">Приведенный здесь код является довольно стандартной реализацией **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b4121-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="b4121-123">При желании для реализации этих методов можно использовать библиотеку ATL.</span><span class="sxs-lookup"><span data-stu-id="b4121-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="b4121-124">Однако не `CPlayer` поддерживает [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) или любые дополнительные функции COM, поэтому использовать ATL здесь не существует.</span><span class="sxs-lookup"><span data-stu-id="b4121-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


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



<span data-ttu-id="b4121-125">Далее. [Шаг 2. Создание объекта кплайер](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b4121-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4121-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b4121-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4121-127">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="b4121-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="b4121-128">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4121-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
